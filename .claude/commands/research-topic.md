---
description: Run one topic dossier through the eight-step pipeline (load, gather, compile, verify, attack, supplement, write, distribute)
argument-hint: <company-slug> <topic: thesis|company|product|buyers|competitive|activity|people>
---

# Research Topic

Build one dossier for: **$ARGUMENTS** (a company slug and a topic). If either is missing, ask. The company folder `research/{slug}/` must exist (run `/research-company` first if not). The topic's question, ownership boundary, and analytical spine are defined in `playbook/03-topics.md`; the full method is `playbook/01-pipeline.md` section 2.

## Step 1: Load

Read in full: `00-scope.md`, `00-coverage-map.md`, every already-written `dossier-*.md` for this company, and this topic's `inbound-queue/pending/` entries. Then draft the dossier's **section plan**: the numbered sections, each defined by the question it answers (scaffolding, never conclusions). Present the section plan plus the sub-question carve for the gather, and pause for approval.

## Step 2: Gather

Fan out 2 to 4 parallel research agents, each owning a disjoint sub-question slice. When the topic's evidence lives on LinkedIn or X, include a slice that runs the `/social-crawl` motion; when the company has public repos and the topic is product, include a `/repo-recon` slice. Dedicate one slice (or one agent) to the **skeptic pass**: hunting evidence against the scope's stated prior.

Every gather agent prompt must include:

- The slice: sub-questions covered, sub-questions explicitly excluded.
- The loop: up to 3 reason-search-reflect rounds; at most 2 Exa searches plus 1 batched crawl per round; stop on the named-gap test, diminishing returns, or the round cap.
- The grading rules: two-axis `[R·C]` per source, sole-source caps at C3 (`playbook/02-epistemics.md` section 3).
- The tool rules: `playbook/04-tools.md` (crawl `maxCharacters`, explicit `numResults`, natural-language queries, pre-score from result text before crawling, live-fetch systems of record for time-sensitive facts).
- Organize-only: report sourced findings, never conclusions or tags. Every finding carries its external source URL.
- Output: one file per agent at `research/{slug}/{topic}/01-gather/gather-{slice}.md` per `templates/gather-report.md`.
- Read files past truncation.

After the agents return, verify their output files exist on disk before proceeding.

## Step 3: Compile

Merge the gather reports into `01-gather/compiled.md`: dedupe by URL and claim, structure by the section plan, preserve every citation and grade. Update `00-coverage-map.md` (solid / needs-verify / missing).

## Step 4: Verify

Triage: list the claims that are load-bearing AND (single-source, old, of unknown origin, or time-sensitive). Fan out verification agents over that list, framed adversarially ("your job is to refute this claim"), targeting primary records: regulator registers, package-registry APIs, live product docs, official rosters, direct `curl` fetches. Rules: verify against running systems, and every absence finding needs a positive control (`playbook/02-epistemics.md` sections 5 and 7).

Output: `02-verification/verify-{batch}.md` per `templates/verification-report.md`, with a verdict table (CONFIRMED / REFUTED / PARTIAL, confidence, primary source) and surfaced conflicts.

## Step 5: Critical attack

Yours alone; never delegated. Attack the assembled picture: weak load-bearing claims, unexamined surfaces, quiet contradictions, anything that would embarrass you if the company read it. Output: a target list for Step 6, or a decision that the gaps are framing (fix at write time) rather than coverage.

## Step 6: Supplement

Only the attack's named gaps. Small targeted agent runs, same rules as Step 2. Skip entirely when the attack surfaced no coverage gaps.

## Step 7: Write

Write `research/{slug}/dossier-{topic}.md` yourself, once, from the compiled gather, the verification verdicts, and the inbound-queue entries, following `templates/dossier.md` exactly:

- Ownership header (Owns / Does NOT own, naming the other six topics' homes).
- Tag legend, then purpose-led sections.
- Every load-bearing claim: in-text citation plus `[F/I/A + NN%]` tag, assigned by you now (calibration guide: `playbook/02-epistemics.md` section 1).
- Conflicts surfaced with both values and both sources.
- Inbound-queue entries adjudicated: primary-verified findings supersede unverified ones; independent findings coexist; unconfirmed ones enter as low-confidence inference or an open question.
- Open Questions / Decisions Pending, Key Terms, full Reference List.

## Step 8: Distribute

Walk all seven topics **by name**, asking for each: what did this session find that that topic owns? For each net-new finding (drop test: would the owner's own gather find it anyway?), write one file to `research/{slug}/{other-topic}/inbound-queue/pending/`: headline, 1 to 2 sentences, citation, source note, topical home hint. Then drain backflow into any already-written dossier (absorb surgically, merge references, tag, move the queue file to `archive/`), and log one line per event in `00-progress.md`.

Close by reporting: dossier path, claim counts by tag class, conflicts surfaced, queue entries routed, and which topic is next.
