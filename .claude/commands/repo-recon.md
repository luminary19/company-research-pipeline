---
description: Explore a GitHub organization or repository for product research, scan first then dive
argument-hint: <owner or owner/repo> [--out=<dir>]
---

# Repo Recon

Explore the GitHub target in **$ARGUMENTS** to establish what a company's public code actually shows: what is real, what is active, what is a shell. If no target was given, ask.

The engineering surface is one of the highest-signal, lowest-cost verification sources in company research: it is primary, it is dated, and it cannot be retro-edited the way a marketing page can.

## Step 1: Scan (breadth before depth)

Use free direct fetches (`curl`) against the GitHub REST API; no search product needed:

1. **Org level** (when the target is an owner): `GET /orgs/{owner}/repos` (or `/users/{owner}/repos`). Capture per repo: name, description, language, created/pushed dates, stars, forks, archived flag.
2. **Repo level**: `GET /repos/{owner}/{repo}` for metadata, then the README via `raw.githubusercontent.com/{owner}/{repo}/{default_branch}/README.md`, then the file tree via the contents or git-trees API.
3. Build the scan report: a repo inventory table plus, for the focal repo, the README summary and tree outline, ending with 3 to 6 **drill candidates** (the files or questions most worth a deep look).

Present the scan and pause: let the user pick drill targets before spending depth.

## Step 2: Dive (rounds, on request)

Per drill round: fetch the chosen files (raw fetches; `/exa-crawl` for rendered pages like release notes or hosted docs), and answer the round's question concretely.

High-signal checks for company research, from practice:

- **Activity reality**: last-push dates across the org. One actively committed repo surrounded by frozen forks tells you where the real work is (usually a private monorepo).
- **Fork depth**: for a repo forked from an upstream, `GET /repos/{owner}/{repo}/compare/{upstream-default}...{default}` shows ahead/behind counts. Check a rebase or integration branch too; a big behind-count on the default branch often just means upstream velocity, not dormancy. The ahead-commits are the company's actual contribution; read their themes.
- **Shipped vs marketed**: does the "get started" repo linked from marketing actually contain code? Does the SDK's repository field resolve (a 404 means closed source behind a public npm package)?
- **External traction**: stars, forks, and who imports the packages. Registry download curves that spike on release dates and collapse between them indicate internal CI, not adoption.
- **Cross-check the package registry** directly (`registry.npmjs.org/{package}` JSON): versions, publish cadence, maintainers. Live registry beats any cached search result.

## Step 3: Report

Write the exploration report to the output directory: scan inventory, per-round findings with URLs, and an honest bottom line on what the public engineering surface does and does not prove. Every claim carries its API URL or file link. Findings feed the **product** dossier (buildable state) and the **activity** dossier (momentum signals); route accordingly via the inbound queue.
