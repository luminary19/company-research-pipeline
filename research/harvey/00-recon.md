---
type: Recon
company: harvey
created: 2026-07-04
status: PROVISIONAL — every claim here is an unverified baseline to be tested in the topic dossiers
---

# Recon: Harvey (harvey.ai)

> **Provisional.** This is a surface map from a first Exa + GitHub pass, not verified truth. Grades and final tags are assigned later. The whole point of the topic dossiers is that this first pass is partly wrong.

## What Harvey appears to be

Harvey is a **domain-specific generative-AI platform for legal and professional-services work** — sold top-down to elite law firms and enterprise/in-house legal teams. Legal entity: **Counsel AI Corporation**. Founded **summer 2022** in San Francisco. It builds a product layer (retrieval, agents, workflows, evals, domain-tuned models) on top of frontier foundation models (originally OpenAI; now multi-model incl. Anthropic Claude/Fable and Google Gemini), and is now moving to build its own **legal foundation-model series** and open-source benchmarks.

Positioning has evolved: "AI assistant for a solo lawyer" (2022–23) → "enterprise platform / system for a firm" (2024–25) → "**AI operating system for legal**, agentic + memory" (2026). Founders talk about extending the playbook to tax, finance, compliance, procurement, accounting.

## People (provisional)

- **Winston Weinberg** — co-founder & CEO. Former first-year litigation associate at O'Melveny & Myers (landlord-tenant / securities litigation). Non-technical founder, domain-proximate. Now a paper billionaire (NYT "AI billionaires" feature). Known quote/philosophy: employees must "re-earn" their role every ~6 months.
- **Gabriel (Gabe) Pereyra** — co-founder & President. Former research scientist at Google DeepMind / Google Brain, then ML engineer at Meta AI. USC CS. The technical founder; drives the model/research direction.
- **Harvey Labs** (research team) — run by **Niko Grupen** (former Google Brain researcher) and **Julio Pereyra** (former O'Melveny associate; likely related to Gabe — verify). Building the legal foundation-model series + LAB benchmark.
- **John Haddock** — Chief Business Officer (per StartupIntros).
- Team: >20% of staff are lawyers ("Applied Legal Researchers" embed with engineers). Headcount grew fast: ~82 (early 2025 per one source) / ~100 (2023 OpenAI post) / ~350 (StartupIntros, mid-2025) — **CONFLICT, carry**. Likely 500–1000+ by mid-2026 given raise pace.

## Funding ladder (provisional — several total-funding conflicts)

| Announced | Round | Raised | Valuation | Lead(s) |
|---|---|---|---|---|
| Nov 2022 | Seed | $5M | — | OpenAI Startup Fund (first institutional investor), Elad Gil |
| Apr 2023 | Series A | $21M | ~$150M | Sequoia |
| Dec 2023 | Series B | $80M | $715M | Elad Gil + Kleiner Perkins (OpenAI SF, Sequoia) |
| Jul 2024 | Series C | $100M | $1.5B | GV (Google Ventures), Kleiner Perkins, SV Angel |
| Feb 2025 | Series D | $300M | $3B | Sequoia (Coatue, GV, OpenAI SF, **LexisNexis/REV**) |
| Jun 2025 | Series E | $300M | $5B | Kleiner Perkins + Coatue (DST, GV, Conviction, REV) |
| ~Oct 2025 | Growth | €50M | — | EQT Growth (secondary source; verify) |
| Dec 2025 | Series F | $160M | $8B | Andreessen Horowitz (a16z) |
| Mar 2026 | Growth | $200M | $11B | GIC (Singapore) + Sequoia |

Total raised: **>$1.2B** (sources vary: $987.9M mid-2025 [MVP], $1.2B [SVIC/CNBC], $1.3B [StartupIntros] — **CONFLICT, carry**). Sequoia has led **three** rounds ("ultimate sign of conviction," Pat Grady). Note the striking cadence: **four rounds in ~12 months** across 2025→early 2026.

## Traction (provisional, company-reported — treat as claimed, not audited)

- **ARR**: ~$100M (Sept/Oct 2025) → **$190M (Jan 2026)** — roughly doubled in ~4 months.
- **Customers**: 1,300+ organizations across ~60 countries; a **majority of the AmLaw 100** (one source: 50 of top 100; another: 42% of AmLaw 100 — **CONFLICT, carry**).
- **Users**: 74,000+ lawyers (Nov 2025) / 100,000+ legal professionals (2026).
- **Agents**: 25,000+ custom agents running on the platform (Mar 2026); 500+ prebuilt agents.
- Marquee early clients: **Allen & Overy** (now A&O Shearman; first major firmwide rollout, Feb 2023), **PwC** (Mar 2023, exclusive within Big Four for a period), Paul Weiss.

## Product (marketed — shipped state TBD in product dossier)

Core surfaces: **Assistant** (chat/draft/analyze), **Vault** (secure doc store + bulk analysis, up to 100k docs), **Knowledge** (research across legal/regulatory/tax), **Workflows** (pre-built + custom multi-step), **Agents** (500+ prebuilt, Agent Builder, ad-hoc/pre-built/custom, 25k+ custom), **Shared Spaces** (cross-org collaboration), **Contract Intelligence** (launched ~May 2026), **Command Center** (adoption analytics), **Harvey Mobile**, **Ecosystem** (integrations: Ask LexisNexis, iManage, Datasite, DeepJudge, MS Word/365). RAG-grounded with citations. **Memory** feature in fine-tuning. **Deep Research** mode.

## Tech stack (from careers pages + eng blog — high signal for the eng-role scope)

- **Languages**: Python (AI/ML services), TypeScript/Node.js (product), Go (infra). Frontend: React + TypeScript + TailwindCSS (PWA).
- **Cloud/infra**: multi-cloud **Azure + GCP**; Azure OpenAI Service; Azure Kubernetes Service; PostgreSQL; Redis; Terraform/Pulumi (IaC); Datadog + Sentry (observability); PagerDuty/Incident.io. "Billions of prompt tokens, millions of daily requests."
- **AI architecture**: agent framework built on the **OpenAI Agents SDK** (chose external lib over building their own); "**Tool Bundles**" abstraction (packaged capabilities: file search/grep, drafting sub-agents, Lexis search); model routing / model proxy; context management; heavy internal **eval** culture (BigLaw Bench, LAB); on-demand vision system for document images (cost-optimized); proprietary hallucination-decomposition/citation-verification systems; BYOK encryption for customer data.
- **Model layer**: multi-model routing across OpenAI (GPT-5/5.5), Anthropic (Claude Opus/Sonnet, Fable 5), Google (Gemini). Building **own legal foundation models** (Harvey Labs) — plans to open-source data/models/benchmarks.

## Public engineering surface (GitHub — github.com/harveyai, confirmed Harvey's org)

- `harveyai/harvey-labs` — **LAB** (Legal Agent Benchmark), Python, **467★**, pushed 2026-07-01 (actively maintained). 1,200+ tasks, 24 practice areas, 75,000+ rubric criteria.
- `harveyai/biglaw-bench` — **BigLaw Bench**, 168★, pushed 2026-03-17.
- `harveyai/deep-research-starter` — starter for OpenAI Deep Research API, Python, 11★.
- Forks: `teams-ai` (MS Teams), `pdfplumber` (PDF extraction), `react-doc-viewer`, `Recognizers-Text`. → confirms React/TS + PDF-heavy + MS-ecosystem stack.
- **Product code is closed** (private monorepo). Only benchmarks + forks are public. `counsel-ai` org exists but is empty.

## Competitive set (provisional)

- **Incumbents + AI** (Tier 1, database-grounded): Thomson Reuters **CoCounsel** (ex-Casetext, acq. $650M 2023; Westlaw-grounded; 1M+ users; public pricing ~$225/seat/mo), LexisNexis **Lexis+ AI / Protégé** (GA Feb 2026, 300+ workflows; Shepard's; runs Claude+GPT), **Westlaw Precision**, Bloomberg Law. *Note LexisNexis (via REV/RELX) is simultaneously an **investor** in Harvey and a **competitor** — a key tension.*
- **AI-native / specialized** (Tier 2): Harvey (flagship), **Legora** (EU), **Robin AI** (UK/EU contracts), **Spellbook** (Word add-in, ~$350M val), **Luminance** (contract intelligence, ~$1.5B), **Ironclad** (CLM, ~$3.2B), **EvenUp** (plaintiff/PI), **vLex** (acq. by Clio $1B Dec 2025), **GC AI** (in-house), **Eve.legal** (plaintiff).
- **Horizontal foundation labs** going vertical: OpenAI, Anthropic (both partners AND latent threats), Google.
- Harvey's edge: AmLaw-100 distribution, custom-agent flexibility (25k), platform-independence (no Westlaw/Lexis lock-in). Harvey's gap: **no native access to Westlaw/Lexis proprietary case-law corpus** — "lags on pure research." Multi-vendor is the norm (firms run Harvey + CoCounsel + a CLM).
- Pricing: enterprise-only, no public pricing. Reported ~$1,000–$1,200/user/mo, ~20-seat minimum (~$240k–$288k/yr floor).

## Recent activity (2026, provisional)

- **Jun 2026**: announced building custom **legal foundation-model series** (open-sourcing data/models/benchmarks); expanding Harvey Labs; "Training a Legal Agent with Applied Compute" blog.
- **Jun 2026**: Anthropic **Fable 5** available in Harvey (LAB all-pass 13.3% high score; BigLaw Bench 93.4%).
- **May 2026**: launched **LAB** benchmark (open-source, no leaderboard at launch; partners incl. Anthropic, OpenAI, Nvidia, DeepMind, Mistral, Stanford); **Contract Intelligence** + Command Center adoption analytics; partnerships with **Datasite** and **DeepJudge**.
- **Mar 2026**: $200M @ $11B; ARR $190M; expanding "embedded legal engineering teams" globally; Singapore/Sydney APAC expansion; marketing tie-up with Gabriel Macht (Harvey Specter, *Suits*).
- Skepticism thread: no independently-published hallucination benchmarks; Stanford HAI legal-AI hallucination studies (6–33%); "attorney verification required." Harvey's differentiation vs. "thin wrapper" critique is the recurring debate.

## Name collisions (record for every later search)

Harvey Norman (retail, AU), Harvey Nichols (retail, UK), Harvey Mudd College, Harvey (1950 film / Jimmy Stewart), Hurricane Harvey (2017), Harvey Specter (*Suits* character — ironically now a marketing partner), Steve Harvey, Harvey Weinstein (unrelated; note CEO surname is *Weinberg*, not Weinstein — easy mis-type), PJ Harvey. **Disambiguate every query** to: harvey.ai / "Harvey AI" / legal AI / Winston Weinberg / Gabriel Pereyra / Counsel AI Corporation.

## Obvious open questions (feed the dossiers)

1. **Moat durability** (thesis/competitive): is the durable value in workflow/data/eval/distribution, or does it erode when foundation labs + Westlaw/Lexis ship comparable agents? LexisNexis is both investor and rival.
2. **Marketed vs shipped** (product): 25k "custom agents" and 500+ prebuilt — how capable are they really? LAB initial results show frontier models at single-digit all-pass on long-horizon legal work ("not yet good enough"). Gap between demo and reliable production?
3. **Own foundation models** (thesis/product): real R&D moat or defensive spend against model-layer commoditization? Feasible for a company this size vs. frontier labs?
4. **Unit economics** (company/buyers): $50/task, 20+ min latency on frontier agent runs (LAB). At enterprise pricing, do the economics hold as usage scales?
5. **Org health / eng culture** (people): "re-earn your role every 6 months" intensity; senior-heavy hiring; embedded lawyers. What's it actually like to build here?
6. **Concentration risk** (buyers/company): heavy AmLaw-100 dependence; what happens in mid-market / in-house / non-US?
7. **Data-total & headcount conflicts** to resolve: total funding, AmLaw-100 %, headcount.

## Proposed topic order (standard build order)

thesis → company → product → buyers → competitive → activity → people → synthesis.
(Deepest cut, per the engineering-role scope: **product, thesis, competitive, people**.)
