---
description: Crawl one or more URLs via Exa with the tuned parameters, honest status classification, and the cached-index fallback
argument-hint: <url> [url ...] [--out=<dir>]
---

# Exa Crawl

Crawl the URL(s) in **$ARGUMENTS** and save the raw content to disk. If no URL was given, ask for one. Default output directory: the current company's topic gather folder if one is active, otherwise ask.

## Procedure

1. **Batch**: put every requested URL into a single `crawling_exa` call (`urls` array). Set `maxCharacters` to a large value (e.g. 1000000); omitting it silently truncates pages at ~3,000 characters. PDFs crawl the same way as pages.
2. **Save raw**: write each result to its own file in the output directory, named from the URL host and path, with a small header recording the URL, fetch date, and tool used. Never paraphrase into the raw file; it is evidence, not summary.
3. **Classify honestly**, per URL:
   - `clean`: substantive full content.
   - `partial`: content present but visibly incomplete (truncated tables, missing body sections).
   - `paywalled`: body under ~500 characters plus a subscribe/sign-in prompt. No fallback exists; report it and suggest finding the content elsewhere.
   - `failed`: empty or error.
4. **Fallback** (for `failed` and empty results, one retry only): `web_search_advanced_exa` with the query set to the URL's host + path, `numResults: 3`. This hits Exa's cached index and often recovers JavaScript-heavy pages. If the cache hit succeeds, save it and mark the file `clean (via cached index; check in-body dates for staleness)`.
5. **Time-sensitive content warning**: if the page carries versions, prices, or live statuses, note in the file header that a cached or crawled copy may lag the system of record, and suggest a direct `curl` of the underlying API when one exists (`playbook/04-tools.md` section 3).

## Return

A per-URL table: URL, status, output file path, one-line content summary. The file on disk is authoritative; never report a save that did not happen.
