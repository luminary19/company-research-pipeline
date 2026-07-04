---
type: Verification Report
topic: company
batch: identity-funding-governance
company: harvey
date: 2026-07-04
claims_checked: 6
---

# Verify: identity, funding, governance (company)

Adversarial re-check against SEC EDGAR (the primary system of record for a US company's securities offerings) and Harvey's own round announcements. Fetched 2026-07-04 with a proper User-Agent.

## Verdict table

| Claim | Verdict | Confidence | Key primary source |
|---|---|---|---|
| Legal entity = "Harvey AI Corp", formerly "Counsel AI Corp"; Delaware; HQ 201 Third St Suite 500, SF | CONFIRMED | 98% | SEC EDGAR submissions JSON (CIK 0001974654) |
| Incorporated 2022 (year only; exact day not public) | CONFIRMED | 95% | SEC Form D (yearOfInc 2022) |
| Board of directors = Weinberg, Pereyra, Pat Grady (Sequoia), Ilya Fushman (KP), John LaBarre | CONFIRMED | 94% | SEC Form D 2026-04-06, related persons |
| The Mar-2026 round sold ~$200M | CONFIRMED | 96% | Form D 2026-04-06: totalAmountSold = $200,009,773 |
| Full funding ladder Seed→$11B (rounds/dates/leads) | CONFIRMED (per-round) | 90% | Harvey /blog announcements (7 of 9 rounds) |
| Total raised (single figure) | REFUTED as a single number — CONFLICT stands | — | Multiple aggregators disagree ($988M–$1.3B) |

## Per-claim detail

### Identity / incorporation
- **Attack**: is "Counsel AI → Harvey" real, and is the entity actually Delaware/SF? Check the registrant record, not press.
- **Found** (SEC EDGAR, live): `name: "Harvey AI Corp"`, `formerNames: ["Counsel AI Corp"]`, `stateOfIncorporation: DE`, business address `201 THIRD STREET, SUITE 500, SAN FRANCISCO, CA 94103`. Form D `yearOfInc: 2022`. Two USPTO "HARVEY" marks (serials 97690544 class 042 SaaS; 97690542 legal info services) owned by "Counsel AI Corporation," filed 2022-11-23.
- **Verdict**: CONFIRMED 98%. Residual gap: exact incorporation day/month and the Delaware/CA entity file numbers (state registers were bot-blocked; SEC data supersedes for identity).

### Governance / board (control structure)
- **Attack**: who actually controls the company? Verify board via the filing's related-persons, not a secondary liquidity site.
- **Found** (Form D 2026-04-06 related persons): **Directors** — Winston Weinberg (also Exec Officer), Gabriel Pereyra (also Exec Officer), **Pat Grady** (Sequoia), **Ilya Fushman** (Kleiner Perkins), **John LaBarre** (also Exec Officer). **Exec officers (non-director)** — **Alan Ghelberg** (CFO per secondary), **Katie Burke**. Ten investors in the offering.
- **Verdict**: CONFIRMED 94%. Founders + two lead-investor directors (Sequoia, KP) + LaBarre = a founder-controlled board with the two earliest institutional leads seated. No independent/outside chair disclosed. Note: the two co-founders hold both officer and director roles → concentrated founder control.

### Funding ladder + total
- **Attack**: are round figures Harvey-primary, and is any single "total raised" defensible?
- **Found**: 7 of 9 rounds trace to Harvey's own /blog posts; the Mar-2026 round's ~$200M is confirmed by the Form D dollar figure ($200,009,773). Total-raised figures diverge irreconcilably: $806M (websets, stale), $987.9M (MVP), "over $1B"/"$1.2B+" (Harvey/CNBC/Sequoia + Dealroom), $1.19B (PitchBook), $1.22B (Tracxn; = mechanical sum of headline amounts), $1.3B (StartupIntros).
- **Verdict**: rounds CONFIRMED; single total REFUTED — carry the conflict. Best defensible statement: **"over $1.2B across ~9 rounds"** (matches the mechanical sum of announced headline amounts and Harvey's own "more than $1B" as of Mar 2026).

## Conflicts surfaced (carried)
- **Total raised**: $988M–$1.3B across sources — carried; "over $1.2B" is the most defensible.
- **Series E valuation**: Harvey $5B (primary) vs Manhattan Venture Partners "$9.2–9.3B pre/post" — the MVP figure is anomalous and contradicts Harvey's own post; treated as likely MVP data error, carried not resolved.
- **Series A amount**: $21M headline (Harvey/Sequoia) vs ~$25.8–25.9M (Form D / PitchBook) — carried.
- **Headcount (2026)**: ~350–400 editorial vs 1,100–1,441 scrapers — carried; editorial (interview-sourced) is more credible, scrapers likely over-count.
- **ARR**: all figures Harvey-self-reported/unaudited; "$300M ARR (Jun 2026)" is uncorroborated aggregator framing — treat as unverified.

## Corrections for the compiled gather
- Upgrade board/officers from R3/R4 (Collective Liquidity) to **R1 (SEC Form D)**: directors = Weinberg, Pereyra, Grady, Fushman, LaBarre.
- Confirm the $200M Growth round from the primary filing (not just press).
