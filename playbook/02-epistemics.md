# Epistemics: The Rules That Keep You Honest

Research pipelines fail quietly. The search works, the prose reads well, and the conclusions are subtly wrong because a marketing page got treated as a shipped product, a stale cache got treated as current, or a single vendor figure got repeated until it looked corroborated. This file is the guard rail set. It is short, and every rule in it was earned by hitting the failure it prevents.

## 1. The claim tag: [F/I/A + NN%]

Every load-bearing claim in a dossier carries a tag:

| Tag | Meaning | Example |
|---|---|---|
| `[F/NN%]` | **Fact**: checked against a primary source | `The seed round closed in April 2025 [F/97%]` |
| `[I/NN%]` | **Inference**: your reasoning from evidence | `The launch burst reads as pre-fundraise positioning [I/80%]` |
| `[A/NN%]` | **Assumption**: unproven, but must hold for the read to stand | `Identity is the durable layer [A/55%]` |

`NN%` is your confidence, assigned by you at write time. Never let a gather or verification agent assign the final tag; agents report evidence, you adjudicate.

**Split tags** are allowed and often more honest: a vendor survey supports `[F/90% that it is claimed, I/60% that it is representative]`. A judgment call layered on solid signals supports `[F/85% on the signals, I/70% on the conclusion]`.

Calibration guide, from practice:

- Multiple independent primary sources agreeing verbatim: F at 90 to 97.
- Single primary source, no contradiction found after adversarial search: F at 85 to 90.
- Company self-reported figure, unaudited: F at 80 to 90 **that it is claimed**; the truth of the figure is a separate, lower-confidence judgment.
- Well-evidenced reasoning: I at 65 to 85. If your inference deserves more than 85, look for the primary source that would make it a fact.
- A load-bearing assumption you cannot test from outside: A at 40 to 60, and it belongs in the "what must be true" list, not buried in prose.

## 2. The iron rule of citation

No fact without an in-text citation that resolves to an openable URL, and a reference list entry at the end of the dossier. If a finding cannot be traced to an external source, it is labeled unverified and treated as a lead, not a fact.

Corollary: **gather output is an unverified baseline, even when cited.** Extraction-stage citations prove where a claim came from, not that it is true. The verify step is what upgrades a claim to primary-confirmed.

## 3. Two-axis source grading: [R·C]

Every source a gather agent uses gets graded on two independent axes.

**Reliability (R): the provenance of the source, independent of any claim.**

| Grade | Meaning |
|---|---|
| R1 | Authoritative: peer-reviewed, official filings, regulator records, primary data |
| R2 | Credible: established outlets, industry bodies, reputable research firms |
| R3 | Practitioner: trade press, expert blogs, vendor documentation |
| R4 | Weak: self-published, promotional, unattributed |

**Credibility (C): corroboration of the specific claim.**

| Grade | Meaning |
|---|---|
| C1 | Corroborated: two or more independent sources agree |
| C2 | Consistent: aligns with other evidence, not directly confirmed |
| C3 | Uncorroborated: single source, plausible |
| C4 | Contested: sources disagree |

Two deterministic rules that prevent the most common grading inflation:

1. **A source that is the sole origin of its figure caps at C3**, no matter how many outlets repeat it. Ten articles citing one vendor survey is one source.
2. **Reliability is relative to the claim type.** A vendor's docs are R3-authoritative for "what the vendor markets" and much weaker for "what is true about the market." A source used outside its competence gets capped down.

Synthesis weights findings by grade, never by retrieval order. The first result is not the best result.

## 4. Conflicts are surfaced, never silently resolved

When two sources disagree on a number, a date, or a fact: both values and both sources go in the dossier, marked as a surfaced conflict. Resolve it only when a primary record settles it, and then say so ("resolved in favor of the primary record"). Surfacing the conflict IS the deliverable; a dossier that reads too clean has usually laundered its conflicts.

## 5. Marketed versus shipped

The single most valuable distinction in company research. A company's product pages are the primary source for **what the company markets**. What actually ships is a different question, answered by different sources: the live docs' availability tables, the package registry, the public repos, named customers, third-party integration evidence. Keep the two layers separate in the dossier, and expect them to disagree; where they disagree is usually the most important finding in the whole engagement.

## 6. Identity verification before attribution

Before attributing any finding to a person: name AND role AND company must match. Common names contaminate searches, and portfolio ecosystems recycle the same people across entities. One mis-attributed quote can poison a person-level dossier.

The same applies to companies: watch for name collisions (an unrelated company, a place, an open-source project sharing the name) and record known collisions in the coverage map so every later search excludes them.

## 7. The absence-of-evidence ban

"X was not found" is a finding about your search, not about the world, until you add a **positive control**: demonstrate that the method finds known-present items. "The company appears on no standards-body roster (and the rosters checked do list its named peers, so the method finds members)" is a publishable finding. Without the control, it is a search failure waiting to embarrass you.

## 8. Freshness is not what it looks like

Search-index date filters reflect publish or crawl dates, not content freshness; a stale page re-crawled yesterday looks current. For anything time-sensitive (versions, prices, statuses, live availability), go to the system of record: the registry's JSON API, the regulator's register, the live docs page, fetched directly. A cached search result once reported a package version that the live registry contradicted; the live registry was right.

## 9. Read files in full

Agent file-reading tools truncate long files silently. A sub-agent reporting on a half-read file produces findings that look complete and are not. Every spawn prompt that involves reading source material must instruct: continue reading with offsets until the entire file is loaded.

## 10. State your prior, then hunt against it

Write your hypothesis down before the gather starts, and dedicate part of the gather (one agent, or one pass) to **disconfirming** it: the skeptic slice. Grade the disconfirming evidence with the same rigor. The hypothesis is frozen for the wave; you update it between waves, in writing, not silently mid-search. This is cheap insurance against the failure mode where research becomes an elaborate confirmation of what you already believed.
