# Tool Playbook: Exa and Apify

Verified usage rules, including the cost traps and silent failures. Everything here was hit in practice; none of it is in the tools' own descriptions.

## 1. Exa

Exa carries the bulk of the pipeline: discovery searches, page and PDF crawling, and (via its cached index) a fallback for pages that block direct crawls. The MCP server exposes several tools; these are the ones that matter.

### 1.1 Which tool when

| Tool | Use it for | Notes |
|---|---|---|
| `web_search_advanced_exa` | Default for discovery | Full filter surface: `numResults`, `type`, `category`, date filters, `includeDomains`, `includeText`/`excludeText`, `additionalQueries` |
| `web_search_exa` | Quick spot lookups | Fewer knobs, fine for "find me this one page" |
| `crawling_exa` | Full-page and PDF extraction by URL | Batch multiple URLs in one call |
| `company_research_exa`, `people_search_exa` | Optional conveniences | The same coverage is available via `category` filters on advanced search |
| `deep_researcher_start` / `_check` | Rarely | Only when shallow search has demonstrably failed on a deep angle |

### 1.2 The two cost traps

1. **Always set `maxCharacters` on every crawl** (a large value, e.g. `1000000`). Omitting it silently truncates pages at around 3,000 characters, and the truncation looks like a complete page. The cap governs how much text comes back, not billing.
2. **Always set `numResults` explicitly and never to 0.** `numResults: 0` silently bills for the default 10.

Also skip `enableSummary` and `enableHighlights` (extra cost per result; you are going to read the text anyway), and note that a search result's `text` field is substantial page content, not a snippet: score relevance from it **before** paying for a crawl. That pre-scoring step is the biggest single cost lever in the pipeline.

### 1.3 Query phrasing

Exa is a neural search engine. Phrase queries as natural language, never boolean or keyword strings:

- Good: `companies building identity infrastructure for AI agents that raised funding in 2025`
- Bad: `"AI agent" AND identity AND funding`

Filter quirks:

- `includeText` / `excludeText`: a single item of at most 5 words. Multiple items return a 400 error. For multi-term narrowing, use `additionalQueries` or post-filter the results yourself.
- `category: "company"` rejects date and text filters, and does not disambiguate name collisions (searching a common company name returns every entity sharing it). Pair it with `includeDomains` when the company's domains are known.
- Useful `category` values that work in practice: `research paper`, `company`, `news`, `personal site`, `financial report`.

### 1.4 Freshness

Date filters reflect publish or crawl dates, not content freshness. A stale page re-crawled yesterday passes a "past week" filter. For anything time-sensitive (package versions, prices, live statuses), fetch the system of record directly, for example with `curl` against a registry's JSON API or the regulator's own register. When a cached search result and a live fetch disagree, the live fetch wins.

### 1.5 The search motion (per gather round)

1. **Primary search**: the main query plus up to 3 `additionalQueries`, `numResults` around 15.
2. **Complementary search**: shifted filters or angle (different category, different date window, different phrasing).
3. **Score and dedupe** by URL against everything already collected; keep candidates that clear a relevance bar from their `text` field.
4. **Batch-crawl** the top 8 to 12 candidates in one `crawling_exa` call (one `urls` array, `maxCharacters` set).

### 1.6 Crawl failures and the fallback

When `crawling_exa` returns empty or errors on a URL, retry once via search: `web_search_advanced_exa` with the query set to the URL's host and path, `numResults: 3`. This hits Exa's cached index and recovers many JavaScript-heavy pages that the crawler cannot render. Classify every crawl honestly: `clean`, `partial`, `paywalled` (body under ~500 characters plus a subscribe prompt; no fallback exists, find another source), or `failed`. The file you saved is authoritative over what any agent claims it saved.

## 2. Apify

Apify covers what Exa cannot reach: login-gated LinkedIn content and X/Twitter. Treat it as the social supplement, not the primary engine.

### 2.1 Actors that work

| Actor | Use | Cost order | Notes |
|---|---|---|---|
| `harvestapi/linkedin-profile-posts` | LinkedIn posts from N profiles/companies | ~$1.50 per 1k posts | No cookies needed; batch all targets in one run via the `targetUrls` array |
| `apidojo/tweet-scraper` | X posts, primary | ~$0.0004 per tweet | One run per handle; search-mode query `from:{handle} since:{date} until:{date}` |
| `api-ninja/x-twitter-advanced-search` | X fallback | ~$0.01 per run | Only when the primary actor fails across the board; normalize its output keys to the primary's shape |
| `fastcrawler/x-twitter-article-to-markdown` | X Article (long-form) bodies | small, capped | At most 10 tweet IDs per run; pass the host tweet's own ID, never the article's ID |

Actor pricing drifts. Re-verify with `fetch-actor-details` (with pricing info) before a large run.

### 2.2 Transport quirks (the MCP layer)

- `call-actor`'s `waitSecs` (0 to 45) controls how long the call waits inline. There is no async flag; for longer runs, start the run and poll with `get-actor-run`.
- The dataset ID lives at `storages.datasets.default.id` in the run object, not at `defaultDatasetId`.
- `get-dataset-items` supports a `fields` projection: use it, because raw items can carry hundreds of fields that will flood your context. Quirk: array- and object-typed fields must be projected by their bare parent key (`author`, not `author.name`); dotted children of arrays are silently dropped.
- Page large datasets (`limit` + `offset` loop) instead of one giant read; a full unpaged read of a big dataset can idle past the transport timeout.

### 2.3 Budget guards

- The actors' own `maxPosts` / `maxItems` inputs are the **only** functional spend caps. Platform-level charge-cap fields exist but were verified non-functional; do not rely on them.
- `maxPosts: 0` means literally zero, not unlimited.
- Date-window queries: the `until` bound is exclusive. And on the X scraper, handle-mode with start/end parameters silently ignores the date window; use search-mode (`from:` query) when the window matters.
- Never attach custom map functions to the X scraper; it triggers automated bans.
- Enforce a per-run budget estimate before launching anything at scale: items times unit cost, written down, compared against what you are willing to spend. Actor docs will not stop you.

### 2.4 Fallback discipline

Fall back to the secondary X actor only when **all** handles in a run fail (a lane-wide outage). A partial result set usually means some accounts are genuinely quiet, and re-running them through a second actor doubles cost to confirm silence.

## 3. Direct fetches (the free third tool)

A surprising share of verification never needs a search product at all. `curl` against structured public APIs is free, fast, and primary:

- Package registries (npm, PyPI): versions, publish dates, maintainers, download counts, as JSON.
- GitHub REST API: org repo lists, repo metadata, branch comparisons, commit activity, contributor lists. Raw file access via `raw.githubusercontent.com`.
- Regulator and government registers: company registries, licensing registers, appointment rosters.
- HTTP status checks: a marketing page's "browse our code" link returning 404 is itself a finding.

The pattern: **search products for discovery, systems of record for verification.**
