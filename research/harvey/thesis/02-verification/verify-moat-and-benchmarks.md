---
type: Verification Report
topic: thesis
batch: moat-and-benchmarks
company: harvey
date: 2026-07-04
claims_checked: 5
---

# Verify: moat premise + benchmark reality (thesis)

Adversarial re-check of the load-bearing thesis claims that were single-source, contested, or time-sensitive, against the running systems (Harvey's live benchmark pages + primary/secondary coverage of the Anthropic-connector development). Fetched 2026-07-04.

## Verdict table

| Claim | Verdict | Confidence | Key primary source |
|---|---|---|---|
| Frontier models complete <10% of long-horizon legal tasks end-to-end (LAB all-pass); Opus 4.7 tops at 7.1% | CONFIRMED | 96% | harvey.ai/blog/legal-agent-benchmark-initial-results |
| Top LAB config costs ~$50.90/task and ~22 min latency (Opus 4.7) | CONFIRMED | 95% | (same) |
| Post-trained GLM-5.1 lifts rubric pass 0.853→0.913, beating GPT-5.5 xhigh & Opus 4.8 Max; 2nd on all-pass | CONFIRMED | 94% | harvey.ai/blog/training-a-legal-agent-with-applied-compute |
| Harvey's 2024 proprietary model was beaten by ≥7 frontier models on its own BigLaw Bench → went multi-model ("renting > owning") | CONFIRMED (as Harvey's own admission, via secondary) | 85% | Harvey "Expanding Harvey's Model Offerings" (via legalrealist.ai) |
| Anthropic (May 2026) made Harvey a swappable MCP connector inside Claude ("hub → spoke") | CONFIRMED (event); interpretation CONTESTED | 88% event / — interp | legaltechnology.com (Legal IT Insider); legalrealist.ai |

## Per-claim detail

### 1–2. LAB initial results (all-pass, cost, latency)
- **Attack**: verify Harvey's own headline "not yet good enough" figures are stated as claimed and not softened/rounded in the recap; benchmark pages are the system of record for the vendor's own numbers.
- **Found** (verbatim, live page): "the frontier models we evaluated complete less than 10% of tasks end-to-end in aggregate… Claude Opus 4.7 leads at 7.1%, with Sonnet 4.6 at 5.4%, Opus 4.6 at 4.2%, GPT-5.5 at 2.1%, and Gemini 3.5 Flash at 0.8%… a frontier that is improving rapidly but is not yet good enough. Legal work is far from saturated." Cost/latency: "about $50.90 per task and roughly 22 minutes of wall-clock time. GPT-5.5 is approximately 3x cheaper."
- **Verdict**: CONFIRMED at 95–96%. Caveat: this is Harvey grading models on Harvey-authored tasks/rubrics — R1 for "what Harvey's benchmark reports," not an independent measure of Harvey-the-product.

### 3. GLM-5.1 post-train result
- **Attack**: confirm the improvement numbers and that the model genuinely surpasses the named frontier models on rubric pass, on Harvey's live page (not just the vendor's).
- **Found** (verbatim, harvey.ai): "Post-training over GLM-5.1 increases rubric pass rate to 0.913, exceeding both GPT-5.5 xhigh and Opus 4.8 Max… Before training, GLM-5.1 was below GPT-5.5 xhigh and Opus 4.8 Max. During training, it passed both on rubric pass rate… making it the strongest available model by rubric pass rate and second only to Opus 4.8 Max on all-pass rate." Base "near 85% pass rate" (=0.853). Method: "full-parameter, fully asynchronous reinforcement learning on AC2." Caveat surfaced on same page: "Roughly 10% of base GLM-5.1 rollouts hit the context limit"; residual failure on quantitative tasks ("poor calculations… imprecise numbers").
- **Verdict**: CONFIRMED at 94%. Note: rubric-pass (dense) ≠ all-pass (strict); the model is strongest on rubric pass, only 2nd on all-pass — do not conflate.

### 4. Harvey scrapped its 2024 proprietary model after frontier models beat it on BigLaw Bench
- **Attack**: is the "own model failed" story real or a skeptic's spin? Trace to Harvey's own statement.
- **Found**: legalrealist.ai reports (and cites Harvey's own "Expanding Harvey's Model Offerings" post): "Harvey built a custom LLM, tested it against frontier models on its own benchmark, and the frontier models won… seven models — from Google, OpenAI, Anthropic, and xAI — now outperform the original Harvey system on Harvey's own benchmark. Harvey went multi-model." This RESOLVES the apparent contradiction with the June-2026 "legal foundation model series": the 2024 custom case-law model (v1) was superseded; the 2026 post-trained open-weight GLM-5.1 series (v2) is a different, cheaper approach. **Not a contradiction — a documented model-layer pivot (own → rent → own-v2-cheaply).**
- **Verdict**: CONFIRMED at 85% (Harvey-primary claimed via a reliable secondary; the primary "Expanding Model Offerings" post exists but was read here through legalrealist's citation — lift to 90%+ if fetched directly in a later pass).

### 5. Anthropic made Harvey a swappable connector inside Claude ("hub → spoke")
- **Attack**: did this event happen, and is "commoditization" the only reading? Check both a neutral trade source and the skeptic.
- **Found**: Legal IT Insider (R2) confirms the MCP program and quotes Harvey's own framing — the connector is "another access point to Harvey," "a Claude user can invoke Harvey's legal workflows from inside Claude." LegalRealist (R3): "Anthropic just launched 20+ connectors — including Harvey itself — and 12 practice-area plugins… The platform that sold itself as the hub is now a spoke in Claude's hub. A firm using Harvey through Claude's connector can swap Harvey for a different connector… without changing anything else." Also: when Anthropic launched a legal Cowork plugin (Feb 2026), "$285 billion [was] erased from legal tech stocks in five trading days" before recovering.
- **Verdict**: event CONFIRMED at 88%. **Interpretation CONTESTED and CARRIED**: Harvey = "more distribution"; skeptics = "commoditization / loss of hub position." Surfaced, not resolved.

## Conflicts surfaced
- **Own-model narrative**: "building a legal foundation model series" (Law.com, Jun 2026) vs "scrapped its proprietary model / renting beats owning" (Harvey via legalrealist) — RESOLVED as a v1→v2 evolution (own case-law model 2024 → multi-model → post-trained open-weights 2026). Carried into the dossier as an explicit narrative, not a live conflict.
- **Anthropic-connector meaning**: distribution boon vs commoditization threat — CARRIED (interpretive, unresolvable from outside).
- **Metric conflation risk**: SPA-workflow answer accuracy 98.47% vs LAB all-pass 7.1% vs rubric pass 91.3% — three different metrics; not a contradiction. Flagged so the dossier never presents them as competing versions of one number.

## Corrections for the compiled gather
- The recon shorthand "BigLaw Bench 60%→90%" is NOT a clean Harvey-published series; do not quote it as one. Use the actual published numbers (BLB 74% work-product 2024; SPA 98.47% answer accuracy; LAB all-pass single-digit; GLM rubric 85→91.3). → applied at write time.
- "0.2% hallucination rate" is R3-only (third-party deep-dives), not a Harvey primary → treat as an unverified vendor-adjacent claim, not a fact.
