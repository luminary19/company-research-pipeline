---
type: Verification Report
topic: product
batch: shipped-state-and-metrics
company: harvey
date: 2026-07-04
claims_checked: 6
---

# Verify: shipped state + metric reconciliation (product)

Most product-architecture claims are already primary (Harvey eng blog / careers / developer docs = R1 for Harvey's own architecture; GitHub API = R1 primary for the public code). This note resolves the load-bearing shipped-vs-marketed and metric questions.

## Verdict table

| Claim | Verdict | Confidence | Basis |
|---|---|---|---|
| Product code is a private monorepo; only benchmarks + forks are public | CONFIRMED | 95% | GitHub API — only harvey-labs actively pushed; no public SDK on npm/PyPI (positive control passed) |
| "Agents execute legal work end-to-end" is qualified by mandatory human-in-the-loop | CONFIRMED | 92% | Harvey's own /agents ("Own the Judgment. You make the call") + every independent review |
| Contract Intelligence, Command Center, Shared Spaces, Connector Library = Early Access/waitlist, not GA | CONFIRMED | 90% | Harvey's own announcement blogs (each says EA/waitlist) |
| Memory is pre-product (co-build, future tense) | CONFIRMED | 90% | harvey.ai/blog/memory-in-harvey (all conditional) |
| Post-trained GLM-5.1 is a benchmark result, NOT a confirmed production model | CONFIRMED (as research) | 85% | Applied Compute post frames prod as forward-looking |
| Tech stack (Python/Go/React-TS-Tailwind; Azure+GCP; K8s; LanceDB; voyage-law-2-harvey; OpenAI Agents SDK) | CONFIRMED | 90% | Harvey eng blog + 5+ job posts (verbatim) |

## Per-claim detail

### Private-monorepo / no public SDK
- **Found**: `github.com/harveyai` has 7 public repos; only `harvey-labs` (LAB) is actively committed (pushed 2026-07-01). No official Harvey client on npm or PyPI (positive control: openai/anthropic/langchain all resolve; Harvey-named packages 404). A developer API *does* exist (developers.harvey.ai — Vault/Assistant guides, `ready_to_query`, 10 req/min) but no published SDK library.
- **Verdict**: CONFIRMED 95%. The engineering surface proves an active research/eval team and an open benchmark; it proves nothing about the private product's scale.

### "End-to-end" vs human-in-the-loop
- **Attack**: does Harvey's "agents execute end-to-end" marketing survive its own product copy and independent use?
- **Found**: Harvey's /agents page itself: "Delegate the Work. **Own the Judgment**… You make the call"; Agent Builder ships "human-in-the-loop checkpoints as a core feature." Latham did NOT deploy Harvey for advocacy/oral-argument/novel strategy. ABA Opinion 512 requires lawyer supervision. Every independent review: "first-pass accelerator, not a verification tool."
- **Verdict**: CONFIRMED 92%. Shipped reality = review-ready first drafts on high-volume, pattern-matchable work; humans retain judgment/novel-issue/advocacy. Links to thesis §6.1 (LAB <10% all-pass).

### Early-Access surfaces
- **Found** (Harvey's own blogs): Contract Intelligence = design-partner waitlist (only testimonial is Harvey's own GC, John LaBarre); Command Center = "Early Access… join the waitlist"; Shared Spaces = "live in early access… GA expected March"; Connector Library = "mid-June Early Access for select customers." Memory = co-build/listening-tours, entirely future tense.
- **Verdict**: CONFIRMED 90%. Several 2026 marketed surfaces are not yet GA — a real marketed-vs-shipped gap.

### GLM-5.1 production status
- **Found**: the Applied Compute post reports a benchmark result ("strongest available model on LAB by rubric pass rate") and frames deployment forward-looking ("as these systems move from benchmarks into production"). ~10% of base GLM-5.1 rollouts hit context limit; weak on quantitative tasks.
- **Verdict**: CONFIRMED as a research result at 85%. Do NOT present GLM-5.1 as Harvey's shipped default model; it is a proof-of-concept for the own-model-v2 bet (thesis §5.2).

## Conflicts surfaced (carried)
- **Harvey's own pages disagree on metrics** (different dates/definitions, all R1): daily agent activity "700k+ tasks" (/agents) vs "400K+ agentic queries/day" (Agent Builder blog); "50M terms/week" vs "20M+ terms in review tables"; users "142,000" (platform) vs "100,000" (Mar-2026 blog); knowledge sources "100+" vs "500+" vs "over 100 incl. Wolters Kluwer." Carried — treat all as company-reported, directionally large.
- **Vault "100k docs"**: not found on any Harvey page (they say "tens of thousands"); eesel notes an unspecified per-Vault cap. The "100k" recon figure is dropped as unverified.
- **Pricing outlier**: AI Vortex's "$75–200/user/mo" is ~10× below the convergent ~$1,000–1,200/seat/mo estimate — flagged and excluded.

## Corrections for the compiled gather
- Drop "up to 100k docs" for Vault; use "tens of thousands" (Harvey) with a noted unspecified cap.
- Label GLM-5.1 a benchmark/research result, not the shipped production model.
- Present agent throughput and "3–5× cost reduction" as Harvey-self-reported (C3).
