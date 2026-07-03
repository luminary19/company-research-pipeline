---
description: Pull LinkedIn posts or X/Twitter posts via Apify actors, with budget guards and paged dataset reads
argument-hint: <linkedin profile/company URLs, or X handles> [--days=N] [--max-per-source=N] [--out=<dir>]
---

# Social Crawl

Pull recent posts for the targets in **$ARGUMENTS** via Apify. LinkedIn targets are profile or company URLs; X targets are bare handles. Default window: 7 days. Default cap: 30 posts per source. If no targets were given, ask.

Requires the Apify MCP server. Full quirk reference: `playbook/04-tools.md` section 2.

## Step 1: Budget gate (always, before any run)

Estimate the spend: targets x cap x unit cost (LinkedIn ~$1.50 per 1k posts via `harvestapi/linkedin-profile-posts`; X ~$0.0004 per tweet via `apidojo/tweet-scraper`). Present the estimate and the caps, and get a yes before launching. Actor pricing drifts; for large runs, re-verify with `fetch-actor-details` first. The actors' own `maxPosts` / `maxItems` inputs are the only functional spend caps; do not trust platform-level charge caps.

## Step 2: Run

**LinkedIn** (one batched run for all targets):

- Actor: `harvestapi/linkedin-profile-posts`, input `{ targetUrls: [all URLs], maxPosts: <cap> }`.
- `maxPosts: 0` means zero, not unlimited.

**X** (one run per handle):

- Actor: `apidojo/tweet-scraper`, input `{ searchTerms: ["from:{handle} since:{YYYY-MM-DD} until:{YYYY-MM-DD}"], maxItems: <cap>, sort: "Latest" }`.
- Use search-mode `from:` queries as shown; handle-mode silently ignores date windows. `until` is exclusive. Never attach a custom map function (automated ban risk).
- Long-form X Articles: enrich via `fastcrawler/x-twitter-article-to-markdown`, at most 10 tweet IDs per run, passing the host tweet's own ID (never the article's ID).

Transport: `call-actor` with `waitSecs` up to 45; if the run is still going, poll `get-actor-run`.

## Step 3: Read results (paged, projected)

- The dataset ID is at `storages.datasets.default.id` in the run object.
- Read with `get-dataset-items` using a `fields` projection to keep the payload small. Quirk: array/object fields project by bare parent key (`author`, not `author.name`).
- Page with `limit` + `offset` (LinkedIn: ~15 per page; X: large limits are fine). Never one giant unpaged read.

## Step 4: Save + fallback

Write one markdown file per source to the output directory: header (source, window, run cost, fetch date), then one entry per post (date, text, engagement, URL). Files are evidence; do not editorialize in them.

X fallback: only when **all** handles in a run fail (lane-wide outage), rerun via `api-ninja/x-twitter-advanced-search` and normalize its output keys to the primary actor's shape. A partial result set means some accounts are genuinely quiet; do not double-spend to confirm silence.

## Return

Per-source table: source, posts retrieved, window actually covered, output file, cost. Plus the run total against the Step 1 estimate.
