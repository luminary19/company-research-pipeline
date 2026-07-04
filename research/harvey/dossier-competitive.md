---
type: Dossier
subject: competitive
company: harvey
created: 2026-07-04
updated: 2026-07-04
version: 1.0
status: draft
primary_source: https://legalrealist.ai/posts/26-harvey-v-legora/
description: 'Owns the competitive landscape and whether Harvey''s moat holds. Headline: (1) Three fronts — incumbents that own the case-law corpora Harvey lacks (Thomson Reuters CoCounsel 1M users, LexisNexis Protégé, Clio/vLex $1B), AI-native rivals led by Legora (~$5.6B, the consensus co-leader), and the existential front: the foundation labs Harvey rents from are entering legal directly [F/88%]. (2) Anthropic made Harvey a swappable connector inside Claude and OpenAI is building a legal vertical (hiring Ironclad''s founder), and Weinberg himself concedes "our main competitor is the labs" [F/85%]. (3) The honest moat read: Harvey''s durable strengths are its 2/3-AmLaw-100 install base, forward-deployed-engineer distribution, and proprietary lawyer-graded eval data — but the model layer is already commoditized, integration switching costs are contested, and the labs can commoditize the onboarding Harvey charges for. The load-bearing tension: Harvey''s moat is a distribution/data/services moat, not a technology moat, and it must compound faster than the labs absorb the application layer.'
---

# Dossier, Competitive

## Owns (single source of truth)

This dossier owns **the market map, the per-competitor briefs, the moat analysis, and where Harvey is vulnerable**. It is the home for facts about rivals (their funding, products, positioning) and for the adversarial "does the moat hold" question at the market level.

**Does NOT own:** whether the underlying bet is sound (dossier-thesis owns the moat *premise*; this dossier tests it against what rivals actually ship); Harvey's own product internals (dossier-product); who buys and multi-vendor behavior's demand mechanics (dossier-buyers — this dossier owns the *competitive* reading of that behavior); the entity/funding of Harvey itself (dossier-company); the timeline (dossier-activity); the org (dossier-people). A rival's funding round is owned here (it is a fact about the rival); Harvey's own funding is dossier-company's.

## How to read the tags

`[X/NN%]`: **F** fact (primary-checked), **I** inference, **A** assumption. Vendor pages are R1 for "what they market," weak for competitive claims. No vendor publishes rate cards, so pricing/verdicts are R3 estimates (surfaced as ranges). Conflicts surfaced inline. Every fact resolves to the Reference List.

---

## 1. The market map — three fronts

> Purpose: the structure of the competition Harvey faces.

Harvey competes on **three simultaneous fronts**, each with a different logic:

1. **Incumbents (database-grounded).** Thomson Reuters (CoCounsel/Westlaw), LexisNexis (Lexis+/Protégé), Bloomberg Law, Clio/vLex. They **own the licensed case-law corpora** that citation-grounded research requires — the one thing Harvey does not have [F/88%].
2. **AI-native rivals.** Legora (co-leader), Spellbook, Robin AI, Luminance, Ironclad, EvenUp/Eve, GC AI, Kira. Same architectural bet as Harvey; the top is a **Harvey–Legora duopoly** [F/82%].
3. **Horizontal foundation labs (the existential front).** Anthropic, OpenAI, Google — Harvey's *suppliers* now entering legal *directly* [F/85%]. This is the front Weinberg himself calls the main one.

## 2. Incumbents (they own the corpus)

> Purpose: the database-grounded rivals and the corpus gap.

- **Thomson Reuters CoCounsel** (ex-Casetext, acq. $650M 2023): hit **1M users across 107 countries (Feb 2026)**; being rebuilt on **Anthropic's Claude Agent SDK** (early access Jun 2026, GA Aug 2026); Westlaw-grounded with KeyCite citation verification; ~$225/seat/mo Core [F/85%]. Strength vs Harvey: authoritative research + citation grounding. Weakness: less flexible custom-agent building.
- **LexisNexis Lexis+ / Protégé**: **GA Feb 2026**, 300+ workflows, Shepard's + "Verify Trust Markers," multi-model (Anthropic/Google/OpenAI), May 2026 added agentic Protégé Work + BYOK + 100K-doc Vault; ~$275/seat [F/85%]. **The dual dynamic**: powers Harvey's "Ask LexisNexis" via API *and* competes via Protégé, while parent RELX's REV invested in Harvey's Series D+E — "integration without access" (Harvey gets "<1% of the repository") [F/88%] (Artificial Lawyer; thesis §6.4).
- **Westlaw Precision** (TR) & **Bloomberg Law AI**: Bloomberg's AI Assistant is **free with subscription (~$200–400/seat) — the cheapest incumbent**, "competent but less mature" [F/78%].
- **Clio / vLex**: **Clio acquired vLex/Fastcase for $1B (closed Nov 2025 — largest legal-tech M&A ever)** + $500M Series G at $5B; Vincent AI runs on 1B+ enriched docs, 110 jurisdictions [F/85%].
- **The corpus gap (central).** Harvey **has no native research database**; it reportedly tried to buy vLex first (~$600M, 2024) but **lost to Clio**, then pivoted to renting LexisNexis content [F/80%] (TechCrunch). Every comparison agrees "Harvey lags on pure research." This is Harvey's clearest structural product deficit vs incumbents.

## 3. AI-native rivals (the duopoly and the field)

> Purpose: the same-architecture competitors.

- **Legora** (the consensus co-leader): **~$5.6B (Apr 2026)** after a $50M Atlassian/Nvidia extension (Nvidia's first legal-AI bet), up from $1.8B (Series C, Oct 2025, Bessemer); **$100M+ ARR** ("fastest ever to $100M," Bessemer); 1,000+ orgs, 50+ markets; **Claude-based → model-agnostic aOS** on Azure. Matches Harvey's celebrity marketing (Jude Law, Aaron Judge/Yankees vs Harvey's Gabriel Macht) [F/82%]. **The market is a Harvey–Legora duopoly at the top**, split by axis (below).
- **Spellbook**: $50M Series B at **$350M** (Khosla, Oct 2025); Word add-in, mid-market, 4,000–4,500 teams; GPT-5 + Opus [F/82%].
- **Robin AI** (the cautionary tale): failed $50M raise → ~50 layoffs → insolvency → rescued at £163m (Mar 2026); "scaled too quickly to compete with Harvey and Legora" [F/80%]. A signal that the middle is being squeezed.
- **Luminance / Ironclad** (contract intelligence / CLM): valuations widely cited as ~$1.5B / ~$3.2B are **uncorroborated/stale** — Luminance's disclosed round is a $75M Series C (Point72, no valuation); Ironclad's $3.2B is a 2022 figure [CONFLICT, carried].
- **Plaintiff side**: **EvenUp** $150M Series E at **$2B+** (Oct 2025; REV on cap table), **Eve.legal** $103M at $1B+ — a segment Harvey does not serve [F/80%].
- **GC AI** (in-house): rare public pricing **$500/seat**, ~$73M raised, revenue $1M→$10M in a year [F/78%].
- **Kira Systems** (doc/contract review): appears in buyer stacks ("Harvey for thinking, Kira for reviewing"); a point-solution rival [F/70%].

## 4. The horizontal labs — the existential front

> Purpose: the front Weinberg calls the main one.

**4.1 Anthropic is furthest in.** May 12–13, 2026: "Claude for the Legal Industry" — **20+ MCP connectors + 12 practice-area plugins, with Harvey itself as a connector inside Claude** (the hub→spoke inversion; thesis §6.3) [F/88%] (LawNext). The Feb 2026 legal-plugin release preceded a **~$285B single-session market-cap wipeout** of legal/software/analytics names (TR reportedly -18%, RELX -17%) — magnitude/date attribution is contested (R3·C1), carried [F/70%]. The plugins ship a **free "setup interview" that learns firm playbooks** — the same onboarding Harvey/Legora charge five- and six-figure contracts to provide.

**4.2 OpenAI is building a legal vertical directly.** Planned "Codex for Legal" + a forward-deployed "Deployment Company," signalled by **hiring Ironclad founder Jason Boehmig to lead product for legal** [F/82%] (Artificial Lawyer). Read as the most direct shot at Harvey's fine-tuning + FDE moat — OpenAI can copy the FDE motion.

**4.3 Harvey's own concession.** Weinberg: **"I think our main competitor is the labs… Every single company on Earth is competing against them"** [F/88% first-party] (Sourcery). OpenAI's rumored legal release "confirmed his thesis." That the CEO names the labs as the primary competitor is the single most important competitive fact in this dossier.

## 5. Moat analysis (analytical spine)

> Purpose: the honest strength/vulnerability decomposition.

**Strengths that hold (S1–S6):**

| # | Strength | Durability |
|---|---|---|
| S1 | **~2/3 AmLaw-100 install base** + brand (the default legal-AI name) | Strong — but a *retention* moat, not a growth moat [I/70%] |
| S2 | **Forward-deployed legal engineers** (services-heavy deployment) | Real — but now directly attacked by OpenAI's FDE "Deployment Company" [I/60%] |
| S3 | **Proprietary lawyer-graded eval data** (BigLaw Bench/LAB, Applied Legal Researchers, synthetic-data flywheel) | The most defensible — expensive to reproduce; partly open-sourced [I/72%] |
| S4 | **Enterprise security / ethical-wall certification** (SOC2/ISO, tenant isolation) | A barrier vs consumer tools; not vs Lexis/TR/Anthropic [I/65%] |
| S5 | **Multi-model runtime** (own agent infra, routing, 3–5× cost) | Real engineering; replicable by well-funded rivals [I/60%] |
| S6 | **Distribution + relationships** (Lighthouse co-dev, Transformation Office) | Strong but relationship-based, not structural [I/62%] |

**Vulnerabilities (V1–V6):**

| # | Vulnerability | Severity |
|---|---|---|
| V1 | **Model-layer commoditization** — Harvey's own model lost to 7 frontier models on its own bench; "the AI is rented, not owned" | High [F/85%] |
| V2 | **No native case-law corpus** — structural research deficit vs Westlaw/Lexis/vLex | High [F/85%] |
| V3 | **Thin-by-design integration → contested switching cost** — "one product cycle away from irrelevance"; lock-in is a retention, not growth, moat | High [I/65%] |
| V4 | **Premium price ceiling** — ~$1,000–1,500/seat (50–100× API markup) vs cheaper bundled incumbents and free lab plugins | Medium-High [F/78%] |
| V5 | **Labs commoditize onboarding** — Anthropic's free "setup interview" ships what Harvey charges for | Medium-High [F/75%] |
| V6 | **Open-source substitution** — "MikeOSS" runs a 40-attorney firm at 2–4% of Harvey's price (3,300+ GitHub stars) | Low-Medium [I/50%] |

**The verdict:** Harvey's moat is a **distribution + proprietary-data + services moat, not a technology moat** [I/72%]. The technology (runtime, RAG, evals) is real and hard (dossier-product) but replicable; the durable edge is the AmLaw-100 relationships and the lawyer-graded eval/data flywheel. Whether that compounds faster than the labs absorb the application layer is the open question.

## 6. Positioning — the 2×2 and the "$17B question"

> Purpose: where Harvey sits and what the market is betting.

- **Vertical-split 2×2** (analyst consensus): **Harvey = complex-reasoning / US BigLaw**; **Legora = high-throughput / international**; incumbents = research-grounded; point solutions (Spellbook/EvenUp/GC AI) own niches [I/70%].
- **The dominant frame is "foundation absorbing the platform" / the "$17B question"**: Harvey's ~57× and Legora's ~56× ARR multiples *require the application layer to stay independent of the labs* [I/68%] (LegalRealist). If the labs commoditize the layer, the multiples compress hard (thesis §6.6).
- **The live buy-vs-build fork**: **Freshfields "chose neither"** — an Anthropic co-build + Gemini firmwide — the real-world instantiation of firms deciding they don't need Harvey *or* Legora [F/72%] (Point Blank). This is the scenario that most threatens the whole AI-native category.

## Open Questions / Decisions Pending

- **Will the labs win the vertical?** OpenAI's legal-vertical + Boehmig hire and Anthropic's connectors are the decisive variable. Weinberg's own answer: differentiate on security/governance/collaboration/memory/integrations (thesis §3.4) — i.e., the things a general runtime won't build for legal.
- **CONFLICT carried:** switching cost — one-year deals (fragile) vs contracts lengthening (sticky) — decides whether S1/S6 are real moats.
- **CONFLICT carried:** Luminance (~$1.5B?) and Ironclad (~$3.2B?) valuations are uncorroborated/stale.
- **Unknowable from outside:** true churn/NRR; whether the AmLaw-100 install base defends against a free/cheaper lab plugin.
- **Load-bearing tension handed to synthesis:** Harvey leads a category that the foundation labs are now entering directly, on a moat that is distribution+data+services rather than technology. For an engineering candidate: this is the single most important thing to understand — the interesting question isn't "is the tech good" (it is) but "does Harvey's data/distribution/eval flywheel outrun the labs," and you should have a view.
- **Routed this session:** thesis (backflow — the labs-as-main-competitor concession + Anthropic hub→spoke reinforce §6.2–6.3; already reflected); activity (Anthropic May 2026 launch, OpenAI Boehmig hire Jun 2026, the Feb-2026 market-cap event — timeline); people (OpenAI hiring Ironclad's Boehmig = talent-war signal; Legora as the org Harvey competes with for hires); product (CoCounsel on Claude Agent SDK — same-family tech; Protégé 100K-doc Vault as a feature comparison).

## Key Terms

| Term | Plain meaning |
|---|---|
| Corpus | The licensed body of case law / statutes a research tool cites from (Westlaw/Lexis own these) |
| MCP connector | A plug that lets an LLM (Claude) call an external tool/data source — here, Harvey-as-a-connector |
| Hub → spoke | The inversion where Harvey (once the platform) becomes one swappable option inside Claude |
| FDE moat | Defensibility from embedding engineers in customers — replicable if a rival builds the same team |
| ARR multiple | Valuation ÷ annual recurring revenue; ~57× here prices in near-perfection |
| Retention vs growth moat | A moat that keeps existing customers (data gravity) vs one that wins new ones |
| Duopoly | A market led by two players — here Harvey (US/complex) and Legora (international/throughput) |

## Reference List

- Anthropic / LawNext 2026, *Anthropic Goes All-In on Legal: 20+ Connectors and 12 Plugins for Claude*, 12 May 2026, <https://www.lawnext.com/2026/05/anthropic-goes-all-in-on-legal-releasing-more-than-20-connectors-and-12-practice-area-plugins-for-claude.html>.
- Artificial Lawyer 2025, *LexisNexis Explains Why REV Invested in Rival Harvey*, 13 Feb 2025, <https://www.artificiallawyer.com/2025/02/13/lexisnexis-explains-why-rev-invested-in-rival-harvey/>.
- Artificial Lawyer 2026, *Ironclad Founder Jason Boehmig Joins OpenAI for Legal Vertical Launch*, 1 Jun 2026, <https://www.artificiallawyer.com/2026/06/01/ironclad-founder-jason-boehmig-joins-openai-for-legal-vertical-launch/>.
- LawNext 2026, *CoCounsel Reaches 1 Million Users…*, 24 Feb 2026, <https://www.lawnext.com/2026/02/three-years-after-launching-as-first-ai-legal-assistant-cocounsel-reaches-1-million-users-and-thomson-reuters-teases-whats-ahead.html>.
- Law.com 2026, *LexisNexis Announces GA of Lexis with Protégé*, 24 Feb 2026, <https://www.law.com/legaltechnews/2026/02/24/lexisnexis-announces-general-availability-of-ai-workflow-platform-lexis-with-protg/>.
- LawNext 2025, *Clio Completes Historic $1 Billion vLex Acquisition, $500M Series G*, 10 Nov 2025, <https://www.lawnext.com/2025/11/clio-completes-historic-1-billion-vlex-acquisition-announces-500-million-series-g-at-5-billion-valuation-plus-exclusive-interview-with-ceo-and-cfo.html>.
- LegalRealist AI 2026, *The $17 Billion Question* (Harvey v Legora; moat, 2×2), <https://legalrealist.ai/posts/26-harvey-v-legora/>.
- marketledgrowth 2026, *The 58x Delusion* (thin-integration/switching-cost), <https://marketledgrowth.substack.com/p/the-58x-delusion-the-case-against>.
- Point Blank 2026, *Everyone Picked Harvey or Legora — Freshfields Chose Neither*, <https://www.pointblank.law/p/everyone-picked-harvey-or-legora-freshfields-chose-neither>.
- Sourcery 2026, *Breaking: $11B Harvey Hits $300M ARR* (Weinberg "main competitor is the labs"), <https://www.sourcery.vc/p/breaking-11b-harvey-hits-300m-arr>.
- TechCrunch 2026, *Legal AI Startup Legora Hits $5.6B Valuation*, 30 Apr 2026, <https://techcrunch.com/2026/04/30/legal-ai-startup-legora-hits-5-6-valuation-and-its-battle-with-harvey-just-got-hotter/>.
- TechCrunch 2025, *Clio Drops $1B on Law Data Giant vLex* (Harvey's lost vLex bid), 30 Jun 2025, <https://techcrunch.com/2025/06/30/legal-software-company-clio-drops-1b-on-law-data-giant-vlex/>.
- Vaquill 2026, *Harvey / Legora / CoCounsel Pricing Reality 2026*, <https://www.vaquill.ai/blog/harvey-legora-cocounsel-pricing-reality-2026>.
- Zevra 2026, *Claude Legal guide* (~$285B market-cap event), <https://zevra.tech/en/guide/guide-claude-legal>.
