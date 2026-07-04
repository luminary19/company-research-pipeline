---
type: Gather Report
topic: competitive
slice: ai-native
company: harvey
date: 2026-07-04
rounds_run: 3
stop_reason: round-cap
---

# Gather: AI-native legal startups (direct rivals)

## Scope

Covered: AI-native legal startups positioned as direct rivals to Harvey — Legora (flagship), Robin AI, Spellbook, Luminance, Ironclad, EvenUp, GC AI, Eve.legal. For each: positioning vs Harvey, funding/valuation, models used, ICP, traction, differentiation, and where each beats/loses to Harvey. Plus the published segment/landscape map (which rival owns which axis) and consolidation/M&A signals among AI-native players.

Excluded (sibling slices own): incumbents — CoCounsel/Thomson Reuters, LexisNexis/Lexis+ AI, Westlaw, Bloomberg Law, vLex → slice "incumbents". Horizontal foundation labs (Anthropic/Claude legal plug-in, OpenAI, Microsoft Copilot as model-maker competitors) → slice "labs-moat". Harvey's own internals (product, ARR, funding cadence beyond the comparison anchor) → other topic. Buyer TAM → other topic.

Note on the Harvey anchor: Harvey figures appear only as the comparison reference point that rivals are measured against. Harvey most-cited valuation is $11B (Mar 2026, Sequoia-led $200M round) with ~$190M ARR and 100,000+ lawyers across ~1,300 orgs including most of the Am Law 100. [R2·C1] (Presenc landscape, 2026-05-15, <https://presenc.ai/research/legal-ai-tools-landscape-2026>; TechCrunch, 2026-04-30, <https://techcrunch.com/2026/04/30/legal-ai-startup-legora-hits-5-6-valuation-and-its-battle-with-harvey-just-got-hotter/>). CONFLICT on Harvey valuation across dates/sources: $8B (Oct 2025, a16z-led, per legalcomplex/36kr) vs $11B (Mar 2026, per TechCrunch/Presenc); Sacra's Legora page still cites Harvey at "$5B after $300M Series E" (stale). Recorded, not resolved — Harvey is a sibling slice's subject.

## Findings

### Legora (the flagship direct rival — European, Claude-based)

**Positioning / why analysts frame it as Harvey's closest AI-native competitor.** Swedish-born (Stockholm, founded 2023 as "Leya", rebranded Legora Feb 2025), YC Winter 2024, HQ moved to New York. Explicitly framed as the "Harvey v. Legora" rivalry — TechCrunch's Anna Heim: "The Harvey-Legora rivalry is now the closest analog the legal industry has to two companies trading rounds and customer wins inside what is essentially a duopoly, with the rest of the field already an [also-ran]." [R2·C1] (TechCrunch, 2026-04-30, <https://techcrunch.com/2026/04/30/legal-ai-startup-legora-hits-5-6-valuation-and-its-battle-with-harvey-just-got-hotter/>; tech-insider, 2026-05-07, <https://tech-insider.org/legora-550-million-series-d-5-5-billion-valuation-harvey-ai-2026/>). Home-turf dynamic: Legora (European origin) is expanding into the US (offices NY, Denver, plus announced Houston/Chicago) while Harvey (US origin) pushes into Europe. [R2·C1] (TechCrunch; TFN, 2026-04-30, <https://techfundingnews.com/legora-600m-series-d-nvidia-atlassian-legal-ai-5-6b-valuation/>).

**Valuation / funding (capture the figure).** Two headline numbers to hold:
- **~$5.6B post-money** — reached April 2026 via a **$50M extension** of the Series D, bringing the round to **$600M total**; extension added Atlassian and NVentures (Nvidia's VC arm — reportedly Nvidia's first legal-tech / legal-AI investment) plus Airtree, Barclays, Geodesic, Insight, Liberty Global, Nikesh Arora. [R2·C1] (TechCrunch, 2026-04-30; Tech.eu, 2026-04-30, <https://tech.eu/2026/04/30/legora-extends-series-d-to-600m-with-backing-from-atlassian-and-nventures-reaching-56b-valuation/>; Sacra, <https://sacra.com/c/legora/>).
- **~$1.8B** — the Series C figure, **$150M closed 30 Oct 2025**, led by Bessemer Venture Partners. [R1·C1] (Legora/BusinessWire PR, 2025-10-30, <https://www.businesswire.com/news/home/20251030974157/en/>; Legora blog, <https://legora.com/blog/series-c>; corroborated ArcticStartup, 2025-10-31, <https://arcticstartup.com/legora-raises-150-million-series-c/>).
- Full ladder: Seed $10.5M (Benchmark) → Series A $25M (Jul 2024) → Series B $80M at $675M post (May 2025, ICONIQ Growth + General Catalyst) → Series C $150M at $1.8B (Oct 2025, Bessemer) → **Series D $550M at $5.55B (10 Mar 2026, led by Accel)** → +$50M extension to $600M at $5.6B (Apr 2026). Total raised >$800–850M. [R3·C1] (Sacra, <https://sacra.com/c/legora/>; recatools, 2026-06-16, <https://recatools.com/ai-directory/legora/>; nrich, 2026-04-30, <https://nrich.io/challenger-brand-gtm-library/legora>).

**Traction.** Crossed **$100M+ ARR** — Bessemer confirmed as the "fastest enterprise business ever" to $100M ARR (~18 months); Sacra estimates ARR path $3M (end-2024) → $50M (end-2025) → $100M (Apr 2026). Scaled 40 → 400+ employees in a single year; **1,000+ law firms / in-house teams across 50+ markets** (up from ~200–250 orgs in ~20 markets in May 2025). Avg annual contract ~$280K/customer (Sacra estimate). [R2·C1 on ARR/headcount] (Tech.eu, 2026-04-30; nrich; Sacra). Named clients: Bird & Bird, Cleary Gottlieb, Linklaters, Goodwin, MinterEllison, White & Case, Baker McKenzie, HSFK, Mannheimer Swartling, plus Morrison Foerster (firmwide, Jun 2026) and Barclays (in-house). [R1·C1] (Legora newsroom + Series C PR).

**Models used — Claude-based, now model-agnostic.** Anthropic's own customer case study: "Legora uses Claude throughout their platform… integrated Claude throughout their entire legal technology stack"; CEO Junestrand: "Claude's exceptional intelligence is what truly sets it apart for us"; Claude Sonnet 4 scored 18% higher on Legora's proprietary legal eval set; also uses Claude Code for dev. [R1·C1] (Anthropic case study, <https://www.anthropic.com/customers/legora>; Claude.com, <https://claude.com/customers/legora>). NUANCE/evolving: with the **Legora aOS™** launch (7 May 2026) the platform is described as **LLM-agnostic, routing across both Anthropic and OpenAI** models, built on Microsoft Azure. [R2·C1] (Law.com, 2026-05-07, <https://www.law.com/legaltechnews/2026/05/07/legora-launches-agentic-ai-legal-operating-system-legora-aos/>; recatools; Microsoft customer story, 2025-05-27, <https://www.microsoft.com/en/customers/story/23171-legora-azure-openai>). CONFLICT on characterization: aivortex frames Legora as single-model "built on Anthropic's Claude" (vs CoCounsel multi-model), while Law.com/recatools/tech-insider describe an agnostic routing layer across OpenAI+Anthropic. Recorded — likely reflects an evolution from Claude-centric to routed-agnostic as aOS launched. [R3·C4] (aivortex, 2026-04-17, <https://www.aivortex.io/legal/agentic-ai/legora-european-legal-ai/>; tech-insider, 2026-05-07).

**Celebrity marketing (the brand war with Harvey).** Legora ran the **"Law Just Got More Attractive"** OOH campaign featuring actor **Jude Law** (NYC, London, Scandinavia); signed a multi-year partnership with **Aaron Judge and the New York Yankees** (announced 8 Apr 2026); and partnered with golfer **Ludvig Åberg** — each chosen around a "standards/preparation" theme. This directly answers Harvey's brand partnership with actor **Gabriel Macht** (Harvey Specter of "Suits"). [R1·C1 on Judge/Yankees] (Legora newsroom, 2026-04-08, <https://legora.com/newsroom/legora-signs-multi-year-partnership-with-baseball-star-aaron-judge-and-the-new-york-yankees>); [R2·C1 on Jude Law + Macht contrast] (TechCrunch, 2026-04-30; nrich, 2026-04-30).

**Product / differentiation vs Harvey.** Positions itself as the "agentic operating system for legal work" (Legora aOS) — SaaS→"AaaS" (Agent-as-a-Service) framing. Modules: Agent, Tabular Review (spreadsheet-style bulk doc review), Word/Outlook add-ins, Research, Playbooks, Workflows (orchestration, Jun 2025), Portal (client-facing, GA Q1 2026). Land-and-expand; deep integration (iManage, SharePoint, MCP connectors). Certs: SOC 2 Type II, ISO 27001, ISO 42001, GDPR, HIPAA; zero training on customer data; 33+ languages incl. Arabic. [R1·C2] (Legora aOS page, <https://legora.com/product/aos>; Sacra product section; recatools). Where it beats Harvey (per commentators): European/multi-jurisdictional footprint and collaboration ("collaborative AI"), faster international expansion, brand momentum. Where it loses: Harvey's ~2x valuation ($11B vs $5.6B), larger Am Law 100 install base, and ~$600M funding "head start on belief." [R3·C2] (nrich; aivortex; tech-insider).

### Robin AI (UK/EU contracts — the cautionary tale)

**One-paragraph brief.** London-based (founded 2019 by ex-Clifford Chance disputes lawyer Richard Robinson + ML scientist James Clough), AI-powered contract drafting/review + managed legal services, targeting enterprise in-house teams; offices London, New York, Singapore. Notable 2025 collapse: after a planned **$50M round fell through** (first reported by Sifted, 24 Oct 2025), it made ~50 layoffs, faced an HMRC winding-up petition, and was **listed for distressed sale on IP-BID.com** (~$10M ARR, ~170 staff at peak, ~£11M annual loss). AI-enabled law firm **Scissero acquired Robin AI's managed legal services team** (Dec 2025, terms undisclosed). Then a **rescue: £31.2M raised at a £163M post-money valuation** (allotment 11 Mar 2026), stabilizing the company. [R2·C1] (Sifted via Law.com, 2025-10-29, <https://www.law.com/legaltechnews/2025/10/29/reports-of-robin-ai-insolvency-grow-/>; Legal IT Insider, 2025-10-28, <https://legaltechnology.com/robin-ai-listed-for-distressed-sale-nine-months-after-making-the-sunday-times-100-tech-list/>; Law.com/Scissero, 2025-12-09, <https://www.law.com/legaltechnews/2025/12/09/reports-emerge-of-a-possible-buyer-for-part-of-robin-ai-/>).

**Funding.** Series A Feb 2023 (SoftBank-led); Series B £20.6M / ~$26M Jan 2024 (led by Temasek); £19.8M / ~$25M extension Nov 2024 (PayPal Ventures, Cambridge University, customer consortium); backers also include Google, QuantumLight (Revolut's Nik Storonsky). ~$69M raised pre-collapse; then the **£31.2M rescue at £163M** (Mar 2026). [R2·C2] (Nonbillable/Sifted, <https://www.nonbillable.co.uk/news/robin-ai-job-cuts-funding-setback>; 36kr, <https://eu.36kr.com/en/p/3566918367870082>); rescue figure single-source [R3·C3] (Funding Spotter, 2026-03-23, <https://www.fundingspotter.com/news/robin-ai-growth-round>).

**ICP / differentiation vs Harvey.** In-house legal teams, contract review/negotiation + managed services; UK/EU-centric. Investors judged growth "not AI-level" (~50–100x ARR expectations unmet). Legal IT Insider's read: "Robin AI attempted to grow in order to compete with the likes of Harvey and Legora and its losses indicated that it has scaled too quickly." Where it loses to Harvey: growth rate, capital position, product breadth — the clearest example of an AI-native rival that could not keep pace. [R2·C1] (Legal IT Insider, 2025-10-28; Artificial Lawyer, 2025-10-27, <https://www.artificiallawyer.com/2025/10/27/robin-ai-lays-off-staff-as-growth-disappoints/>).

### Spellbook (Word add-in, contract drafting — mid-market)

**One-paragraph brief.** St. John's/Toronto-founded (CEO Scott Stevenson), launched the first GenAI contract-review tool in 2022; "Cursor for contracts." Works **inside Microsoft Word** (draft, redline, review against playbooks, compare-to-market). Serves **4,000–4,500 legal teams in 80+ countries**; tripled revenue in 2025, on pace toward $100M ARR; 10M+ contracts. [R1·C1] (Spellbook.com; Spellbook Series B blog, 2025-10-09, <https://spellbook.com/blog/series-b>).

**Funding.** **$50M Series B at $350M post-money (9 Oct 2025), led by Khosla Ventures (Keith Rabois, ex-lawyer, joined board).** Prior: $10.9M seed (May 2023, Moxxie) → $20M Series A (Jan 2024, Inovia). Plus a **$40M debt facility from RBCx (Mar 2026) explicitly earmarked for M&A/acquisitions** in the consolidating legal-AI market. Total ~$120M+ ($80M+ equity + $40M debt). Backers incl. Thomson Reuters Ventures, The LegalTech Fund. [R2·C1] (Law.com, 2025-10-09, <https://www.law.com/legaltechnews/2025/10/09/contract-platform-spellbook-announces-50m-series-b-funding-round/>; BetaKit, <https://betakit.com/spellbook-raises-50-million-usd-series-b-led-by-khosla-ventures/>; BusinessWire, <https://www.businesswire.com/news/home/20260304571140/en/>; Sacra, <https://sacra.com/c/spellbook/>).

**Models used.** Powered by state-of-the-art LLMs — **OpenAI GPT-5 and Anthropic Opus** (per own site/PR). [R1·C1] (Spellbook.com; BusinessWire, 2025-10-09).

**ICP / differentiation vs Harvey.** Mid-market + in-house transactional/commercial legal; publishes-ish pricing; Word-native ergonomics (no context switch). Owns the "mid-market & solo" axis in the landscape map. Where it beats Harvey: lower friction / lower cost for smaller teams, Word embedding. Where it loses: not built for Am Law 100 breadth or litigation/research; competes downmarket. [R3·C2] (Presenc, 2026-05-15; Sacra competition section).

### Luminance (contract intelligence — document volume)

**One-paragraph brief.** London-based (spun out of Cambridge; early backing from Invoke Capital / Mike Lynch, Slaughter & May). Contract intelligence / document analysis built on its **own proprietary "Legal-Grade" pre-trained legal LLM** (marketed differentiator: does not rely solely on general-purpose models). Landscape leader on **document volume** — 150M+ docs processed. [R1·C2] (Luminance press, <https://www.luminance.com/press/luminance-raises-75-million-in-series-c-funding-round-led-by-point72-private-investments>; Presenc landscape).

**Funding.** **$75M Series C (18 Feb 2025), led by Point72 Private Investments**; brought fundraising to $115M+ over the prior year and **~$165M total**. Prior: $40M Series B (Apr 2024, March Capital). [R1·C1] (Luminance press, 2025-02-18; parsers.vc, <https://parsers.vc/startup/luminance.com/> lists total ~$118M disclosed). **CONFLICT on valuation:** Presenc's landscape table lists Luminance at "~$1.5B (Series C)" [R3·C3, sole source] (Presenc, <https://presenc.ai/research/legal-ai-tools-landscape-2026>), but no primary funding announcement discloses a valuation, and a $75M Series C on ~$165M total makes a $1.5B post-money implausible/unconfirmed. Recorded, not resolved — treat the $1.5B as an unverified single-source figure.

**ICP / differentiation vs Harvey.** Enterprise contract analysis, due diligence, M&A doc review; horizontal across legal + procurement/commercial. Beats Harvey on raw document-processing throughput and its owned-model story; loses on generalist legal reasoning/research breadth and Am Law distribution. [R3·C2] (Presenc "document volume" axis).

### Ironclad (CLM + AI — contract lifecycle management)

**One-paragraph brief.** US contract lifecycle management (CLM) platform adding AI (its "Jurist" AI assistant, agent-based, for draft/review/negotiate/research). Named a Leader in the 2025 Gartner Magic Quadrant for CLM and Forrester Wave Q1 2025. Landscape leader on the **"CLM + AI"** axis. [R1·C2] (Ironclad.com, <https://ironcladapp.com/>; Presenc landscape).

**Funding / scale.** Latest widely-cited valuation **~$3.2B** (this is the Jan 2022 Series E figure, led by Franklin Templeton; no newer priced round surfaced). **~$150M ARR.** [R3·C3, single/stale source for $3.2B] (Presenc, 2026-05-15; Sacra Legora/Spellbook competition sections cite Ironclad $150M ARR). ICP: enterprise legal ops / in-house contracting (system-of-record: approvals, routing, post-signature analytics). Differentiation vs Harvey: owns the CLM workflow + repository layer Harvey does not; loses on generative legal research and firm-side (BigLaw) work. Named by Sacra as the most direct competitor to Spellbook as Spellbook moves upmarket. [R3·C2] (Sacra Spellbook, <https://sacra.com/c/spellbook/>).

### EvenUp (plaintiff / personal-injury demand letters)

**One-paragraph brief.** San Francisco (founded 2019, CEO Rami Karabibar; co-founders Ray Mieszaniec, an ex-PI attorney). Category leader in AI for **personal-injury (plaintiff-side)** — Claims Intelligence Platform powered by its **proprietary "Piai" model** (trained on hundreds of thousands of injury cases + millions of medical records). Products: demand letters, medical chronologies, negotiation prep, PLAAS (Pre-Litigation as a Service). 2,000+ PI firms (incl. 20% of top-100 US PI firms), ~10,000 cases/week, 200,000+ cases resolved, $10B+ damages, 250K+ verdict/settlement dataset. [R1·C1] (EvenUp PR/blog, 2025-10-07, <https://www.evenuplaw.com/blog/evenup-2b-valuation/>; LawSites, <https://www.lawnext.com/2025/10/evenup-ai-platform-for-personal-injury-lawyers-raises-150m-at-2b-valuation.html>).

**Funding (conflict resolved by dates).** **$150M Series E at $2B+ valuation (7 Oct 2025), led by Bessemer** (with REV/RELX-LexisNexis' VC arm, B Capital, SignalFire, Adams Street, Premji, Bain Capital, HarbourVest, Lightspeed, Broadlight); total raised $385M; 4th round in 24 months. The earlier "$135M Series D unicorn / >$1B" figure (per haqq's map) is the **prior round (Oct 2024)** — valuation doubled in <1 year. [R2·C1] (Fortune, 2025-10-07, <https://fortune.com/2025/10/07/exclusive-evenup-raises-150-million-series-e-at-2-billion-valuation-as-ai-reshapes-personal-injury-law/>; Crunchbase News, 2025-10-07, <https://news.crunchbase.com/venture/legal-tech-ai-unicorn-evenup-ai-doubles-valuation/>; prior Series D: Crunchbase, 2024-10-08, <https://news.crunchbase.com/venture/ai-legal-tech-evenup-unicorn-bain/>).

**ICP / differentiation vs Harvey.** Plaintiff PI firms — a workflow-native vertical Harvey does not serve (Harvey = BigLaw/in-house generalist). Not competing for the same buyer; owns the "plaintiff-side" axis alongside Eve. Notable strategic signal: LexisNexis' VC arm (REV) is on the cap table. [R2·C2] (LawSites; alatirok, 2026-05-20, <https://alatirok.com/legal-ai-2026-harvey-vs-evenup-vs-robin-ai-vs-spellbook/>).

### GC AI (in-house counsel agent)

**One-paragraph brief.** SF/San Mateo in-house-counsel copilot; founder is a three-time General Counsel. Built end-to-end for corporate in-house teams (concise, business-focused outputs shaped by a ~20,000-line system prompt; Skill Library for MSAs/NDAs/DPAs; contract agents in Word). **Rare public pricing: from $500/seat/month.** 1,500+ in-house teams (named: Vercel, Snyk, Tipalti, Gusto, Hitachi, Tonal, Arc'teryx). Revenue reportedly grew $1M → $10M in one year. [R1·C1 on positioning/pricing] (GC AI, <https://gc.ai/>); [R2·C2 on revenue] (legalcomplex, 2026-01-07, <https://legalcomplex.com/blog/legal-tech-raised-6bn-in-2025-as-ai-boom-shows-divisions>).

**Funding.** ~$73M raised, Series A stage. [R3·C3, single source for $73M figure] (haqq, 2026-06-15, <https://haqq.ai/blog/san-francisco-legal-ai-startups>; Presenc lists "Series A").

**ICP / differentiation vs Harvey.** Generalist in-house counsel wanting concise answers for busy stakeholders — GC AI markets itself as "the only legal AI built end to end for in-house counsel," contrasting its 3-time-GC founder + in-house-tuned outputs against Harvey's Big-Law origin. Owns the "in-house counsel" axis in the landscape map. Beats Harvey on in-house-specific UX/pricing transparency at the low end; loses on BigLaw distribution, litigation, and deep caselaw research (GC AI explicitly says specialized/research-heavy practices should use other platforms). [R1·C2] (GC AI comparison page; Presenc axis table).

### Eve.legal (plaintiff-side litigation OS)

**One-paragraph brief.** San Mateo (founded 2023, CEO Jay Madheswaran). "EveOS" — the AI operating system for **plaintiff law** (PI, med-mal, workers' comp, SSDI, labor & employment): intake, casework automation, medical-chronology from tens of thousands of pages, legal research, nightly case review, firm analytics. Trusted by 1,200+ plaintiff firms (450+ as of Sep 2025); processes 200,000+ cases annually; customers recovered $3.5B+ in settlements. [R1·C1] (Eve.legal, <https://eve.legal/>; Eve PR, 2025-09-30, <https://www.prnewswire.com/news-releases/eve-raises-103-million-at-1-billion-valuation-to-help-plaintiff-firms-deliver-justice-through-ai-transformation-302570807.html>).

**Funding.** **$103M Series B at $1B+ valuation (30 Sep 2025), led by Spark Capital** (with a16z, Lightspeed, Menlo Ventures). ~$164M raised total (per haqq). [R1·C1 on Series B] (Eve PRNewswire, 2025-09-30; LawSites); total figure [R3·C3] (haqq, 2026-06-15).

**ICP / differentiation vs Harvey.** Plaintiff firms — like EvenUp, a vertical Harvey does not target. Competes with EvenUp (both plaintiff), not directly with Harvey. Beats Harvey on plaintiff-firm-native, matter-based, high-volume medical-record workflows; loses on generalist BigLaw/corporate scope. Emphasizes privilege/confidentiality vs consumer AI. [R1·C2] (Eve.legal; Eve PR).

## Segment map (which rival owns which axis)

The published Presenc "Category Leaders by Axis" table (2026-05-15) maps cleanly onto the slice brief. [R3·C1 as a published landscape table] (Presenc, <https://presenc.ai/research/legal-ai-tools-landscape-2026>):

| Axis | Leader |
|---|---|
| Am Law 100 install base | **Harvey** |
| Mid-market & solo | **Spellbook** |
| Document volume processed | **Luminance** (150M+ docs) |
| Research / citation | **CoCounsel + Lexis+ AI** (tied — incumbents, sibling slice) |
| CLM + AI | **Ironclad** |
| In-house counsel | **GC AI** |
| Plaintiff-side | **Eve.legal** (and EvenUp for PI demand generation) |

Presenc "Top Tools at a Glance" table figures (single-source landscape values, several uncorroborated): Harvey $11B / $190M ARR; Luminance ~$1.5B (Series C) / 150M+ docs; Spellbook ~$350M (Series B) / 4,000+ teams; Ironclad ~$3.2B / late-stage; GC AI Series A; Eve.legal Series A. [R3·C3] (Presenc). Note: the $350M Spellbook figure is corroborated by primary PR (C1); the $1.5B Luminance and $3.2B Ironclad figures are NOT independently corroborated and are flagged above.

Complementary "SF map" framing (haqq, 2026-06-15): Harvey (~$1.2B raised, ~$11B), Eve (~$164M raised, San Mateo), EvenUp (~$135M Series D framing, unicorn), GC AI (~$73M raised, $500/seat/mo), Ivo (contract review in Word, enterprise in-house, ~$77M raised, ~$6,000/seat/yr). Shared assumption across all: English-first, US common law, Word-native, enterprise-SaaS pricing. [R3·C2] (haqq, <https://haqq.ai/blog/san-francisco-legal-ai-startups>). (Ivo surfaced as an additional AI-native contract-review rival not in the original brief list — recorded as a lead.)

Analyst read (multiple): the field is increasingly framed as a **Harvey–Legora duopoly at the top**, with vertical specialists (Spellbook mid-market, GC AI in-house, EvenUp/Eve plaintiff, Luminance/Ironclad contracts) each winning a niche while horizontal generalists "struggle below the Am Law 200 line." [R2·C2] (TechCrunch, 2026-04-30; Presenc "six things" #5; tech-insider, 2026-05-07).

## Consolidation / M&A signals among AI-native players

- **Clio acquired vLex for ~$1B (Dec 2025)** — largest deal in Clio's history; creates an SMB legal stack competing with Harvey-into-AmLaw "from below." (vLex is an incumbent-research asset → sibling slice, but the deal is the top consolidation signal in legal AI.) [R2·C1] (Presenc; legalcomplex, 2026-01-07).
- **Legora acquired Walter AI (Canadian legal-AI startup, Mar 2026)** to bolster agentic capabilities in Legora aOS. [R2·C1] (Law.com, 2026-05-07, <https://www.law.com/legaltechnews/2026/05/07/legora-launches-agentic-ai-legal-operating-system-legora-aos/>).
- **Scissero (AI-enabled law firm) acquired Robin AI's managed legal services team (Dec 2025)** out of Robin's distressed-sale process; Robin's core AI business then rescued via £31.2M round (Mar 2026). [R2·C1] (Law.com, 2025-12-09).
- **Spellbook secured a $40M RBCx debt facility (Mar 2026) explicitly to fund acquisitions of smaller legal-AI competitors** — a stated consolidation play. [R1·C1] (BusinessWire, 2026-03-04, <https://www.businesswire.com/news/home/20260304571140/en/>).
- **Legora × Ironclad AI-to-AI partnership (Jun 2026)** — pairs Legora's analysis/research AI with Ironclad's contracting AI across the contract lifecycle (integration, not acquisition). [R1·C2] (Legora newsroom, 2026-06-17).
- Market context: 2025 legal-tech funding ~$5.99B (up 22%), 14 rounds of $100M+; 2025 exits totaled $2.29B (down 39%), only 10% of deals disclosed price; top exit vLex ($1B). [R2·C1] (legalcomplex, 2026-01-07). (haqq cites a narrower "$2.4B in 2025" for legal-AI specifically vs legalcomplex's broader "legal-tech" $5.99B — different scope, not a true conflict.)

## Reflection trace

- **Round 1** — searched (1) Legora funding/valuation/celebrity marketing/why-Harvey's-closest-rival, and (2) broad AI-native landscape (Robin/Spellbook/Luminance/Ironclad/EvenUp/GC AI/Eve); then batch-crawled legalcomplex + haqq + Presenc + Sacra/Legora. Closed: Legora full funding ladder, ARR, traction, celebrity war, segment map (Presenc axis table), and headline figures for all 8 rivals. Remaining gaps: Robin AI funding history + "troubles" detail; Luminance/Ironclad valuation provenance; EvenUp round/valuation conflict; each rival's model stack.
- **Round 2** — aimed at Robin AI (funding + collapse) + Luminance funding, and EvenUp round/valuation + Ironclad + Legora models. Closed: Robin AI full saga (failed $50M raise → layoffs → insolvency listing → Scissero buys managed-services → £31.2M/£163M rescue Mar 2026); Luminance $75M Series C (Point72, ~$165M total) which contradicts Presenc's $1.5B; EvenUp conflict resolved ($150M Series E $2B+ Oct 2025 vs prior $135M Series D $1B Oct 2024). Remaining: explicit Legora model confirmation; Spellbook round specifics; Ironclad current valuation.
- **Round 3 / stop** — searched Legora model stack + Spellbook/Ironclad funding. Closed: Legora Claude-based (Anthropic case study; Sonnet 4 +18% on their eval) evolving to model-agnostic aOS routing OpenAI+Anthropic; Spellbook $50M Series B at $350M (Khosla/Rabois, Oct 2025) + $40M RBCx debt for M&A + GPT-5/Opus models. **Stopped at round-cap (3);** remaining minor gaps (Ironclad current priced valuation, Luminance exact valuation, Eve's model stack) judged low-yield for this slice.

## Gaps and not-found

- **Ironclad current valuation (priced round):** only the stale ~$3.2B (2022 Series E, Franklin Templeton) figure surfaced; no 2024–2026 priced round found in the searches run. Not evidence of absence — a targeted Ironclad-funding search was not spent (round-cap).
- **Luminance valuation:** no primary source discloses a post-money valuation on the $75M Series C; Presenc's ~$1.5B is uncorroborated and inconsistent with round size (flagged as CONFLICT, not resolved).
- **Eve.legal model stack:** not disclosed in sources touched (Eve emphasizes purpose-built plaintiff workflows + privilege, but does not name underlying LLMs). Not searched to exhaustion.
- **GC AI exact funding total:** $73M is single-source (haqq); no primary GC AI funding announcement crawled.
- **Robin AI rescue round (£31.2M/£163M):** single-source (Funding Spotter); the surrounding distress narrative is heavily corroborated (Law.com, Sifted, Legal IT Insider, City AM, 36kr), but the specific rescue figure/valuation was not independently confirmed.
- **Ivo:** surfaced as an additional AI-native contract-review rival (enterprise in-house, Word-based, ~$77M raised, ~$6,000/seat/yr) not in the original brief; recorded as a lead, not researched in depth.

## Sources consulted

Grades per playbook 02-epistemics §3. R1 = rival's own site/funding PR or lead investor; R2 = established outlet/trade press (TechCrunch, Law.com, Artificial Lawyer, Sifted, Fortune, Crunchbase News, Legal IT Insider, Tech.eu, BetaKit, PRNewswire/BusinessWire wire PR); R3 = landscape/comparison/aggregator blogs; R4 = promotional. Sole-source figures capped at C3.

**Legora**
- <https://techcrunch.com/2026/04/30/legal-ai-startup-legora-hits-5-6-valuation-and-its-battle-with-harvey-just-got-hotter/> — TechCrunch, 2026-04-30 [R2·C1]
- <https://tech.eu/2026/04/30/legora-extends-series-d-to-600m-with-backing-from-atlassian-and-nventures-reaching-56b-valuation/> — Tech.eu, 2026-04-30 [R2·C1]
- <https://techfundingnews.com/legora-600m-series-d-nvidia-atlassian-legal-ai-5-6b-valuation/> — TFN, 2026-04-30 [R2·C2]
- <https://www.businesswire.com/news/home/20251030974157/en/> — Legora Series C PR (BusinessWire), 2025-10-30 [R1·C1]
- <https://legora.com/blog/series-c> — Legora, 2025-10-30 [R1·C1]
- <https://arcticstartup.com/legora-raises-150-million-series-c/> — ArcticStartup, 2025-10-31 [R2·C1]
- <https://sacra.com/c/legora/> — Sacra (estimates), 2025-10 [R3·C2]
- <https://legora.com/newsroom/legora-signs-multi-year-partnership-with-baseball-star-aaron-judge-and-the-new-york-yankees> — Legora newsroom, 2026-04-08 [R1·C1]
- <https://nrich.io/challenger-brand-gtm-library/legora> — nrich (GTM case study), 2026-04-30 [R3·C2]
- <https://legora.com/> and <https://legora.com/product/aos> — Legora site/aOS [R1·C2]
- <https://www.anthropic.com/customers/legora> and <https://claude.com/customers/legora> — Anthropic case study [R1·C1 for "uses Claude"]
- <https://www.law.com/legaltechnews/2026/05/07/legora-launches-agentic-ai-legal-operating-system-legora-aos/> — Law.com, 2026-05-07 [R2·C1]
- <https://www.microsoft.com/en/customers/story/23171-legora-azure-openai> — Microsoft customer story, 2025-05-27 [R1·C2]
- <https://recatools.com/ai-directory/legora/> — recatools review, 2026-06-16 [R3·C2]
- <https://www.aivortex.io/legal/agentic-ai/legora-european-legal-ai/> — AI Vortex, 2026-04-17 [R3·C3]
- <https://tech-insider.org/legora-550-million-series-d-5-5-billion-valuation-harvey-ai-2026/> — tech-insider, 2026-05-07 [R3·C2]

**Robin AI**
- <https://www.law.com/legaltechnews/2025/10/29/reports-of-robin-ai-insolvency-grow-/> — Law.com, 2025-10-29 [R2·C1]
- <https://legaltechnology.com/robin-ai-listed-for-distressed-sale-nine-months-after-making-the-sunday-times-100-tech-list/> — Legal IT Insider, 2025-10-28 [R2·C1]
- <https://www.artificiallawyer.com/2025/10/27/robin-ai-lays-off-staff-as-growth-disappoints/> — Artificial Lawyer, 2025-10-27 [R2·C1]
- <https://www.law.com/legaltechnews/2025/12/09/reports-emerge-of-a-possible-buyer-for-part-of-robin-ai-/> — Law.com (Scissero), 2025-12-09 [R2·C1]
- <https://www.nonbillable.co.uk/news/robin-ai-job-cuts-funding-setback> — Nonbillable/Sifted, 2025-10 [R2·C2]
- <https://www.fundingspotter.com/news/robin-ai-growth-round> — Funding Spotter (rescue round), 2026-03-23 [R3·C3]
- <https://eu.36kr.com/en/p/3566918367870082> — 36Kr, 2025-10 [R3·C2]
- <https://robinai.com/> — Robin AI site [R1·C2]
- <https://pitchbook.com/profiles/company/442688-14> — PitchBook profile (not opened past teaser) [R2·C3]

**Spellbook**
- <https://www.law.com/legaltechnews/2025/10/09/contract-platform-spellbook-announces-50m-series-b-funding-round/> — Law.com, 2025-10-09 [R2·C1]
- <https://spellbook.com/blog/series-b> — Spellbook, 2025-10-09 [R1·C1]
- <https://betakit.com/spellbook-raises-50-million-usd-series-b-led-by-khosla-ventures/> — BetaKit, 2025-10-09 [R2·C1]
- <https://www.businesswire.com/news/home/20260304571140/en/> — Spellbook/RBCx debt PR, 2026-03-04 [R1·C1]
- <https://sacra.com/c/spellbook/> — Sacra, 2025-10-10 [R3·C2]
- <https://www.clay.com/dossier/spellbook-funding> — Clay aggregator [R3·C3]
- <https://spellbook.com/> — Spellbook site [R1·C1 for models/scale]

**Luminance**
- <https://www.luminance.com/press/luminance-raises-75-million-in-series-c-funding-round-led-by-point72-private-investments> — Luminance press, 2025-02-18 [R1·C1]
- <https://parsers.vc/startup/luminance.com/> — parsers.vc aggregator [R3·C2]

**Ironclad**
- <https://ironcladapp.com/> — Ironclad site [R1·C2]
- (Ironclad $3.2B / $150M ARR via Presenc + Sacra competition sections — see below) [R3·C3]

**EvenUp**
- <https://fortune.com/2025/10/07/exclusive-evenup-raises-150-million-series-e-at-2-billion-valuation-as-ai-reshapes-personal-injury-law/> — Fortune, 2025-10-07 [R2·C1]
- <https://news.crunchbase.com/venture/legal-tech-ai-unicorn-evenup-ai-doubles-valuation/> — Crunchbase News, 2025-10-07 [R2·C1]
- <https://www.lawnext.com/2025/10/evenup-ai-platform-for-personal-injury-lawyers-raises-150m-at-2b-valuation.html> — LawSites, 2025-10-07 [R2·C1]
- <https://www.evenuplaw.com/blog/evenup-2b-valuation/> — EvenUp blog, 2025-10-07 [R1·C1]
- <https://www.businesswire.com/news/home/20251007138957/en/> — EvenUp Series E PR, 2025-10-07 [R1·C1]
- <https://news.crunchbase.com/venture/ai-legal-tech-evenup-unicorn-bain/> — Crunchbase News (Series D), 2024-10-08 [R2·C1]
- <https://legaltechnology.com/2024/10/08/evenup-raises-135m-series-d-valuing-the-personal-injury-startup-at-1bn/> — Legal IT Insider, 2024-10-08 [R2·C1]
- <https://evenuplaw.com/> — EvenUp site [R1·C2]

**GC AI**
- <https://gc.ai/> — GC AI site (positioning, $500/seat/mo, clients) [R1·C1]
- (GC AI $73M via haqq; revenue $1M→$10M via legalcomplex — see below) [R2·C2 / R3·C3]

**Eve.legal**
- <https://www.prnewswire.com/news-releases/eve-raises-103-million-at-1-billion-valuation-to-help-plaintiff-firms-deliver-justice-through-ai-transformation-302570807.html> — Eve PR (PRNewswire), 2025-09-30 [R1·C1]
- <https://eve.legal/> — Eve site [R1·C1]

**Landscape / M&A / cross-cutting**
- <https://presenc.ai/research/legal-ai-tools-landscape-2026> — Presenc landscape (axis table, tool table), 2026-05-15 [R3·C2 as landscape; C3 for its sole-source valuations]
- <https://haqq.ai/blog/san-francisco-legal-ai-startups> — HAQQ SF map, 2026-06-15 [R3·C2]
- <https://legalcomplex.com/blog/legal-tech-raised-6bn-in-2025-as-ai-boom-shows-divisions> — Legalcomplex/Artificial Lawyer, 2026-01-07 [R2·C1]
- <https://alatirok.com/legal-ai-2026-harvey-vs-evenup-vs-robin-ai-vs-spellbook/> — Alatirok comparison, 2026-05-20 [R3·C2]
