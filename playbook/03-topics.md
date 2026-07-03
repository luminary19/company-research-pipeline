# The Seven Topics

A company is too big to research as one question. The pipeline decomposes it into seven dossiers, each owning one slice, together covering everything that matters. The decomposition is MECE by design: every fact has exactly one home, and each dossier declares what it owns and what its neighbors own.

## 1. The topics, in build order

| # | Dossier | The question it answers | Analytical spine |
|---|---|---|---|
| 1 | **thesis** | Is the company's bet real? The why-now forces, the core claim, what must be true for it to work | Load-bearing assumptions table; moat premise |
| 2 | **company** | What is true about the entity? Identity, history, founders, funding, traction, ownership orbit | Ecosystem and investor-orbit map |
| 3 | **product** | What ships versus what is marketed? The product line, the buildable state, the honesty gaps | Marketed-versus-shipped x-ray |
| 4 | **buyers** | Who buys and why? ICPs, jobs-to-be-done, the customer journey, the realistic market size | Jobs-to-be-done; buyer-side TAM |
| 5 | **competitive** | Does the moat hold? The market map, per-competitor briefs, where the company is vulnerable | Moat analysis; 2x2 positioning |
| 6 | **activity** | What is the company doing right now, and what happens next? Timeline, posture, forecast | Forecast horizons (6 and 12 months) |
| 7 | **people** | Who runs it, who is being hired, and what does that signal? | Hiring-as-signal; public-professional profiles |

## 2. Why this order

- **thesis first** because it governs everything: every later dossier tests some part of the bet, and you cannot grade evidence for or against a bet you have not articulated.
- **company and product next** because they establish ground truth about the entity and the artifact before you evaluate the market around them. Product's marketed-versus-shipped reality is the honesty gate the rest of the research leans on.
- **buyers and competitive after** ground truth, because demand and moat only make sense measured against what actually exists.
- **activity late**, because a temporal read (is this launch burst a fundraise setup? is the hiring a pivot signal?) only means something against the established thesis, product, and competitive picture.
- **people last**, because hiring-as-signal and founder-trajectory reads are the most inference-heavy dossier and need every prior dossier as context. It is also the dossier with the strictest ethical boundary; see section 5.
- **synthesis after all seven**, re-deriving the answer to your Phase 0 question with all seven verified. Each dossier hands the synthesis its load-bearing tension explicitly (the open question its own evidence could not close).

Each dossier loads all previously written dossiers in full at step 1, cross-references them, and never re-derives their facts.

## 3. Ownership boundaries

Every dossier opens with an ownership header:

- **Owns (single source of truth):** the facts this file is the home for.
- **Does NOT own:** each adjacent slice, with a pointer to the owning dossier.

This does three jobs. It keeps dossiers from bloating into everything-documents. It makes conflicts findable (two dossiers claiming the same fact is a structure bug). And it forces the distribute step: because boundaries are explicit, a finding that belongs elsewhere is recognizable at the moment you find it.

Typical boundary calls, from practice:

- A competitor's funding round: owned by **competitive** (it is a fact about the rival), even though it was found while researching activity.
- The company's own funding: owned by **company**; the *timing read* of the round ("14 months post-seed, inside the usual raise cadence") is owned by **activity**.
- A founder's public claim about the product: the claim's truth is owned by **product**; the fact that the founder said it, and what that signals, is owned by **people** or **activity**.

## 4. The inbound queue

Cross-topic routing is a filesystem convention, chosen because it is append-only and safe when multiple sessions or agents write concurrently:

```
research/{company}/{topic}/inbound-queue/
├── pending/    one small file per routed finding, awaiting absorption
└── archive/    absorbed findings, moved here after integration
```

Each queue entry is one file: a headline, one or two sentences, the citation, the source session, and a topical home hint (name the topic area, never a precise section; the owning dossier decides placement). Nobody edits another session's entry; integration is a move from `pending/` to `archive/`, which doubles as the audit trail.

Two integration paths:

- **Forward**: the destination dossier is not yet written. The queue entry waits and gets absorbed at that dossier's step 1.
- **Backflow**: the destination dossier is already written. Drain at the end of the session that produced the finding: absorb surgically into the owning section, merge the reference list, assign the tag yourself, move the file to `archive/`.

Keep a one-line-per-event backflow log in the company's `00-progress.md` (date, from, affects, item, status). It is the record that saves you when you later wonder whether a correction actually landed.

## 5. The people-dossier boundary

The people dossier has a hard ethical line: **public-professional signal only**.

In scope: the public org map, hiring posture and what it signals, careers-page and job-posting analysis, public talks and posts, stated professional history (verified; see the identity-verification rule).

Out of scope: inferred private psychology presented as findings, personal-life material, anything that reads as surveillance rather than diligence. The test: if the person read this dossier, would it read as substantive professional research, or would it raise their guard? Research that fails this test is worse than useless; it poisons the relationship the research was meant to serve.
