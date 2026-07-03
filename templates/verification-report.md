# Verification Report Template

One file per verification batch, written to `research/{company}/{topic}/02-verification/verify-{batch}.md`. Verification is framed adversarially: the job is to refute the claim, and a claim that survives an honest refutation attempt earns its confidence.

---

```markdown
---
type: Verification Report
topic: {topic}
batch: {batch-name}
company: {company-slug}
date: {YYYY-MM-DD}
claims_checked: {N}
---

# Verify: {batch name}

## Verdict table

| Claim | Verdict | Confidence | Key primary source |
|---|---|---|---|
| {claim as compiled} | CONFIRMED | {NN%} | {source}, <URL> |
| {claim} | REFUTED | {NN%} | {source}, <URL> |
| {claim} | PARTIAL | {NN%} | {source}, <URL> |

## Per-claim detail

### {Claim 1}

- **Attack**: {how refutation was attempted; which primary record was checked and why it is the system of record}.
- **Found**: {what the primary record actually says, quoted or precisely paraphrased, with URL}.
- **Verdict**: {CONFIRMED / REFUTED / PARTIAL} at {NN%}. {If PARTIAL: exactly which part holds and which does not.}
- **Positive control** (required for any absence finding): {evidence the method finds known-present items}.

### {Claim 2}

{...}

## Conflicts surfaced

- {Both values, both sources, and whether a primary record resolves it. "Resolved in favor of the primary record" or "carried".}

## Corrections for the compiled gather

- {Any compiled finding this batch proved wrong, stated as old -> new, so the dossier writer applies it.}
```

---

## Rules

- Go to systems of record: regulator registers, registry JSON APIs, live docs, official rosters, direct fetches. A secondary article repeating the claim is not verification.
- Verify against running systems: capability claims are tested against what is live and shipped today, not against whitepapers.
- Time-sensitive claims get a same-day check with the fetch date recorded.
- Identity rule: any person-attributed claim requires name AND role AND company to match before it counts.
