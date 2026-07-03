---
description: Orchestrate the full company-research pipeline for one company (scope, recon, seven topic dossiers, integration)
argument-hint: <company name>
---

# Research Company

Run the full pipeline from `playbook/01-pipeline.md` for the company: **$ARGUMENTS**

If no company name was given, ask for one before doing anything else.

## Step 1: Resolve state

1. Derive the working slug (kebab-case of the company name) and check whether `research/{slug}/` already exists.
2. If it exists, read `research/{slug}/00-progress.md` and `00-coverage-map.md`, report where the engagement stands (which dossiers are done, what is queued), and resume from the next undone phase below. Do not redo completed work.
3. If it is new, continue to Step 2.

## Step 2: Scope (Phase 0)

Interview the user briefly (3 questions maximum):

1. Why this company, and what decision does the research feed?
2. What is your current prior about the company? (Stated plainly; it will be tested, not protected.)
3. Any known constraints: deadline, topics that matter most, sources to avoid?

Then scaffold the working folder:

```
research/{slug}/
├── 00-scope.md            the answers above, written down
├── 00-progress.md         one line per session/event; backflow log table
├── 00-coverage-map.md     from templates/coverage-map.md
└── {topic}/               created lazily, one folder per topic as each starts
    ├── 01-gather/
    ├── 02-verification/
    └── inbound-queue/{pending,archive}/
```

## Step 3: Recon (Phase 1)

Run the recon pass per `playbook/01-pipeline.md` Phase 1:

1. Broad Exa discovery across the company name, products, founders, funding, press. Natural-language queries; follow `playbook/04-tools.md` for parameters.
2. Crawl the obvious primary surfaces (site, docs, blog, careers, funding databases, GitHub org) via the `/exa-crawl` motion.
3. Record name collisions the moment you notice them.
4. Write `00-recon.md` (provisional, labeled as such) and seed `00-coverage-map.md`.

Pause and present the recon summary plus the proposed topic order before continuing.

## Step 4: Topic dossiers (Phase 2)

Walk the seven topics in order (thesis, company, product, buyers, competitive, activity, people; rationale in `playbook/03-topics.md`), **one per session**:

- For each topic, invoke `/research-topic {slug} {topic}`.
- After each dossier, update `00-progress.md` and the coverage map, and confirm the distribute step ran (the seven-topic walk).
- At session end, tell the user which topic is next so the engagement resumes cleanly.

## Step 5: Integration (Phase 3)

After the seventh dossier:

1. Drain every topic's `inbound-queue/pending/`.
2. Re-read each dossier's Open Questions; close what later dossiers answered.
3. Write `synthesis.md`: the answer to the Step 2 decision question, drawing on all seven dossiers, with each dossier's load-bearing tension stated honestly, every claim tagged and cited per `playbook/02-epistemics.md`.

## Rules that bind every step

- One topic per session. Do not chain dossiers in one context window.
- You (the main conversation) own judgment steps: critical attack, tag assignment, dossier writing, synthesis. Agents own legwork: gather, verification fetches.
- Every sub-agent prompt includes: the slice it owns, the grading rules (`playbook/02-epistemics.md` sections 3 and 7), the Exa/Apify parameter rules (`playbook/04-tools.md`), the output template path, and the instruction to read files past truncation.
