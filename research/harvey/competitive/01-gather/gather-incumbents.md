---
type: Gather Report
topic: competitive
slice: incumbents
company: Harvey (harvey.ai)
date: 2026-07-04
rounds_run: 3
stop_reason: All five slice sub-topics covered with corroboration across R1–R3 sources; hit the 3-round cap with no remaining high-value gaps for the incumbent slice.
---

## Scope

This report organizes evidence on Harvey's **incumbent, database-grounded legal-AI competitors** — the legacy legal-research publishers that own proprietary case-law corpora and have bolted AI onto them. Covered: (1) Thomson Reuters CoCounsel / Westlaw, (2) LexisNexis Lexis+ with Protégé, (3) Bloomberg Law AI, (4) vLex/Fastcase and the Clio acquisition, plus (5) a head-to-head vs Harvey and the corpus-gap dynamic. Facts here are about Harvey's RIVALS, not Harvey's own product internals.

**Excluded (owned by sibling slices):** AI-native startups (Legora, Robin, Spellbook, Luminance, Ironclad, EvenUp, GC AI → "ai-native" slice); foundation labs going vertical (→ "labs-moat" slice); Harvey's own product internals and buyer TAM. Where a source touches Harvey pricing/positioning, it is included only as a comparison anchor.

**Grading key:** R1 = vendor's own product/pricing/press page (authoritative for "what they market," weak for competitive claims) or official filing; R2 = Law.com, LawSites/LawNext, Artificial Lawyer, Reuters/PRNewswire, established trade press; R3 = comparison/review blogs (several AI-assisted). Sole-source items capped at C3. Conflicting figures surfaced inline.

**Disambiguation:** "Harvey" = harvey.ai legal AI (not the hurricane, actor, or Harvey Nichols). "CoCounsel" = TR/Casetext product (not the unrelated "CoCounsel" nonprofit or other legal-services marketplaces). "Vincent" = vLex's AI (common first name — confirmed all cites are vLex). "Protégé" = LexisNexis assistant (generic word; all cites verified to LexisNexis). "REV" = RELX's VC arm (also styled "Rev Ventures").

---

## Findings

### 1. Thomson Reuters CoCounsel (ex-Casetext, acquired $650M, 2023)

**What it is / scale.** CoCounsel is TR's flagship legal AI assistant, originally built by legal-research startup Casetext (launched 2023 as "the first AI legal assistant of its kind") and acquired by Thomson Reuters for **$650M in 2023** (four months after CoCounsel's release). On **Feb 24, 2026 TR announced CoCounsel reached 1 million users across 107 countries/territories** — spanning legal, tax, audit, compliance, risk, and global-trade professionals (not legal-only); TR did not break out active vs. licensed seats. The milestone sent TR stock up ~11–12%, its biggest one-day jump since 2009. TR says **4,500+ subject-matter experts** contribute to validating CoCounsel outputs.
- https://www.lawnext.com/2026/02/three-years-after-launching-as-first-ai-legal-assistant-cocounsel-reaches-1-million-users-and-thomson-reuters-teases-whats-ahead.html [R2]
- https://legaltech.ca/2026/02/24/thomson-reuters-cocounsel-one-million-professionals/ [R2]
- https://www.artificiallawyer.com/2026/02/24/trs-cocounsel-hits-1-millions-users-despite-claude-crash/ [R2]
- https://www.prnewswire.com/news-releases/one-million-professionals-turn-to-cocounsel-as-thomson-reuters-scales-ai-for-regulated-industries-302694903.html [R1]
- https://finimize.com/content/thomson-reuters-cocounsel-hit-1-million-users [R2]

**GA capabilities.** **CoCounsel Legal launched Aug 5, 2025** with agentic **Deep Research** (multi-step research agents that formulate a plan, iteratively find/analyze Westlaw documents, and produce structured memos with citations), "guided workflows" (lease-abstract, 8-K generation, contract benchmarking, complaint/discovery drafting, deposition review), plus a Litigation Document Analyzer (replacing "Quick Check"). A **new "Westlaw Advantage"** tier (launched Aug 13, 2025) carries the Deep Research agentic layer. Core capabilities also include document review, contract analysis, deposition prep, and a Timeline tool. Grounded in Westlaw's case law + Practical Law, with **KeyCite** for citation verification.
- https://www.law.com/legaltechnews/2025/08/05/thomson-reuters-launches-cocounsel-legal-introduces-westlaw-advantage-with-agentic-ai-deep-research-capabilities/ [R2]
- https://www.lawnext.com/2025/08/thomson-reuters-launches-cocounsel-legal-with-agentic-ai-and-deep-research-capabilities-along-with-a-new-and-final-version-of-westlaw.html [R2]
- https://ailawyertoolscompared.com/westlaw-ai/ [R3]

**2025–26 launches / models.** TR is rebuilding CoCounsel Legal from the ground up ("next generation," **early access opened week of Jun 22, 2026; full US GA planned Aug 2026**, then Canada/UK/Australia). The next-gen product is **built on Anthropic's Claude Agent SDK**, shifts from discrete "skills" to a conversational "senior-associate" agent that drafts a plan and produces a single iterable work product, and adds Workspaces, "Brief Builder," and firm-intelligence skill authoring. TR frames this as **"fiduciary-grade AI"** (grounded from step one, traceable citations, inspectable reasoning, no third-party model training on client data) and positions CoCounsel as an "agentic operating system" reachable via API/MCP across Google, Microsoft, OpenAI, AWS, and Anthropic. Underlying models are **multi-model** (historically GPT-4 + proprietary TR AI; now heavily Claude/Anthropic, with OpenAI + Google also used). Note: Artificial Lawyer references a Feb 2026 "Claude Crash" (an Anthropic outage) that CoCounsel weathered.
- https://www.lawnext.com/2026/06/thomson-reuters-opens-early-access-to-the-next-generation-of-cocounsel-legal-saying-beta-users-fing-loved-the-product.html [R2]
- https://www.law.com/legaltechnews/2026/06/22/thomson-reuters-announces-new-features-early-access-to-next-gen-of-cocounsel-legal-/ [R2]
- https://via.news/technology/thomson-reuters-cocounsel-ai-hits-1-million-users-globally-as-legal-industry [R3]

**Pricing.** TR does not publish a clean rate card. Third-party figures cluster at **CoCounsel Core ≈ $225/user/mo** as a Westlaw add-on; **Westlaw Precision bundled with CoCounsel ≈ $428/user/mo**; **All Access ≈ $500/user/mo**; per-task "On Demand" ≈ $50–75. **As of 2026 CoCounsel is Westlaw-only — no standalone product** — so real all-in cost is typically **$300–$600+/user/mo** (Westlaw base $200–400 + CoCounsel add-on ~$100–225). Some large firms report CoCounsel bundled at no extra charge during multi-year Westlaw renewals. (Conflicting labels across aggregators: "Basic Research ~$220," "Essentials" a lower entry tier ~$1,464/mo for a 5-attorney firm ≈ $293/seat.)
- https://www.aivortex.io/legal/compare/cocounsel-pricing-2026/ [R3]
- https://spellbook.com/learn/cocounsel-pricing [R3]
- https://www.casefleet.com/blog/legal-ai-pricing-rate-limits-and-overages [R3]

**Strength vs Harvey:** Westlaw's decades-curated, licensed case-law corpus + KeyCite citation verification, native to firms' existing research workflow, 1M-user distribution, and a lower add-on price for existing Westlaw shops. **Weakness vs Harvey:** hard Westlaw lock-in (no portable/standalone option); historically strongest in litigation/research, weaker on M&A/transactional and on custom firm-specific agent building; limited workflow customization vs Harvey's Agent Builder.

---

### 2. LexisNexis Lexis+ with Protégé (GA Feb 24, 2026)

**What it is.** Protégé is LexisNexis's gen-AI legal workflow platform, publicly launched as a personalized assistant ~late 2024, **entered US Commercial Preview Jan 21, 2026, and hit general availability Feb 24, 2026, replacing the prior "Lexis+ AI."** GA ships with **300+ pre-built workflows** (motion drafting, clause/contract generation, redlining, risk analysis, citation checks) plus a **no-code Workflow Builder** and a concierge service. Grounded in the LexisNexis content repository + users' own documents, bolstered by **Shepard's Citations**. Global rollout across Canada/UK/Europe/APAC planned through 2026.
- https://www.law.com/legaltechnews/2026/02/24/lexisnexis-announces-general-availability-of-ai-workflow-platform-lexis-with-protg/ [R2]
- https://www.lexisnexis.com/community/pressroom/b/news/posts/general-availability-of-lexis-with-protege-sets-new-standard-for-automating-legal-work-with-easy-to-use-authoritative-ai-workflows [R1]
- https://www.lexisnexis.com/community/pressroom/b/news/posts/lexisnexis-unveils-global-launch-of-protege-ai-workflows-for-legal-professionals [R1]

**Models.** **Multi-model — Anthropic, Google, and OpenAI foundation models** customized for legal by LexisNexis (one comparison specifies "direct access to GPT-5 and Claude" through the Lexis interface). On Feb 24, 2026 LexisNexis also integrated **Anthropic's legal "plugin"/Legal skills** into Protégé.
- https://www.aivortex.io/legal/agentic-ai/lexis-protege-vs-cocounsel-vs-harvey/ [R3]
- https://www.law.com/legaltechnews/2026/02/24/lexisnexis-announces-general-availability-of-ai-workflow-platform-lexis-with-protg/ [R2]

**May 7, 2026 "next evolution" expansion.** Six new/expanded components: **Protégé Work** (skills-and-orchestration layer — describe a goal in natural language, Protégé routes to a skill, presents a structured plan, then executes → the "centerpiece," moving from a workflow library to an agentic framework); **Protégé Agentic Drafting** (purpose-built drafting agents for contracts/motions/briefs/deal docs); **Protégé Vault** (now up to **100,000 docs per Vault**, accepting audio/video/image); **Protégé Workrooms** (permission-secured collaboration spaces with role-based access + audit trails); **Shepard's Verify Trust Markers** (flags citations that can't be verified as *existing* — note: confirms existence/retrievability, not that authority supports the proposition); and **Protégé BYOK** (bring-your-own encryption key, "deployed in AmLaw 100 firms"). Outputs now export to Word/Excel/PowerPoint/PDF.
- https://www.lawnext.com/2026/05/lexisnexis-expands-lexis-with-protege-adding-agentic-skills-collaboration-workrooms-and-customer-held-encryption-keys.html [R2]
- https://www.law.com/legaltechnews/2026/05/07/lexisnexis-announces-new-security-agentic-ai-updates-to-lexis-with-protg-/ [R2]
- https://www.lexisnexis.com/community/pressroom/b/news/posts/lexisnexis-launches-next-evolution-of-lexis-with-protege-the-legal-ai-platform-built-on-the-authority-legal-work-demands [R1]

**Documented limits (LexisNexis own help pages, via aggregator):** users "limited to 25 Deep Research conversations per month"; uploads 10 files/session, 20MB/file, 2,500–400,000 chars each; up to 50 Vaults at 500 docs each (older limit — superseded by the 100K expansion for Vault). [R3 relaying R1]
- https://www.casefleet.com/blog/legal-ai-pricing-rate-limits-and-overages [R3]

**Pricing.** Custom/quoted, typically bundled into a Lexis+ subscription. Third-party estimates: **~$275/seat/mo** common; Essential tier ~$128, Professional ~$494 (unconfirmed); AI add-on estimated ~$50–150/user/mo on top of base Lexis+. LexisNexis is bundling Protégé access into renewals to make Lexis+ stickier.
- https://www.techno-pulse.com/2026/04/best-ai-legal-tools-in-2026-harvey-ai.html [R3]
- https://www.casefleet.com/blog/legal-ai-pricing-rate-limits-and-overages [R3]

**The dual relationship with Harvey ("integration without access").**
- **Ask LexisNexis (partnership):** A **strategic alliance announced Jun 18, 2025** integrates LexisNexis primary-law content + Shepard's into Harvey via API/RAG. **"Ask LexisNexis" went live in open beta in Harvey on Aug 12, 2025** — natural-language questions returning citation-backed answers from US federal/state case law, statutes, admin codes, agency decisions, with Shepard's validation, without leaving Harvey. Shaped/tested with DLA Piper. LexisNexis framed itself as "the data backbone / AI engine powering legal workflows in other legal AI tools via API." Notably, LexisNexis stated the alliance includes **no cross-selling** of Harvey.
  - https://www.harvey.ai/blog/introducing-ask-lexisnexis [R1]
  - https://www.lexisnexis.com/community/pressroom/b/news/posts/lexisnexis-and-harvey-announce-strategic-alliance-to-integrate-trusted-high-quality-ai-technology-and-legal-content-and-develop-advanced-workflows [R1]
  - https://legaltechnology.com/2025/06/18/lexisnexis-and-harvey-announce-strategic-alliance-in-major-genai-turning-point/ [R2]
  - https://www.lexisnexis.com/community/insights/legal/b/thought-leadership/posts/harvey-lexisnexis-interview-legal-ai-future [R1]
- **Protégé (direct competition):** Simultaneously, LexisNexis competes head-on with Harvey via Protégé. LawNext explicitly lists Protégé's agentic drafting as competing with "Harvey, Spellbook, Legora and DraftWise." So Harvey gets *content-via-API* but LexisNexis keeps its own competing product — the "integration without full access" dynamic. LexisNexis's stated bet: ownership of authoritative content + Shepard's + enterprise controls outweighs newer entrants' product velocity.
  - https://www.lawnext.com/2026/05/lexisnexis-expands-lexis-with-protege-adding-agentic-skills-collaboration-workrooms-and-customer-held-encryption-keys.html [R2]
- **RELX/REV as Harvey investor:** **REV (Rev Ventures), the VC arm of RELX — LexisNexis's publicly-listed parent — is a Harvey investor.** REV joined Harvey's **Series D ($300M, $3B valuation, Feb 2025)** and the **Series E ($300M, $5B valuation, Jun 2025)**, coordinating closely with LexisNexis. LexisNexis publicly explained investing in "a direct competitor," saying the equity stake won't be used to cross-sell and doesn't change Lexis product plans. (RELX had earlier bought Henchman to boost its own AI.)
  - https://www.artificiallawyer.com/2025/02/13/lexisnexis-explains-why-rev-invested-in-rival-harvey/ [R2]
  - https://www.artificiallawyer.com/2025/06/24/lexis-on-revs-new-harvey-funding-workflow-builder/ [R2]
  - https://www.harvey.ai/blog/harvey-raises-series-d [R1]
  - https://www.legaltechnologyhub.com/contents/vc-related-to-lexisnexis-invests-in-harvey/ [R2]

**Strength vs Harvey:** owns Lexis corpus + Shepard's citator; 300+ ready workflows; enterprise controls (BYOK, Workrooms, audit); and it is simultaneously Harvey's content supplier and rival. **Weakness vs Harvey:** Verify checks citation *existence* not support; usage caps (25 Deep Research/mo); positioned as Lexis-shop upgrade rather than firm-agnostic agent platform; product velocity historically trails AI-natives (its own framing).

---

### 3. Westlaw Precision (TR) and Bloomberg Law AI (briefer)

**Westlaw Precision (TR).** The premium Westlaw research tier that hosts CoCounsel; includes Precision search filters, Key Number System, **KeyCite** citation verification, Litigation Analytics, and Practical Law. Public entry pricing (aggregator): **~$155/user/mo single-state (3-yr term)**, ~$266/mo all-states+federal, up to $566+ for AI-enhanced plans; the new **"Advantage" tier adds Deep Research + Litigation Document Analyzer + CoCounsel** and is priced above Edge-with-AI (TR hasn't published exact figures). Positioning vs Harvey: the trusted, litigation-strong research base into which TR is folding AI — bundled, incremental, low-friction for existing Westlaw firms.
- https://ailawyertoolscompared.com/westlaw-ai/ [R3]
- https://dilycode.com/lex-machina-vs-westlaw-edge-vs-bloomberg-law/ [R3]

**Bloomberg Law AI.** Bloomberg Law's **AI Assistant is included free with a subscription** (no add-on fee) — a deliberate pricing contrast to Westlaw/Lexis add-on tiers. A July 15, 2025 release added iterative chat, stored history, jurisdiction filtering, cross-jurisdiction comparison charts, document summaries, and one-click citation verification (**BCite** citator). At Legalweek 2026 Bloomberg previewed **"Intelligent Workspaces"** (combine own docs + Bloomberg content) and **"Deep Thinking" mode** for multi-step reasoning ("Bloomberg Law Answers"). Reviewers consistently rate the AI Assistant **"competent but less mature than CoCounsel or Protégé."** Pricing is sales-quoted; market reports place full Bloomberg Law at **~$200–400/seat/mo — materially below Westlaw or Lexis at comparable depth.** Best fit: financial-services/securities, M&A, regulatory, federal-docket analytics (EDGAR/SEC integration, BLAW Analytics); weak fit: state general practice, contract-first work, or buyers wanting a public API. Positioning vs Harvey: cheapest incumbent entry (AI bundled free), transactional/regulatory-leaning, not a litigation-research leader.
- https://www.vaquill.ai/blog/bloomberg-law-ai-review-honest-assessment-2026 [R3]
- https://lawlessclicks.com/ai-for-law-firms/cocounsel-vs-harvey-ai-bloomberg-law-legal-research-copilot/ [R3]
- https://dilycode.com/lex-machina-vs-westlaw-edge-vs-bloomberg-law/ [R3]

---

### 4. vLex / Fastcase and the Clio ~$1B acquisition (corpus play / consolidation signal)

**The deal.** **Clio (legal practice-management SaaS) acquired vLex for US$1 billion in cash-and-stock — announced Jun 30, 2025, closed Nov 10, 2025** after Spanish regulatory approval. It is the **largest M&A deal in legal-tech history.** Concurrent with close, Clio raised a **$500M Series G led by NEA at a $5B valuation** (plus a $350M debt facility led by Blackstone/Blue Owl), and unveiled Clio Work, Clio for Enterprise, and Vincent Studio (no-code AI tool builder).
- https://www.clio.com/about/press/clio-signs-definitive-agreement-to-acquire-vlex/ [R1]
- https://www.lawnext.com/2025/11/clio-completes-historic-1-billion-vlex-acquisition-announces-500-million-series-g-at-5-billion-valuation-plus-exclusive-interview-with-ceo-and-cfo.html [R2]
- https://www.prnewswire.com/news-releases/clio-completes-landmark-1b-vlex-acquisition-and-announces-500m-series-g-funding-round-at-5b-valuation-302609582.html [R1]
- https://techcrunch.com/2025/06/30/legal-software-company-clio-drops-1b-on-law-data-giant-vlex/ [R2]

**The corpus.** vLex's **Vincent AI** is built on a proprietary global database of **1 billion+ editorially enriched legal documents across 110 jurisdictions** — described as the most comprehensive global legal library. Vincent serves **~2.8 million registered users across 110+ countries** and is used at 8 of the world's 10 largest law firms (though Clio's CEO called Vincent revenue "not that relevant" — "a venture bet"). vLex **merged with US-based Fastcase in 2023**, giving it US reach (1M+ US lawyers); former Fastcase founders Ed Walters and Phil Rosenthal joined. Clio itself serves 200,000+ legal professionals; combined entity branded the "Intelligent Legal Work Platform."
- https://vlex.com/news/vLex-Joins-Clio-in-Landmark-1B-Acquisition-And-Clio-Announces-Series-G-5B-Valuation [R1]
- https://www.theglobeandmail.com/business/article-clio-vlex-acquisition/ [R2]
- https://www.abajournal.com/web/article/clio-buys-vlex-for-1-billion [R2]

**Direct Harvey link (key strategic signal).** **Harvey attempted to acquire vLex first — rumored in 2024 to be raising ~$600M to buy vLex — but the deal fell through; Clio outbid.** After losing vLex, Harvey pivoted to the LexisNexis content alliance (June 2025). This is the clearest evidence of Harvey's corpus gap: it wanted to *own* a database, couldn't, and now rents access. Vincent AI, via Clio's SMB distribution (200K+ firms), becomes a new lower-market competitor.
- https://techcrunch.com/2025/06/30/legal-software-company-clio-drops-1b-on-law-data-giant-vlex/ [R2]
- https://legaltechnology.com/2025/06/18/lexisnexis-and-harvey-announce-strategic-alliance-in-major-genai-turning-point/ [R2]
- https://www.theglobeandmail.com/business/article-clio-vlex-acquisition/ [R2]

---

### 5. Head-to-head vs Harvey — comparisons, the corpus gap, and pricing

**Published three-way / four-way comparisons exist (all R3 comparison blogs, mostly AI-assisted — treat as directional):**
- **Lexis Protégé vs CoCounsel vs Harvey (AI Vortex, Apr 2026):** frames three architectures — Protégé = 300+ pre-built workflows on Lexis content; CoCounsel = multi-model multi-agent Deep Research on Westlaw; Harvey = Agent Builder (cites "$11B valuation, 25,000 custom agents across 1,300 organizations"). Verdict: **"CoCounsel leads on pure legal research (Westlaw = largest curated US corpus); Protégé matches it with Lexis content + Shepard's; Harvey lags on pure research — it doesn't have native access to either Westlaw or Lexis."** Harvey wins on custom workflow agents. Predicts most AmLaw 200 firms deploy ≥2 of the 3 by end-2026.
  - https://www.aivortex.io/legal/agentic-ai/lexis-protege-vs-cocounsel-vs-harvey/ [R3]
- **Harvey vs CoCounsel (GC AI, Jun 2026):** side-by-side. [R3] — https://gc.ai/blog/harvey-vs-cocounsel
- **CoCounsel vs Harvey vs Bloomberg Law (LawlessClicks, Mar 2026):** CoCounsel best for Westlaw-native firms; Harvey premium/enterprise, most customization but most implementation effort; Bloomberg best for transactional. [R3]
  - https://lawlessclicks.com/ai-for-law-firms/cocounsel-vs-harvey-ai-bloomberg-law-legal-research-copilot/ [R3]
- **Harvey vs CoCounsel vs Lexis+ Protégé vs Westlaw Precision (Techno-Pulse, Apr 2026)** and **Best AI Legal Research Tools (Owlesq, May 2026):** feature/pricing matrices (below). [R3]
  - https://www.techno-pulse.com/2026/04/best-ai-legal-tools-in-2026-harvey-ai.html [R3]
  - https://owlesq.com/buyer-guides/best-ai-legal-research-tools-2026 [R3]
- **Lexis+ AI vs Westlaw Precision with CoCounsel (b2bsalestools, Jun 2026):** the two dominant AI-research platforms; corpora (Lexis vs Westlaw) are the real differentiator; costs roughly equivalent ("the choice is platform-fit, not cost"). [R3]
  - https://b2bsalestools.com/compare/lexis-ai-vs-westlaw-precision/ [R3]

**The research-corpus advantage Harvey lacks (the central point).** Multiple independent sources converge: the **licensed, editorially-curated case-law corpus is controlled by the incumbents (Westlaw/TR, LexisNexis, vLex).** Citation-grounded research requires that corpus; independent AI vendors either got acquired (Casetext → TR) or partner for access. Harvey has **no native research database** — it tried to buy vLex (failed), then allied with LexisNexis to rent content (Ask LexisNexis). CoCounsel = Westlaw-grounded; Protégé = Lexis-grounded; Vincent = vLex 1B-doc corpus; Harvey = custom models + partner-supplied content. This is the incumbents' structural moat and Harvey's structural gap.
- https://www.aivortex.io/legal/agentic-ai/lexis-protege-vs-cocounsel-vs-harvey/ [R3]
- https://b2bsalestools.com/compare/lexis-ai-vs-westlaw-precision/ [R3]
- https://techcrunch.com/2025/06/30/legal-software-company-clio-drops-1b-on-law-data-giant-vlex/ [R2]

**Pricing gap (incumbents cheaper/bundled vs Harvey premium).** Consistent across sources — Harvey is the priciest, sold enterprise-only; incumbents are add-ons or bundled:
| Platform | Reported price (third-party) | Notes |
|---|---|---|
| **Harvey** | **~$1,000–1,200/user/mo; ~$288K/yr minimum**; 25–50-seat minimums; enterprise custom | No research-platform subsidy; standalone [R3] |
| CoCounsel | ~$225/user/mo Core; $428 bundled w/ Westlaw; $500 All Access; per-task ~$50–75 | Westlaw-only; all-in $300–600 [R3] |
| Lexis+ Protégé | ~$275/seat; add-on ~$50–150; (Essential ~$128 / Pro ~$494 unconfirmed) | Bundled into Lexis+ renewals [R3] |
| Bloomberg Law AI | ~$200–400/seat; **AI Assistant included free** | Cheapest; AI bundled [R3] |
| Westlaw Precision | ~$155 base → $266 all-states → $428 w/ CoCounsel | Tiered add-on [R3] |
| Vincent (vLex) | Contact vLex / via Clio | Corpus-rich; SMB distribution [R3] |
- https://owlesq.com/buyer-guides/best-ai-legal-research-tools-2026 [R3]
- https://www.techno-pulse.com/2026/04/best-ai-legal-tools-in-2026-harvey-ai.html [R3]
- https://www.casefleet.com/blog/legal-ai-pricing-rate-limits-and-overages [R3]

Common buyer heuristic across guides: *"your existing research platform (Westlaw vs Lexis) decides the research AI; Harvey wins for custom workflow agents; Harvey's economics only work at BigLaw/AmLaw scale."*

---

## Reflection trace

- **Round 1** (2 searches + 1 crawl): Targeted CoCounsel and Protégé — the two biggest incumbents. Searches returned dense trade-press + vendor coverage; the batched crawl (LawNext next-gen CoCounsel, Harvey's Ask-LexisNexis blog, LawNext Protégé expansion, AI Vortex pricing, Westlaw AI guide) resolved capabilities, models, launches, pricing, and the Harvey-partnership mechanics in one pass. Decided Protégé's dual (partner + rival) role and the Claude Agent SDK rebuild were both fully sourced.
- **Round 2** (2 searches + 1 crawl): Filled Bloomberg Law, Westlaw Precision, vLex/Clio, and head-to-head comparisons. Clio/vLex search returned R1 + R2 primary coverage (deal size, close date, corpus, valuation) plus the critical TechCrunch nugget that Harvey tried to buy vLex first. The comparison search surfaced multiple three/four-way blogs; crawl deepened Bloomberg + the three-way + Lexis-vs-Westlaw corpus framing.
- **Round 3** (2 searches, no crawl needed): Two named gaps from the brief — RELX/REV as Harvey investor (confirmed: Series D + E, with LexisNexis's public rationale) and CoCounsel user scale (confirmed: 1M users, Feb 24 2026, 107 countries). Both landed on R1/R2 sources. Stopped: every slice sub-topic corroborated; remaining unknowns (below) are low-value or not obtainable from public sources.
- **Grading posture:** All hard facts (deal sizes, dates, launches, investor rounds, user counts) rest on R1 vendor pages or R2 trade press. All *pricing* and *competitive-verdict* figures are R3 comparison blogs (several AI-assisted, flagged) — surfaced with ranges and conflicts, never as single-point truth. Vendor pages used only for "what they market," not for claims about rivals.

## Gaps and not-found

- **No official rate cards.** None of TR, LexisNexis, Bloomberg, or Harvey publish per-seat pricing; every price here is a third-party estimate (R3). Ranges conflict (esp. CoCounsel tier labels and Harvey's absolute price — $1,000 vs $1,200 vs $288K/yr). Verification-stage should treat all pricing as indicative.
- **CoCounsel 1M = all TR products, not legal-only.** The 1M-user figure spans legal + tax + audit + compliance + trade; TR gave no legal-only or active-vs-licensed breakdown.
- **Vincent (vLex) "2.8M registered users"** is registered, not active/paying; Clio's CEO called Vincent revenue "not that relevant." Adoption depth unclear.
- **Exact model routing** per product (which model handles which task; proprietary-model share) is not disclosed by any vendor — only "multi-model (Anthropic/OpenAI/Google + proprietary)."
- **Bloomberg Law and Westlaw Precision** pricing are the least-sourced (sales-quoted; single R3 estimates each) — sole-source, cap C3.
- **No neutral, methodology-transparent benchmark** (e.g., accuracy/hallucination head-to-head across Harvey vs CoCounsel vs Protégé) was found — all comparisons are qualitative vendor/blog framings.
- **Harvey's own metrics** ($11B valuation, 25K agents, 1,300 orgs, customer counts) appear here only as comparison anchors from R3/R1 Harvey sources; the "harvey-internals" and buyer-TAM slices own verification of those.

## Sources consulted (with grades)

**R1 — vendor/official (authoritative for "what they market"):**
- Harvey blog — Introducing Ask LexisNexis: https://www.harvey.ai/blog/introducing-ask-lexisnexis
- Harvey blog — Series D ($300M, $3B): https://www.harvey.ai/blog/harvey-raises-series-d
- LexisNexis PressRoom — Protégé GA (Feb 24 2026): https://www.lexisnexis.com/community/pressroom/b/news/posts/general-availability-of-lexis-with-protege-sets-new-standard-for-automating-legal-work-with-easy-to-use-authoritative-ai-workflows
- LexisNexis PressRoom — Protégé global launch/preview (Jan 2026): https://www.lexisnexis.com/community/pressroom/b/news/posts/lexisnexis-unveils-global-launch-of-protege-ai-workflows-for-legal-professionals
- LexisNexis PressRoom — Protégé "next evolution" (May 7 2026): https://www.lexisnexis.com/community/pressroom/b/news/posts/lexisnexis-launches-next-evolution-of-lexis-with-protege-the-legal-ai-platform-built-on-the-authority-legal-work-demands
- LexisNexis PressRoom — Harvey strategic alliance (Jun 18 2025): https://www.lexisnexis.com/community/pressroom/b/news/posts/lexisnexis-and-harvey-announce-strategic-alliance-to-integrate-trusted-high-quality-ai-technology-and-legal-content-and-develop-advanced-workflows
- LexisNexis Insights — Q&A on Harvey alliance: https://www.lexisnexis.com/community/insights/legal/b/thought-leadership/posts/harvey-lexisnexis-interview-legal-ai-future
- Clio press — definitive agreement to acquire vLex ($1B): https://www.clio.com/about/press/clio-signs-definitive-agreement-to-acquire-vlex/
- Clio/PRNewswire — deal close + Series G: https://www.prnewswire.com/news-releases/clio-completes-landmark-1b-vlex-acquisition-and-announces-500m-series-g-funding-round-at-5b-valuation-302609582.html
- vLex — Joins Clio ($1B): https://vlex.com/news/vLex-Joins-Clio-in-Landmark-1B-Acquisition-And-Clio-Announces-Series-G-5B-Valuation
- TR/PRNewswire — 1M CoCounsel users: https://www.prnewswire.com/news-releases/one-million-professionals-turn-to-cocounsel-as-thomson-reuters-scales-ai-for-regulated-industries-302694903.html

**R2 — established trade press / news:**
- Law.com — CoCounsel Legal launch (Aug 2025): https://www.law.com/legaltechnews/2025/08/05/thomson-reuters-launches-cocounsel-legal-introduces-westlaw-advantage-with-agentic-ai-deep-research-capabilities/
- Law.com — Next-gen CoCounsel early access (Jun 2026): https://www.law.com/legaltechnews/2026/06/22/thomson-reuters-announces-new-features-early-access-to-next-gen-of-cocounsel-legal-/
- Law.com — Protégé GA (Feb 2026): https://www.law.com/legaltechnews/2026/02/24/lexisnexis-announces-general-availability-of-ai-workflow-platform-lexis-with-protg/
- Law.com — Protégé security/agentic updates (May 2026): https://www.law.com/legaltechnews/2026/05/07/lexisnexis-announces-new-security-agentic-ai-updates-to-lexis-with-protg-/
- LawNext/LawSites — CoCounsel Legal launch: https://www.lawnext.com/2025/08/thomson-reuters-launches-cocounsel-legal-with-agentic-ai-and-deep-research-capabilities-along-with-a-new-and-final-version-of-westlaw.html
- LawNext — Next-gen CoCounsel "F#@%ing loved" (Jun 2026): https://www.lawnext.com/2026/06/thomson-reuters-opens-early-access-to-the-next-generation-of-cocounsel-legal-saying-beta-users-fing-loved-the-product.html
- LawNext — Protégé expansion (May 2026): https://www.lawnext.com/2026/05/lexisnexis-expands-lexis-with-protege-adding-agentic-skills-collaboration-workrooms-and-customer-held-encryption-keys.html
- LawNext — CoCounsel hits 1M users (Feb 2026): https://www.lawnext.com/2026/02/three-years-after-launching-as-first-ai-legal-assistant-cocounsel-reaches-1-million-users-and-thomson-reuters-teases-whats-ahead.html
- LawNext — Clio completes $1B vLex + Series G (Nov 2025): https://www.lawnext.com/2025/11/clio-completes-historic-1-billion-vlex-acquisition-announces-500-million-series-g-at-5-billion-valuation-plus-exclusive-interview-with-ceo-and-cfo.html
- LawNext — Clio buys vLex mega-deal (Jun 2025): https://www.lawnext.com/2025/06/in-a-mega-deal-clio-buys-vlex-for-1-billion-merging-ai-research-and-practice-management.html
- Artificial Lawyer — REV invests in rival Harvey (Feb 2025): https://www.artificiallawyer.com/2025/02/13/lexisnexis-explains-why-rev-invested-in-rival-harvey/
- Artificial Lawyer — REV's new Harvey funding + Workflow Builder (Jun 2025): https://www.artificiallawyer.com/2025/06/24/lexis-on-revs-new-harvey-funding-workflow-builder/
- Artificial Lawyer — CoCounsel 1M users / Claude Crash (Feb 2026): https://www.artificiallawyer.com/2026/02/24/trs-cocounsel-hits-1-millions-users-despite-claude-crash/
- Legal IT Insider — LexisNexis+Harvey alliance / vLex rumor: https://legaltechnology.com/2025/06/18/lexisnexis-and-harvey-announce-strategic-alliance-in-major-genai-turning-point/
- TechCrunch — Clio drops $1B on vLex; Harvey tried to buy vLex: https://techcrunch.com/2025/06/30/legal-software-company-clio-drops-1b-on-law-data-giant-vlex/
- Globe and Mail — Clio buys vLex: https://www.theglobeandmail.com/business/article-clio-vlex-acquisition/
- ABA Journal — Clio buys vLex $1B: https://www.abajournal.com/web/article/clio-buys-vlex-for-1-billion
- TechFundingNews — Harvey Series E $5B (REV participation): https://techfundingnews.com/legal-ai-startup-harvey-300m-series-e-funding-5b-valuation/
- LegalTech.ca — CoCounsel 1M users: https://legaltech.ca/2026/02/24/thomson-reuters-cocounsel-one-million-professionals/
- Finimize — CoCounsel 1M users / stock jump: https://finimize.com/content/thomson-reuters-cocounsel-hit-1-million-users
- Legaltech Hub — VC related to LexisNexis invests in Harvey: https://www.legaltechnologyhub.com/contents/vc-related-to-lexisnexis-invests-in-harvey/

**R3 — comparison / review blogs (several AI-assisted; directional):**
- AI Vortex — Lexis Protégé vs CoCounsel vs Harvey: https://www.aivortex.io/legal/agentic-ai/lexis-protege-vs-cocounsel-vs-harvey/
- AI Vortex — CoCounsel pricing 2026: https://www.aivortex.io/legal/compare/cocounsel-pricing-2026/
- AI Lawyer Tools — Westlaw AI guide: https://ailawyertoolscompared.com/westlaw-ai/
- Vaquill — Bloomberg Law AI review 2026: https://www.vaquill.ai/blog/bloomberg-law-ai-review-honest-assessment-2026
- GC AI — Harvey vs CoCounsel: https://gc.ai/blog/harvey-vs-cocounsel
- b2bsalestools — Lexis+ AI vs Westlaw Precision w/ CoCounsel: https://b2bsalestools.com/compare/lexis-ai-vs-westlaw-precision/
- Owlesq — Best AI legal research tools 2026: https://owlesq.com/buyer-guides/best-ai-legal-research-tools-2026
- Techno-Pulse — Harvey vs CoCounsel vs Protégé vs Westlaw: https://www.techno-pulse.com/2026/04/best-ai-legal-tools-in-2026-harvey-ai.html
- Casefleet — Legal AI pricing / rate limits: https://www.casefleet.com/blog/legal-ai-pricing-rate-limits-and-overages
- LawlessClicks — CoCounsel vs Harvey vs Bloomberg Law: https://lawlessclicks.com/ai-for-law-firms/cocounsel-vs-harvey-ai-bloomberg-law-legal-research-copilot/
- DiLyCode — Lex Machina vs Westlaw Edge vs Bloomberg Law: https://dilycode.com/lex-machina-vs-westlaw-edge-vs-bloomberg-law/
- Spellbook — CoCounsel pricing breakdown: https://spellbook.com/learn/cocounsel-pricing
- Via News — CoCounsel 1M users (built on Claude): https://via.news/technology/thomson-reuters-cocounsel-ai-hits-1-million-users-globally-as-legal-industry
