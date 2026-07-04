---
type: Gather Report
topic: product
slice: marketed-vs-shipped
company: Harvey (harvey.ai)
date: 2026-07-04
rounds_run: 3
stop_reason: 3-round cap reached; named-surface coverage largely exhausted; diminishing returns on new sourced facts
---

# Gather Report — Product surfaces: marketed vs shipped

## Scope

Organize, for each Harvey product surface, (a) what Harvey MARKETS it to do, (b) independent/named-customer evidence of the SHIPPED / generally-available state, and (c) any marketed-vs-shipped gap. Surfaces: Assistant, Vault, Knowledge, Workflows/Workflow Agents, Agents / Agent Builder, Contract Intelligence, Command Center, Shared Spaces, Harvey Mobile, Ecosystem/integrations, Deep Research / reasoning, Memory. Plus reported (non-public) pricing and third-party product reviews of real shipped behavior.

Marketed and shipped are kept explicitly separate. A Harvey marketing/help page is graded **R1 for "what is marketed"** but **WEAK for "what actually ships"**; the shipped claim is graded by its independent evidence. No confidence tags assigned (human assigns final `[F/I/A + NN%]` at write time). Grades shown as `[R·C]`.

Key adversarial probe per brief: Harvey markets "Agents execute legal work end-to-end" and "25,000 custom agents," while its own Legal Agent Benchmark (LAB) uses **all-pass grading** (a task counts only if EVERY rubric criterion passes) and frames agents around "delegate and review" with work that "should remain heavily human-in-the-loop." Findings below separate the marketing verb ("end-to-end") from the shipped reality (review-ready first drafts on high-volume, pattern-matchable work; human retains judgment / novel issues / advocacy).

Disambiguation applied: harvey.ai legal AI / Weinberg & Pereyra only; excluded Harvey Norman / Nichols / Mudd / Specter / hurricane.

---

## Findings

### 1. Assistant (chat / draft / analyze)

- **Marketed** — "Ask questions, analyze documents, and draft faster with domain-specific AI." Nav/body one-liner repeated across all Harvey surfaces. `harvey.ai/platform` [R1·C4 for marketed]. Developer surface exists: Assistant API "enables powerful legal reasoning over your documents and data... natural language queries, document analysis, and grounded legal insights," `developers.harvey.ai/guides/assistant` [R1·C2 marketed]. Vault is "now integrated into Assistant, allowing users to query Vault documents... without switching pages," `harvey.ai/blog/introducing-the-next-version-of-vault` [R1·C2].
- **Shipped evidence** — Multiple independent reviews confirm Assistant is the shipped "front door" and a genuinely legal-tuned chatbot: "the Assistant is Harvey's main chat window... the front door to most of what Harvey can do, and it is the part that feels most like a polished, legal-tuned AI chatbot," eesel AI [R3·C2]. GC AI: "The core interface: an AI chat and drafting tool for questions, document analysis, and clause generation... Output is detailed and structured for firm-style review," `gc.ai` [R3·C2]. tooliverse: "the core workflow centers on the Assistant, which handles everything from contract analysis to deposition summaries without leaving your existing tools" [R3·C2].
- **Gap** — Shipped reality is "first-draft, requires attorney verification," not autonomous. AI For Legal Research: associates report "a first-pass research memo in 20–30 minutes that would previously take 3–4 hours. The memo requires attorney review and typically needs citation verification against Westlaw" [R3·C3]. See §13 (hallucination / human verification) for the corroborated shipped constraint across every independent review.

### 2. Vault (secure doc store, bulk analysis, up to 100k docs)

- **Marketed** — "Securely store, organize, and bulk-analyze legal documents." "A collaborative workspace for large-scale document review, analysis, and synthesis... handle complex matters involving tens of thousands of documents in minutes, not hours or days," `harvey.ai/blog/introducing-the-next-version-of-vault` [R1·C3 marketed]. One-click workflows: "With a single click, users can extract 25+ data points per document," engineered "by our research team of former BigLaw attorneys and AI researchers" [R1·C2 marketed].
- **Shipped evidence** — Vault is the most-validated shipped surface. GC AI (independent) documents the shipped mode structure: Vault "runs in two modes. **Review** returns tabular per-file answers across a document set. **Ask** returns consolidated cross-document answers to a single query. A third mode, **Deep Analysis**, generates comprehensive cited reports across all vault content. Vault syncs with iManage, SharePoint, and Google Drive," `gc.ai` [R3·C2]. Shipped developer/API surface confirms production behavior: Vault API supports upload/manage/delete, files poll to a `ready_to_query` status, and completed review tables expose per-cell "column name, Harvey's short answer (`summary`), the full reasoning (`additional_context`), supporting `citations`, and verification/flag status," with a **10 requests/minute** rate limit, `developers.harvey.ai/guides/vault` [R1·C2]. Named production praise: a "verified Reddit reviewer" said Vault "changed how we handle due diligence... a massive game changer for consistency," via tooliverse [R3·C2]. Ascero attributes the "7-hour average savings on complex document analysis" largely to Vault-style diligence work [R3·C2].
- **Gap** — The "up to 100k docs" ceiling is not confirmed in the marketing copy found (Harvey says "tens of thousands... in minutes"). eesel flags a real shipped limit: "users have noted limits, like a reported cap on documents per Vault, which could be a problem in really big litigation cases" [R3·C2]. **The specific 100k figure was not located in any Harvey page crawled** (see Gaps).

### 3. Knowledge (research across legal / regulatory / tax)

- **Marketed** — "Research complex legal, regulatory, and tax questions across domains." "Access, search, and cite over 100 legal data sources from around the world," `harvey.ai/blog/work-without-boundaries` and `harvey.ai/platform` ("500+ Regional Knowledge Sources" in the "Pull context from" list) [R1·C3 marketed].
- **Shipped evidence** — GC AI: "Research across legal, regulatory, and tax domains... returns synthesized answers with citations" [R3·C2]. Ask LexisNexis is the flagship shipped content layer (see §10). Independent reviewers frame Knowledge/research as a layer on top of Westlaw/Lexis, not a replacement: "Harvey's research capability is not a replacement for Westlaw or Lexis — it's a layer on top of them," AI For Legal Research [R3·C2].
- **Gap** — Data-source count is inconsistent in Harvey's own copy: "over 100 legal data sources" (Work Without Boundaries) vs. "500+ Regional Knowledge Sources" (platform page) vs. "100+ legal knowledge sources, including Wolters Kluwer" (Deep Research blog). Same surface, three different numbers, all R1 marketed.

### 4. Workflows / Workflow Agents (pre-built + custom)

- **Marketed** — "Run pre-built Workflow agents or build your own, tailored to your firm's needs," `harvey.ai/platform` [R1·C3 marketed]. Vault "One-Click Workflows" for common document types, engineered by Harvey's research team [R1·C2 marketed]. The Workflow Engine "expresses our internally-developed AI primitives as low-code, composable blocks," `harvey.ai/blog/integrating-deep-research-into-harvey` [R1·C1 marketed].
- **Shipped evidence** — Paul, Weiss is the public reference: "partnered with Harvey to build out custom AI workflows using Harvey's workflow builder platform... it lets a firm encode its proprietary methodologies... and run them as repeatable Harvey workflows," Ascero [R3·C2]. GC AI (independent) confirms shipped capability: "Harvey's workflow builder lets teams build multi-step automated processes in natural language or through a visual interface, with no code required. Conditionals, classification, role-based permissions, and external partner sharing are all supported" [R3·C2].
- **Gap** — Ascero's framing of what the workflow platform actually is: "Harvey is not selling a model. It is selling a workflow platform with a model underneath it," and workflows are "explicitly the answer to [hallucination] — constrain the model to firm-validated procedures rather than open-ended queries" [R3·C2]. i.e., the shipped strength is constrained, firm-validated automation, not open-ended autonomy.

### 5. Agents / Agent Builder (500+ prebuilt, 25,000+ custom; ad-hoc / pre-built / custom)

- **Marketed** — "Purpose built agents execute complex legal work end to end" / "Harvey Agents execute legal work end-to-end, so you can focus on what only lawyers can do." Three modes: **Ad Hoc** ("Describe what you need. Harvey plans, does the work, and delivers... a review-ready deliverable, fully cited"), **Pre-Built** ("500+ ready-to-use agents vetted by Harvey's lawyers"), **Custom** (Agent Builder: "takes your templates, your steps, and your standards and turns them into a custom agent"). Five-stage loop Plan → Research → Work → Deliver → Review, `harvey.ai/agents` [R1·C4 marketed]. Agent Builder = "evolving Workflow Builder into Agent Builder... Harvey is agentic by design," `harvey.ai/blog/introducing-agent-builder` (Mar 9, 2026) [R1·C2 marketed]. Launch: "500+ use case Agents are live in the platform alongside the company's Agent Builder tool **in early access**," `harvey.ai/blog/built-by-lawyers-tailored-by-you` (May 5, 2026) [R1·C2] and Law.com "currently available in early access" (May 5, 2026) [R2·C2].
- **Shipped evidence (throughput / adoption)** — Harvey-sourced production numbers: **700k+ daily tasks** run using agents; **50M terms extracted weekly**; **5.8M+ documents analyzed daily** (`harvey.ai/agents`) [R1·C2]; separately, the Agent Builder blog reports **400K+ agentic queries daily**, **20M+ terms in review tables**, **445K+ reports created with agentic Deep Analysis**, and **"over 25,000 agentic custom workflows" built with Workflow Builder** [R1·C2]. Independent corroboration: "the platform behind 700,000+ daily AI tasks across 1,300 organizations, with 25,000 custom agents... 100,000 lawyers running these agents daily. That's not aspirational marketing — it's current throughput," AI Vortex [R3·C2].
- **Shipped evidence (named production use)** — A&O Shearman ran agents in production across **antitrust screening, cybersecurity compliance, fund formation, and loan review** ("These aren't demo-day experiments. They're production workflows handling real client work"), AI Vortex [R3·C2]. Harvey-named customer outcomes: **Ashurst** "saves hours on producing lease summaries"; **GSK Stockmann** "built their own agentic workflows to speed up due diligence reviews," `introducing-agent-builder` [R1·C2]. Additional named agent adopters (Harvey's own /agents page, first-party testimonials): Willkie Farr & Gallagher, Gowling WLG, Clayton Utz, Mallesons ("one of the earliest adopters of Harvey's Agent Builder"), Hengeler Mueller [R1·C2].
- **Marketed-vs-shipped gap (the core tension)** —
  - Even Harvey's own marketing bakes in the human: "Delegate the Work. **Own the Judgment.** Agents research, draft, and analyze. **You make the call**"; Agent Builder "designed with **human-in-the-loop checkpoints as a core feature**," and a running agent "can then ask the user to confirm whether... it should proceed" [R1·C3].
  - Independent: "the pattern is consistent: **Harvey agents handle the volume work, human lawyers handle the judgment calls**... Firms report strong results for structured analysis tasks (contract review, document comparison) but **still require human review for judgment-intensive work. ABA Opinion 512 requires lawyer supervision regardless**," AI Vortex [R3·C2]. Weaker "on novel legal questions with no precedent... less reliable when the answer requires creative legal reasoning that doesn't exist in the training data" [R3·C2]. Ascero: agents do "not... replace lawyer judgment on novel issues, court advocacy, or strategy work"; Latham explicitly did NOT deploy Harvey for "advocacy, oral argument preparation, novel-issue legal strategy, or client counsel... partner-only tasks at every firm in the disclosed customer list" [R3·C2].
  - "500+ prebuilt" vs "25,000 custom" are two distinct things: ~500+ Harvey-built/vetted prebuilt agents vs. ~25,000 customer-built custom workflows. The "25,000" accrued during Agent Builder's **early-access** period (GA state of Agent Builder itself is early access as of May 2026).
- **Note (competitor-promotional claim now stale)** — RAGbase (Feb 27, 2026) asserted "No custom AI agents for your workflows. Harvey is a general-purpose tool" [R4·C1]. This was contradicted within ~2 weeks by Agent Builder (Mar 9) and later the Connector Library (June). Treat RAGbase's "what you don't get" list as a dated competitor sales piece, not current shipped state.

### 6. Contract Intelligence (launched ~May 2026)

- **Marketed** — "Surface insights, strengthen negotiations, and accelerate reviews." Announced May 21, 2026 as "a system for in-house teams to manage every contract flowing through their business... Built in close collaboration with a cohort of design partners... adapts to each team's playbooks, risk appetite, and negotiation patterns." Three pillars: accelerate intake/triage/review; negotiate from prior work product ("Every signed contract updates your playbooks automatically"); portfolio-wide visibility, `harvey.ai/blog/introducing-contract-intelligence` [R1·C2 marketed]. Follow-up explainer `harvey.ai/blog/contract-intelligence` (Jun 30, 2026) [R1·C1].
- **Shipped evidence** — Coverage confirms the announcement: "Harvey Announces Contract Review Product, Adoption Analytics Features," Law.com (May 21, 2026) [R2·C2]. But shipped state is **design-partner / waitlist, not GA**: "Our design partners are shaping every part of Contract Intelligence... We'll continue to bring more customers into this process as the product evolves. **Join the waitlist**" [R1·C2].
- **Gap** — The sole customer testimonial on the launch page is from **John LaBarre, "General Counsel at Harvey"** — i.e., Harvey's own in-house GC, not an external customer ("a real force multiplier that saves us hours on every single contract") [R1·C2]. Internal endorsement presented as product proof; no independent named-customer usage located. Product is not generally available as of the sources gathered.

### 7. Command Center (adoption analytics)

- **Marketed** — "Analytics, benchmarking, and agentic insights to lead their organization's AI transformation." "The intelligence layer for your Harvey deployment... transparency into usage, agentic insights, and intelligent recommendations." Features: usage breakdown by practice group/product area; **peer benchmarking** "built on anonymized data from Harvey's 1,500+ deployments globally"; a natural-language "Command Center agent"; Intelligent Recommendations; new-releases section. Built with design partners at Foley Lardner, Rajah & Tann, Haynes Boone, Fisher Phillips, Dentsu, Vinge, Mallesons, `harvey.ai/blog/introducing-command-center` (May 20, 2026) [R1·C2 marketed].
- **Shipped evidence** — Independent coverage: "Command Center gives organizations visibility into how Harvey is being used across practice groups, offices, product areas, and user cohorts," Artificial Lawyer (May 20, 2026) [R2·C2]; LawSites/LawNext (May 20, 2026) [R2·C2].
- **Gap** — **Early Access / waitlist, not GA**: "Command Center is available now to a limited group of customers through **Early Access. Sign up to join the waitlist**" [R1·C2].

### 8. Shared Spaces (cross-org collaboration)

- **Marketed** — "Work with legal teams across organizations in secure, shared spaces." Dedicated page: "brings firms, clients, and their teams into a single AI-powered environment protected by the governance and ethical walls that sensitive legal work demands... Share Vaults, co-build work product, and run workflows." Governance: resource-level (not just space-level) permissions, Intapp integration enforcing ethical walls, real-time audit logs, `harvey.ai/platform/shared-spaces` and `harvey.ai/blog/shared-spaces-and-collaboration-in-harvey` [R1·C3 marketed].
- **Shipped evidence** — Rollout timeline is documented by Harvey: opened access in December (2025) to design partners; "Shared Spaces is **live in early access** with organizations around the world, with **general availability expected in March** [2026]," `harvey.ai/blog/a-new-era-of-collaboration-for-legal-and-professional-services` [R1·C2]. The Brief: May 2026 lists shipped increments — external-partner access without full Harvey licenses, Space Analytics, External Collaboration Management governance/audit layer [R1·C2].
- **Gap** — Guest accounts framed as future ("Shared Spaces **will also support** guest accounts") [R1·C2]. GA target of "March" is Harvey-stated; no independent confirmation of GA date located.

### 9. Harvey Mobile

- **Marketed** — "Get up to speed, capture new information, and keep work moving from anywhere." "Harvey's mobile app brings the power of the platform to your phone or tablet... Ask questions using dictation... Scan and upload documents from a client meeting," `harvey.ai/blog/work-without-boundaries` [R1·C2 marketed].
- **Shipped evidence** — GC AI (independent): "A **mobile app launched in September 2025** with voice-to-prompt and document scanning" [R3·C2]. Help release notes confirm shipped mobile increments: "Deep Analysis is now available on Android" [R1·C2]. The Brief: May 2026 references "a more capable mobile experience" [R1·C1].
- **Gap** — None material; mobile is shipped and dated. Depth of real usage not independently quantified.

### 10. Ecosystem / integrations

- **Marketed** — "Access Harvey where you already work and ground every answer in sources you trust." Platform page "Use Harvey in:" Word, Outlook, iManage, Web Browsers, Email, Mobile; "Pull context from:" Ask LexisNexis, Rettsdata, iManage, NetDocuments, SharePoint, Google Drive, Aderant, Ironclad, APIs [R1·C3 marketed].
- **Shipped evidence (dated, GA or early access)** —
  - **Microsoft Word Add-In**: "now available to all Harvey customers" — generally available, `harvey.ai/blog/announcing-harvey-integrations-with-microsoft` (Dec 5, 2024) [R1·C2]. Confirmed by every independent review as a shipped, core feature [R3·C3].
  - **Microsoft 365 Copilot / SharePoint / Cowork**: M365 Copilot routing "generally available by the end of the year" (stated Dec 2024); SharePoint direct upload "now generally available"; help notes "Use Harvey inside Microsoft 365 Copilot and Cowork," `harvey.ai/blog/agent-platform-and-microsoft-365-copilot` (Mar 4, 2026) + release notes [R1·C2].
  - **Ask LexisNexis**: shipped Aug 12, 2025 — "submit legal questions in natural language and get AI-driven, citation-backed answers from LexisNexis," `harvey.ai/blog/introducing-ask-lexisnexis` [R1·C2]. Reported as a paid add-on (~$400–600/lawyer/yr, Ascero [R3·C2]; a "LexisNexis-bundled seat near $2,400," Vaquill [R3·C2]).
  - **Connector Library**: "Starting mid-June in **Early Access** for select Harvey customers" — native API to Google Drive and Gmail; MCP integrations to iManage, NetDocuments, PitchBook, SS&C Intralinks DealCentre AI, Datasite, and Box, `harvey.ai/blog/connector-library` (Jun 8, 2026) [R1·C2].
  - **Datasite**: integration announced Jun 9, 2026 — deal-room data "directly within Harvey's Assistant, Vault, Workflow Builder, and Word Add-In," with permissions carried over, `harvey.ai/blog/harvey-partners-with-datasite` [R1·C2].
  - **DeepJudge**: partnership announced May 20, 2026 to bring institutional intelligence into Harvey workflows, `harvey.ai/blog/deepjudge-and-harvey-partner` [R1·C2] + Artificial Lawyer / LawNext [R2·C2]. (Partnership announcement; shipped/GA depth not established.)
  - **Box** integration "shipped in 2026," GC AI [R3·C2].
  - **Intapp** (conflicts / ethical walls): partnership referenced as the enforcement layer for Shared Spaces and agent ethical walls, `harvey.ai/blog/long-horizon-agents-and-ethical-walls` [R1·C2].
- **Gap** — Most 2026 connectors are **Early Access for select customers**, not GA. Note a competitor (RAGbase, Feb 2026) claimed "No deep integration with your internal data... It works with what you feed it, session by session" [R4·C1] — a claim superseded by the Connector Library. Independent reviews still caution the DMS-grounding is real but was recent: "deep integrations into iManage, NetDocuments, and Microsoft 365," Plain AI [R3·C2].

### 11. Deep Research / reasoning modes

- **Marketed** — Two distinct things carry "deep" naming:
  1. **Agentic search + Deep Analysis** ("New Reasoning Capabilities"): "agentic document search, multi-source querying, and deep analysis across internal and external data... Harvey's most advanced mode for complex, multi-source legal analysis and reports," `harvey.ai/blog/introducing-harvey-deep-research` [R1·C2 marketed].
  2. **OpenAI Deep Research integration**: "integrating Deep Research within Harvey less than 12 hours after it was released by OpenAI," `harvey.ai/blog/integrating-deep-research-into-harvey` [R1·C2 marketed].
- **Shipped evidence** — The reasoning/Deep Analysis capability is stated GA: "They're **available now to all Harvey customers** from within your account" [R1·C2]; GC AI documents "Deep Analysis... generates comprehensive cited reports across all vault content" as a shipped Vault mode [R3·C2]; Harvey reports "445K+ reports created with agentic Deep Analysis" [R1·C2].
- **Gap** — The **OpenAI Deep Research** integration specifically was **not yet GA** at its blog date: "This feature is currently undergoing **internal testing** and will be available more broadly soon, starting with an **early access** period" [R1·C2]. So "Deep Research" spans one shipped/GA reasoning surface (agentic search / Deep Analysis) and one then-in-testing integration — worth not conflating.

### 12. Memory (in fine-tuning / working context)

- **Marketed** — "Harvey is inviting customers to help shape Memory, bringing your preferred working style, matter context, and best practices into every AI output." "Memory will carry forward the context you choose — matter details, relevant precedent, working preferences, and approved best practices," `harvey.ai/blog/memory-in-harvey` (Jan 8, 2026) [R1·C2 marketed]. LAB blog lists "memory" among research directions the benchmark enables [R1·C1].
- **Shipped evidence** — **None located; Memory is pre-product.** The announcement is explicitly a co-build/roadmap invitation: "we're **co-building** Memory in Harvey with the industry. Over the coming months, we'll host customer listening tours and working sessions... **As an example of how this could work**, when memory is enabled, Harvey **could** use past threads..." [R1·C2].
- **Gap** — Strongest marketed-vs-shipped gap of any surface: Memory is a design-phase concept described in conditional/future tense ("could," "we envision a future where..."), not a shipped feature. Do not treat as available.

### 13. Cross-cutting shipped reality: hallucination & mandatory human verification

Every independent review converges on the same shipped constraint, which tempers the "end-to-end" marketing:
- "Every citation Harvey produces **must be independently verified**... Firms that skip this step are not saving time. They are accumulating malpractice exposure," Legal Intaker [R3·C2] (cites Mata v. Avianca sanctions).
- "Stanford research shows legal AI hallucination rates of **6-33%**. Always verify every case citation... treat every AI output as a draft that requires human verification," AI Vortex (does-harvey-hallucinate) [R3·C2].
- tooliverse "consensus": "requires rigorous human verification due to occasional legal citation hallucinations — **mentioned in 62 reviews**" [R3·C3].
- toolsforhumans: "every output still requires substantive human verification before it goes anywhere near a client... functions as a first-pass accelerator, not a verification tool" [R3·C2].
- Lawyerist and AI For Legal Research: "Attorneys should still verify cited authorities... Attorney verification is non-negotiable. Harvey's enterprise customers uniformly treat Harvey output as a first draft that requires attorney review" [R3·C3].
- Harvey co-founder Gabriel Pereyra "has acknowledged the platform is **not at zero** [on hallucination]," Ascero [R3·C2]. Harvey publishes no independent accuracy benchmark; the LAB benchmark deliberately launched **without a leaderboard** and model results were "to be published in the coming weeks" (not present at page date).

### 14. LAB benchmark — Harvey's own framing of agent limits

- `harvey.ai/blog/introducing-harveys-legal-agent-benchmark` (May 6, 2026) [R1·C2]: 1,200+ (1,250) agent tasks, 24 practice areas, 75,000+ expert rubric criteria. **All-pass grading**: "a task is marked complete only if every criterion passes... A deal-team report that identifies eight of ten risks is not 80% useful; **it is materially incomplete**." Harvey frames LAB as telling firms "which parts of a workflow can be delegated to agents, **where lawyer review matters most, and what capabilities still need to improve**," and where execution "**should remain heavily human-in-the-loop**."
- Relevance to the probe: this is Harvey's own instrument acknowledging that long-horizon agents do NOT reliably complete tasks end-to-end under all-pass grading. **The specific "<10% end-to-end / single-digit all-pass" completion figure from the tasking was NOT found in the sources gathered** — the benchmark page states baseline model results were still forthcoming and launched without a leaderboard (see Gaps).

### 15. Pricing / packaging (no public pricing)

- **Marketed** — Harvey publishes **no pricing and no free trial**; "as of June 2026 there is no pricing page on its website. A demo request is the entry point," GC AI [R3·C2]. Confirmed by all independent sources.
- **Reported (independent, non-Harvey)** — Strong convergence on ~**$1,000–1,200/seat/month, 20-seat minimum, 12-month term, ~$240K–288K/yr floor**: RAGbase ($1,000–1,200/mo, 20 seats, 12 mo, $240–288K) [R4·C2]; Plain AI (~$1,000–1,200, 20-seat, $288K) [R3·C2]; jimmyresearch ($1,000–1,200/lawyer/mo, ~20-seat min) [R3·C2]; Vaquill (founder-confirmed $500–1,500 range; leaked base ~$1,200 and **LexisNexis-bundled seat ~$2,400**, ~$288K/yr floor) [R3·C2]; Ascero ($1,000–1,200/mo = $12K–16.8K/seat/yr; premium bundles $15.6K–16.8K/seat/yr; 25–50+ seat minimums; $300K floor, mid-market $500K–2M+) [R3·C2]; firmtools ($1,200–2,000/seat/mo) [R3·C2]; thelegalprompts ($1,000–2,000/seat/mo mid-market) [R3·C3]. **Outlier:** AI Vortex estimates "$75–200+ per user per month" [R3·C1] — roughly an order of magnitude below every other estimate; flag as inconsistent.
- **Scale / traction figures** (context; funding/traction owned by sibling dossier — captured only where they evidence shipped product usage): Harvey platform page — 142,000 legal professionals, 200K+ queries/day, 1.3M+ files/day, 92% avg monthly usage [R1·C1]; ~$190M ARR & ~100,000 lawyers (RAGbase) / $100M ARR Aug 2025 (Ascero) [R3/R4·C2]; ~50% of Am Law 100 (Ascero) / 42% (toolsforhumans) / 65+ AmLaw 100, 200K queries/day (tooliverse) [R3·C2]; 1,500+ customers, 60+ countries (Harvey/DeepJudge blog) [R1·C2]. A&O (firm-disclosed, not independently audited): 2–3 hrs saved/week/lawyer, 30% contract-review-time reduction, 7-hr savings on complex doc analysis, 1-in-4 daily / 80% monthly, 4,000+ lawyers across 43 jurisdictions (Ascero) [R3·C2].

---

## Reflection trace

- **Round 1** — 2 Exa searches (product-surface overview; Agent Builder / Contract Intelligence / case studies) + 1 batched crawl of 6 pages (harvey.ai/platform, /agents, gc.ai review, asceroai deployment data, aivortex Agent Builder review, introducing-agent-builder). Crawl exceeded inline token limit; delegated full read/extraction to a subagent. Yielded: marketed one-liners for all surfaces; shipped throughput (700k/400k daily tasks, 25k custom workflows, 445k Deep Analysis reports); named production use (A&O four practice areas, Ashurst lease summaries, GSK Stockmann diligence, Paul Weiss workflows); the human-in-the-loop gap language from Harvey itself and from AI Vortex/Ascero.
- **Round 2** — 2 Exa searches (Contract Intelligence/Command Center/integrations; pricing/LAB/limitations) + 1 batched crawl (LAB benchmark, long-horizon-agents, introducing-contract-intelligence, RAGbase pricing). Established: all-pass grading and the "materially incomplete" framing; Contract Intelligence + Command Center as Early Access/waitlist; ethical-walls / matter-isolation constraints on agent autonomy; convergent pricing ($1,000–1,200/seat, 20-seat, $288K floor); the stale RAGbase "no custom agents / no deep integration" claim.
- **Round 3** — 2 Exa searches (Deep Research/Shared Spaces/Memory/M365; help-center limitations/hallucination/G2). Closed surfaces: Deep Research split (GA reasoning vs. in-testing OpenAI integration); Shared Spaces (early access, GA "expected March"); Memory (pre-product co-build); Word Add-In GA (Dec 2024) + M365 Copilot; Vault API shipped behavior (developers.harvey.ai); and the unanimous "every output requires attorney verification" shipped reality (Legal Intaker, Lawyerist, AI For Legal Research, eesel, toolsforhumans, tooliverse, AI Vortex).
- **Stop decision** — Hit the 3-round cap with every named surface covered by ≥1 R1 marketed source and, for most, ≥1 independent shipped source; new searches were returning the same pricing/hallucination facts (diminishing returns). Stopped.

## Gaps and not-found

- **The "<10% end-to-end / single-digit all-pass" LAB completion figure was not located.** The LAB launch blog (May 6, 2026) intentionally shipped without a leaderboard and said baseline model results were forthcoming "in the coming weeks." A later leaderboard/results post (or a third-party writeup of LAB scores) would confirm the single-digit figure; not found in this pass. What IS documented is Harvey's all-pass grading methodology and its explicit "heavily human-in-the-loop" framing.
- **Vault "up to 100k docs" ceiling** — the specific 100,000-document figure was not found in any Harvey page crawled (Harvey says "tens of thousands... in minutes"). eesel notes a "reported cap on documents per Vault" without a number.
- **G2 rating/reviews** — no G2 page surfaced; the closest structured "review consensus" is tooliverse ("62 reviews" on hallucination, "48 reviews" on pricing) and Reddit-sourced quotes. A dedicated G2/Capterra listing was not located.
- **Contract Intelligence & Command Center independent named-customer usage** — only Harvey design-partner lists and the internal (Harvey GC) testimonial found; both are Early Access/waitlist, so real third-party shipped reviews likely do not yet exist.
- **DeepJudge & Datasite shipped depth** — announced as partnerships/integrations (May–Jun 2026); no independent evidence of production usage or GA scope beyond the announcements.
- **Metric inconsistencies across Harvey's own pages** (flag for the verification pass, not resolvable here): daily agent activity stated as "700k+ daily tasks" (/agents) vs "400K+ agentic queries daily" (Agent Builder blog); "50M terms/week" (/agents) vs "20M+ terms in review tables" (blog); "142,000 legal professionals" (platform) vs "100,000 lawyers" (Ascero/AI Vortex). Different definitions/dates, all R1/R3.
- **Spellbook head-to-head comparison** describing Harvey's shipped behavior was referenced only via pricing tables (jimmyresearch, RAGbase) — no substantive Spellbook-vs-Harvey feature review of real behavior located.

## Sources consulted, with grades

Harvey official (R1 for **marketed**; weak for **shipped**):
- harvey.ai/platform — marketed one-liners + platform stats (142k pros, 200K queries/day, 1.3M files/day) [R1]
- harvey.ai/agents — agent modes, five-stage loop, 700k tasks/50M terms/5.8M docs, named testimonials [R1]
- harvey.ai/blog/introducing-agent-builder (Mar 9 2026) — 400K queries/day, 20M terms, 445K Deep Analysis reports, 25k workflows, human-in-the-loop, scheduling=future [R1]
- harvey.ai/blog/built-by-lawyers-tailored-by-you (May 5 2026) — 500+ agents live, Agent Builder early access [R1]
- harvey.ai/blog/introducing-the-next-version-of-vault — one-click workflows, 25+ data points/doc, Vault-in-Assistant [R1]
- harvey.ai/blog/introducing-contract-intelligence (May 21 2026) — design partners, waitlist; internal GC testimonial [R1]
- harvey.ai/blog/contract-intelligence (Jun 30 2026) [R1]
- harvey.ai/blog/introducing-command-center (May 20 2026) — Early Access/waitlist, peer benchmarking on 1,500+ deployments [R1]
- harvey.ai/blog/connector-library (Jun 8 2026) — mid-June Early Access; iManage/NetDocuments/Box/Datasite/Intralinks/PitchBook MCP [R1]
- harvey.ai/blog/harvey-partners-with-datasite (Jun 9 2026) [R1]
- harvey.ai/blog/deepjudge-and-harvey-partner (May 20 2026) — 1,500+ customers/60+ countries [R1]
- harvey.ai/blog/introducing-ask-lexisnexis (Aug 12 2025) [R1]
- harvey.ai/blog/introducing-harveys-legal-agent-benchmark (May 6 2026) — LAB, all-pass grading, no leaderboard [R1]
- harvey.ai/blog/long-horizon-agents-and-ethical-walls (Mar 12 2026) — agent autonomy vs. ethical walls, matter-isolation [R1]
- harvey.ai/blog/introducing-harvey-deep-research ("New Reasoning Capabilities") — agentic search + Deep Analysis GA to all customers [R1]
- harvey.ai/blog/integrating-deep-research-into-harvey — OpenAI Deep Research integration in internal testing/early access [R1]
- harvey.ai/blog/memory-in-harvey (Jan 8 2026) — co-build/roadmap, not shipped [R1]
- harvey.ai/platform/shared-spaces + harvey.ai/blog/shared-spaces-and-collaboration-in-harvey + a-new-era-of-collaboration (GA "expected March") [R1]
- harvey.ai/blog/announcing-harvey-integrations-with-microsoft (Dec 5 2024) — Word Add-In GA, M365 Copilot [R1]
- harvey.ai/blog/agent-platform-and-microsoft-365-copilot (Mar 4 2026) [R1]
- harvey.ai/blog/work-without-boundaries — mobile, iManage, external sharing [R1]
- harvey.ai/blog/the-brief-may-2026 — Shared Spaces increments, Space Analytics [R1]
- help.harvey.ai/release-notes; help.harvey.ai/articles/getting-started-with-harvey — Deep Analysis on Android, M365 Copilot/Cowork [R1]
- developers.harvey.ai/guides/vault — Vault API shipped surface (ready_to_query, review tables, 10 req/min) [R1]
- developers.harvey.ai/guides/assistant — Assistant API shipped surface [R1]
- harvey.ai/blog/wkb-lawyers-deploys-harvey-firmwide (Jun 23 2026) — named firmwide deployment [R1]

Established trade press (R2 for shipped/announcements):
- law.com/legaltechnews — "Harvey Launches Pre-Built AI Agents... early access" (May 5 2026); "Harvey Announces Contract Review Product, Adoption Analytics" (May 21 2026) [R2]
- artificiallawyer.com — Command Center + DeepJudge (May 20 2026) [R2]
- lawnext.com (LawSites) — Command Center + DeepJudge (May 20 2026) [R2]
- lawyerist.com — Harvey review, human-verification framing (Jun 2 2026) [R2/R3]

Independent reviews / analysis (R3 for shipped behavior):
- gc.ai/blog/harvey-legal-ai-review (May 29 2026) — four core products, Vault Review/Ask/Deep Analysis modes, no public pricing/no trial (COMPETITOR; some GC-AI-favorable framing) [R3]
- asceroai.com/news/harvey-big-law-ai-2026-deployment-data (May 28 2026) — A&O/PwC/Paul Weiss/Latham/KKR deployments, firm-disclosed productivity, skeptical caveats, pricing bands [R3]
- aivortex.io Agent Builder Review (Apr 17 2026) — 700k tasks/25k agents/100k lawyers, A&O four practice areas, human-review gap, ABA 512; pricing OUTLIER ($75–200/user/mo) [R3]
- aivortex.io does-harvey-ai-hallucinate (Apr 17 2026) — Stanford 6–33%, verify every citation [R3]
- eesel.ai/blog/harvey-ai-review (Nov 5 2025) — Assistant/Vault/Knowledge/Agents tour; Vault doc-cap limit; agents "marketed... end to end" [R3]
- toolsforhumans.ai/ai-tools/harvey-ai — 42% AmLaw 100, accuracy gaps, mandatory human verification, thin community signal [R3]
- tooliverse.ai/tools/harvey (Dec 10 2025) — 200k queries/day, 65+ AmLaw 100, 62-review hallucination consensus, 20-seat min [R3]
- aiforlegalresearch.com/tools/harvey-ai — RAG grounding, first-pass memo 20–30 min, verify; layer on Westlaw/Lexis [R3]
- legalintaker.com/blog/harvey-ai (Apr 29 2026) — human review, Mata v. Avianca, governance requirements [R3]
- agent-finder.co/reviews/harvey-ai-review (May 22 2026) — 40+ practice areas, 15,000 lawyers (May 2026), enterprise-only [R3]
- vaquill.ai/blog/harvey-ai-price-increase-per-seat (Jun 3 2026) — founder-confirmed $500–1,500; leaked $1,200 base / $2,400 Lexis-bundled; 20-seat/12-mo [R3]
- plainai.tech honest Harvey review (Spring 2026) — $1,000–1,200/seat, 20-seat, $288K, iManage/NetDocuments/M365 [R3]
- jimmyresearch.com/entities/harvey (May 10 2026) — surface list, pricing/token economics, competitor matrix [R3]
- firmtools.ai/harvey-ai (Apr 2 2026) — pricing $1,200–2,000/seat, workflow definition [R3]
- thelegalprompts.com/blog/harvey-ai-alternatives-2026 (Jul 1 2026) — pricing range $1,000–2,000 mid-market [R3]

Promotional / competitor sales content (R4; use with caution):
- ragbase.ai/blog/harvey-pricing-breakdown (Feb 27 2026) — pricing table + "$190M ARR/100k lawyers"; "what you don't get" claims (no custom agents / no deep integration) now stale/superseded [R4]
