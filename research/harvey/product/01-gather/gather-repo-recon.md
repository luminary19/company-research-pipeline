---
type: Gather Report
topic: product
slice: repo-recon
company: Harvey (harvey.ai)
date: 2026-07-04
rounds_run: 4
stop_reason: Public engineering surface fully enumerated (org, 7 repos, 2 registries) with positive controls; GitHub unauth budget approaching limit (44/60 → ~30 left). Diminishing returns.
---

## Scope

Establish what Harvey's **public** code surface actually shows (real / active / shell) as a primary, un-retro-editable verification source for the **product** dossier. Slice: **public engineering surface — GitHub + package registries.**

Method: free direct fetches (curl) against the GitHub REST API, raw.githubusercontent.com, the npm registry search + package JSON, and the PyPI JSON API. GitHub API is the system of record (R1); everything below carries its exact API URL. Confirmed org = **github.com/harveyai** (NOT harvey-ai, NOT the empty counsel-ai).

**What this surface CAN prove:** existence, activity dates, contributor identities, license, dependency/stack signals, and whether a public SDK exists — none of which can be back-dated or retro-edited like a marketing page. **What it CANNOT prove:** anything about the private product monorepo, production infra scale, revenue, or customer count. LAB is a *benchmark*, not the product. Absence of a public SDK is consistent with a closed product behind private infra, and is reported as such.

## Findings

### 1. Org overview

`GET https://api.github.com/orgs/harveyai` — org **"Harvey"**, created **2022-11-08**, blog `https://www.harvey.ai`, location "United States of America", **7 public repos**, **138 followers**, updated 2026-04-05. Company/email fields blank. [R1·C1]

### 2. Full repo inventory

`GET https://api.github.com/orgs/harveyai/repos?per_page=100&sort=pushed` [R1·C1]

| Repo | Orig/Fork | Lang | ★ | Forks | Created | Last push | Archived | Role |
|---|---|---|---|---|---|---|---|---|
| **harvey-labs** (LAB) | Original | Python | 467 | 102 | 2026-03-30 | **2026-07-01** | no | Legal Agent Benchmark — the one actively-committed repo |
| **biglaw-bench** | Original | (docs/PDF) | 168 | 23 | 2024-08-24 | 2026-03-17 | no | Earlier legal eval benchmark + document corpus |
| **deep-research-starter** | Original | Python | 11 | 1 | 2025-07-02 | 2025-07-02 | no | Demo: OpenAI Deep Research API (Streamlit); one-day repo |
| **teams-ai** | Fork (microsoft/teams-sdk) | C# | 4 | 0 | 2024-07-16 | 2024-09-20 | no | MS Teams bot SDK; **2 Python commits ahead** |
| **Recognizers-Text** | Fork (microsoft/Recognizers-Text) | C# | 4 | 0 | 2024-07-17 | 2024-07-22 | no | Date/number/unit entity recognition |
| **pdfplumber** | Fork (jsvine/pdfplumber) | (Python) | 7 | 1 | 2024-02-21 | 2024-02-17 | **yes** | PDF text/table extraction; **0 commits ahead** (pure snapshot) |
| **react-doc-viewer** | Fork (cyntler/react-doc-viewer) | TypeScript | 6 | 1 | 2023-02-23 | 2023-02-24 | **yes** | React file/PDF viewer; **1 commit ahead**, published to npm |

**Activity reality:** exactly ONE repo (`harvey-labs`) is under active commit (PRs merged through 2026-07-01, i.e. days before the recon date). `biglaw-bench` froze in Mar 2026; `deep-research-starter` was a single-day July-2025 demo; all four forks froze in 2023–2024 and two are archived. This is the expected shape when the real product is a **private monorepo** and the public surface is research/eval + a few reference forks.

### 3. Focal dive — `harveyai/harvey-labs` (LAB, "Legal Agent Benchmark")

- **Meta** (`GET /repos/harveyai/harvey-labs`): **MIT license**, size ~503 MB (heavy document corpus), 467★ / 102 forks, 26 open issues, homepage = `harvey.ai/blog/introducing-harveys-legal-agent-benchmark`. [R1·C1]
- **Languages** (`/languages`): Python 494,736 · Shell 16,286 · Dockerfile 3,032 · JavaScript 2,806 — overwhelmingly Python. [R1·C1]
- **README** (`raw.githubusercontent.com/harveyai/harvey-labs/main/README.md`): LAB = "open-source benchmark for evaluating agents on real legal work," two parts — a **dataset of tasks** (agent instructions + documents + rubrics) and an **execution harness** for running/evaluating agents. Badges claim **1,660 tasks** across **24 practice areas + contracting**, MIT. Docs: `architecture.md`, `eval-strategies.md` (all-pass rubric scoring + LLM judge), `tutorial.md` (an M&A data-room assignment end-to-end). [R1·C1]
- **File tree** (`/git/trees/main?recursive=1`): **15,902 blobs**. Real, non-shell structure:
  - `harness/` — `agent_loop.py`, `run.py`, `tools.py`, `system_prompt.md`, and **6 model adapters**: `anthropic.py`, `openai.py`, `google.py`, `mistral.py`, `fireworks.py`, `baseten.py` (all OpenAI-compatible chat-completions style).
  - `harness/skills/{docx,pptx,xlsx}/` — real document-manipulation tooling (redline/accept-changes/comments for docx, deck generation for pptx, workbook build/recalc for xlsx), each with a `SKILL.md` + Python/JS scripts. This mirrors the actual Harvey product surface (Word/PowerPoint/Excel work-product).
  - `evaluation/` — `judge.py`, `scoring.py`, `run_eval.py`, `compare.py`, `charts.py`, `report.py` + rubric prompt.
  - `sandbox/` — Dockerized execution sandbox with a PDF parser.
  - `tasks/` — the corpus.
- **Task taxonomy** (derived from tree): **1,749 `task.json` files** across **25 practice-area folders** (README badge says 1,660 — treat the discrepancy as raw-file-count vs curated-count, not verified). Distribution: contracts 498, corporate-ma 161, intellectual-property 147, corporate-governance 97, trusts-estates 77, funds-asset-mgmt 66, litigation 52, then a long tail (antitrust, tax, bankruptcy, immigration, white-collar, etc.). Each task ships real synthetic documents (`.docx/.pptx/.xlsx/.eml`) + a `task.json`. [R1·C1]
- **Dataset availability:** tasks + documents are committed directly into the public MIT repo (no gated download). Dataset is **openly available**.
- **Recent commits** (`/commits?per_page=12`) — active, plural authors, real engineering: Baseten adapter (#84, 2026-06-24), Fireworks adapter (#83), doc-coverage denominator fix, UTF-8/cp1252 Windows fix, 409 contract-negotiation tasks added (#81, Niko Grupen), Gemini/OpenAI/Mistral judge support (#55). [R1·C1]

### 4. `harveyai/biglaw-bench` (earlier benchmark)

`GET /repos/harveyai/biglaw-bench` — **no license file**, 63 blobs, last push 2026-03-17. README: "BigLaw Bench … developed by Harvey's legal research team," three parts — **Core** (transactional + litigation task categories), **Workflows** (agentic composite tasks; SPA Deal Points extraction), **Retrieval** (merger agreements, SPAs, discovery emails). Repo ships real primary legal PDFs (e.g. D.D.C. docket filings, Enron/AES call transcripts, named merger agreements). This is the predecessor to LAB; LAB is the actively-maintained successor. [R1·C1]

### 5. Contributors (people-signal → route to people dossier)

`GET /repos/harveyai/harvey-labs/contributors` and `/biglaw-bench/contributors` [R1·C1]

**harvey-labs:** `spencerp` (7), `EnesYilmazcode` (Enes Yilmaz, 2), `ngrupen` (**Niko Grupen**, 2), `Abid-cognida` (2), `aaron-ellisbloor` (1), `charlieoneill11` (Charlie O'Neill, 1), `ClemenceLanfranchi` (1), `JarettForzano` (1), `KilgoreHerring` (1), `renantrendt` (1), `SandyYuan` (Sihan "Sandy" Yuan, 1).

**biglaw-bench:** `ngrupen` (**Niko Grupen**, 20 — clearly the primary author), `annazhang-harvey` (2), `GabrielPereyra` (1).

Cross-check notes (report evidence, no conclusion):
- **Niko Grupen (ngrupen)** — confirmed present and central (top biglaw-bench author, active LAB committer). Matches the known-name list.
- The Pereyra on the known-name list should be checked: the GitHub login is **`GabrielPereyra`** with email **`gabe@harvey.ai`** (see registry section), i.e. **Gabriel Pereyra**, not "Julio Pereyra." Flagging the name discrepancy for the people dossier to resolve.
- `Abid-cognida` and `annazhang-harvey` carry org suffixes in their logins ("-cognida" possibly a vendor/contractor, "-harvey" an internal). Worth a people-dossier cross-check.

### 6. Package registries — is there a public Harvey SDK? (**answer: no official SDK/API client**)

**npm** (`https://registry.npmjs.org/-/v1/search?text=...`): a search for `harvey legal` returns only unrelated packages (Harvest CLI, Datadog, ckeditor, etc.) — search demonstrably works and returns results, just none from Harvey. A search for `harvey.ai` surfaces **`@harvey.ai/react-doc-viewer`** — and its package JSON (`registry.npmjs.org/@harvey.ai%2Freact-doc-viewer`) confirms **Harvey maintainers**: `daniel@harvey.ai` (thedch), `gabe@harvey.ai` (gabrielpereyra), plus the upstream fork author. Created 2023-02-24, description "File viewer for React." **This is a forked UI component, not an SDK/API client** — it lines up exactly with the `react-doc-viewer` fork (see §7). `scope:harveyai` search returns zero packages — no official npm org namespace. [R1·C1]

**PyPI** (JSON API existence checks): `harvey-ai`, `harveyai`, `harvey-legal`, `harvey-sdk`, `harvey-labs`, `harvey-client`, `biglaw-bench` → all **HTTP 404**. `harvey` → HTTP 200 but is an **unrelated** project (`architv/harvey`, "helps you manage and choose a license from the command line," author Archit Verma) — NOT the legal-AI company. [R1·C1]

**Positive control (proves the absence is real, not a broken query):** the same PyPI JSON endpoint returns HTTP 200 for `openai`, `anthropic`, `langchain`, and `lexnlp`; the npm search returns dozens of live packages. The tooling works — Harvey simply publishes **no official Python or JS SDK / API client**. Finding: **Harvey's product is closed-source behind private infra; the only Harvey-published registry artifact is a minor forked React viewer component from 2023.**

### 7. Shipped-vs-marketed cross-check (forks = stack signal)

Fork ahead/behind via `GET /repos/harveyai/<fork>/compare/<upstream:branch>...harveyai:<branch>` [R1·C1]:
- **react-doc-viewer** — `cyntler:main...harveyai:main`: **ahead 1 / behind 141, archived.** The single Harvey commit: *"Default to smooth scroll in pdf view for harvey"* (bkakadiya42, 2023-02-23), published ~35 min later as `@harvey.ai/react-doc-viewer` on npm. → Harvey **did** modify it (minimally) and shipped it; stack signal: **in-app React PDF/document viewing** (2023-era).
- **pdfplumber** — `jsvine:stable...harveyai:stable`: **ahead 0 / behind 132, archived.** Zero Harvey commits — a pure reference snapshot. Stack signal: **PDF text/table extraction** was on their radar (used as-is, not customized).
- **teams-ai** — `microsoft:main...harveyai:main`: **ahead 2 / behind 504.** Two Python commits by `skoryky` (2024-07-17): *"Avoid returning token prematurely on signin/verifyState invoke"* and *"Copy activity to new activity when continuing conversation"* — bot-framework auth/continuation fixes. Stack signal: a **2024 Microsoft Teams bot integration** effort (Python), consistent with an enterprise-distribution channel.
- **Recognizers-Text** — fork of Microsoft's date/number/unit entity recognizer (C#), unmodified snapshot. Stack signal: structured entity extraction.

The marketing-linked "starter" repo (`deep-research-starter`, linked from `harvey.ai/blog/integrating-deep-research-into-harvey`) contains **real runnable code** — a Streamlit app + OpenAI Deep Research API samples, MIT, sole contributor `calvinqi`, built in one day (2025-07-02). Confirms Harvey publicly integrates the **OpenAI Deep Research API**.

## Reflection trace

- **Round 1 (org + inventory + registries):** Pulled org meta, full repo list, npm/PyPI first passes. Immediately confirmed the "one live repo among frozen forks" shape and that npm/PyPI first-pass search found no Harvey SDK. PyPI HTML-scrape returned 0 (unreliable) → flagged to redo via JSON API.
- **Round 2 (focal dive):** harvey-labs meta/languages/contributors/commits/tree + biglaw-bench meta/contributors/tree + PyPI JSON existence checks **with a positive control**. The positive control was necessary — a bare "404" list would be indistinguishable from a broken query; showing `openai`/`anthropic` = 200 proves the absence is real.
- **Round 3 (README + identity + forks):** README taxonomy (1,660 badge vs 1,749 raw files — kept both, verified neither as canonical), confirmed PyPI `harvey`=200 is an unrelated project (identity trap avoided), and confirmed `@harvey.ai/react-doc-viewer` is Harvey-owned (maintainer emails) — reclassifying it from "possible SDK" to "forked UI component."
- **Round 4 (fork diffs):** compare API quantified each fork's modifications, converting "they have a fork" into "they added N specific commits" — the difference between a snapshot and real work. Surfaced the `GabrielPereyra`/`gabe@harvey.ai` identity that resolves the react-doc-viewer publisher and flags the "Julio vs Gabriel Pereyra" name discrepancy.
- **Stop:** public surface exhausted (7 repos, 2 registries, all forks diffed) and GitHub unauth budget down to ~30/60. Further calls would be low-yield.

## Gaps and not-found

- **README byte-count discrepancy** — README badge says **1,660 tasks**; the tree has **1,749 `task.json` files**. Not reconciled (curated vs raw count, or in-flight additions). Do not treat either as the verified figure without deeper inspection.
- **Name discrepancy** — task brief lists "Julio Pereyra"; the actual GitHub/email identity is **Gabriel Pereyra (`gabe@harvey.ai`, login `GabrielPereyra`)**. People dossier to resolve whether "Julio" is an error or a second person.
- **Private monorepo is invisible** — none of this touches Harvey's actual production codebase, infra scale, or model stack. The public repos are research/eval + reference forks only.
- **Contributor employment not verified** — logins are strong hints (esp. `-harvey`/company-suffixed and `@harvey.ai` emails) but this slice did not confirm each contributor's role/employment; that is a people-dossier task.
- **Did not fetch** individual `task.json` contents, `docs/architecture.md`/`eval-strategies.md` full text, or `harness/system_prompt.md` (available for a deeper product-mechanics pass if the dossier needs the actual eval methodology or the agent system prompt).
- **NuGet not checked** — the two C# forks (teams-ai, Recognizers-Text) suggest a .NET footprint; a NuGet search for Harvey-published packages was out of scope here.

## Sources consulted (all R1·C1 unless noted; GitHub REST API + raw + registry JSON = primary, dated, un-retro-editable)

- `https://api.github.com/orgs/harveyai`
- `https://api.github.com/orgs/harveyai/repos?per_page=100&sort=pushed`
- `https://api.github.com/repos/harveyai/harvey-labs`
- `https://api.github.com/repos/harveyai/harvey-labs/languages`
- `https://api.github.com/repos/harveyai/harvey-labs/contributors?per_page=30`
- `https://api.github.com/repos/harveyai/harvey-labs/commits?per_page=12`
- `https://api.github.com/repos/harveyai/harvey-labs/git/trees/main?recursive=1`
- `https://raw.githubusercontent.com/harveyai/harvey-labs/main/README.md`
- `https://api.github.com/repos/harveyai/biglaw-bench` · `/contributors` · `/git/trees/main?recursive=1`
- `https://raw.githubusercontent.com/harveyai/biglaw-bench/main/README.md`
- `https://api.github.com/repos/harveyai/deep-research-starter` · `/contributors`
- `https://raw.githubusercontent.com/harveyai/deep-research-starter/main/README.md`
- `https://api.github.com/repos/harveyai/{pdfplumber,react-doc-viewer,teams-ai,Recognizers-Text}` (parent + branch metadata)
- `https://api.github.com/repos/harveyai/react-doc-viewer/compare/cyntler:main...harveyai:main`
- `https://api.github.com/repos/harveyai/pdfplumber/compare/jsvine:stable...harveyai:stable`
- `https://api.github.com/repos/harveyai/teams-ai/compare/microsoft:main...harveyai:main`
- `https://registry.npmjs.org/-/v1/search?text=harvey%20legal` · `?text=harvey.ai` · `?text=scope:harveyai`
- `https://registry.npmjs.org/@harvey.ai%2Freact-doc-viewer`
- `https://pypi.org/pypi/{harvey,harvey-ai,harveyai,harvey-legal,harvey-sdk,harvey-labs,harvey-client,biglaw-bench}/json`
- Positive controls: `https://pypi.org/pypi/{openai,anthropic,langchain,lexnlp}/json` (all HTTP 200)
- `https://api.github.com/rate_limit` (budget tracking)
