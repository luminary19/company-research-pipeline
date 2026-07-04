---
type: Gather Report
topic: people
slice: hiring-culture
date: 2026-07-04
rounds_run: 3
stop_reason: >-
  Reached the 3-round cap with all five sub-questions saturated. First-party
  Harvey careers pages supplied role/comp facts and the values/AI-in-recruiting
  language; techinterview.org + Glassdoor/Levels/Blind + jobsbyculture supplied
  the interview loop and sentiment; the Weinberg "re-earn your role" quote was
  corroborated to primary sources (Fortune + Sequoia podcast verbatim). Round-3
  searches largely re-surfaced already-captured role pages, signalling
  diminishing marginal return.
---

# Gather Report — People / Hiring-as-Signal + Engineering Culture (Harvey, harvey.ai)

## Scope

Public-professional signal ONLY, weighted for a reader preparing for a Harvey
**engineering** interview. Covers: (1) open-roles-as-signal, (2) compensation,
(3) engineering culture, (4) public employee sentiment, (5) the interview
process. Disambiguation: Harvey = harvey.ai, the legal/professional-services
vertical-AI platform (Winston Weinberg / Gabriel Pereyra, 2022), NOT any
same-named person or product.

Organized, not concluded. Every finding carries an openable URL and an [R·C]
grade (R1 = Harvey first-party; R2 = established coverage; R3 = jobsbyculture /
techinterview.org / Glassdoor-aggregate / Levels.fyi; R4 = anonymous single
post → weak signal only. Sole-source caps confidence at C3). Final [F/I/A + NN%]
tags are the human's to assign at write time; none appear here.

EXCLUDED (sibling "leadership-org" slice owns): exec roster / org chart; buyer
personas; competitor org internals.

---

## Findings

### 1. Open-roles analysis (hiring-as-signal)

**Aggregate open-role volume.** Third-party job aggregators counted roughly
**255–292 open roles** across engineering, product, sales, and legal engineering
in mid-2026, refreshed daily from Harvey's Ashby-hosted careers page. jobsbyculture
reports "255 open roles across departments" [R3·C3]
(https://jobsbyculture.com/companies/harvey); Built In's Harvey profile shows
"View All 292 Jobs at Harvey" [R3·C3]
(https://builtin.com/company/harvey/faq/work-life-balance-wellbeing). Harvey's
own careers board did not crawl (CRAWL_NOT_FOUND on
https://www.harvey.ai/company/careers), so a first-party total is not captured —
see Gaps.

**Engineering roles actively posted (first-party harvey.ai/company/careers), with the "hiring-as-signal" read each role gives off:**

- **AI Platform — Senior ($220–300K) and Staff ($231–340K).** Explicitly framed
  as an EARLY team: "This team is early and there's a lot to build: model
  routing, agent architecture, context management, evals. Your work here sets
  the ceiling for what Harvey's AI can do." Signal: the shared model/agent
  foundation layer is still being stood up. [R1·C4]
  (https://www.harvey.ai/company/careers/f7c8e800-c0e4-4606-9860-9822103fe7e4 ;
  https://www.harvey.ai/company/careers/51fb953a-c494-4a09-8fe2-8d7268b863ec)
- **Core Infrastructure — Senior ($200–250K, 4+ YoE) and Staff ($231–340K, 10+ YoE).**
  "processing billions of prompt tokens and millions of daily requests";
  multi-cloud **Azure (preferred) + GCP**, Kubernetes, Terraform/Pulumi,
  Datadog/Sentry/PagerDuty/Incident.io, distributed rate-limiting/quota/failover.
  Signal: scaling + reliability hardening of a live global platform. [R1·C4]
  (https://www.harvey.ai/company/careers/4a82c276-1113-41f6-baf9-a5be27e5c78f ;
  https://www.harvey.ai/company/careers/748edfbe-f819-47fd-85bb-3c4974f8913f)
- **Backend (Product Engineering) — Staff ($231–340K, 10+ YoE).** "What You'll
  Do" bullets read as a capability manifesto: "Retrieval over peta-byte scale
  documents… Managing dedicated GPU capacity across 5+ regions… 1000-step
  planning agents that help take companies public… Evaluating LLMs across a
  10k+ leaf taxonomy of tasks… Internet-scale data collection from over 50+
  jurisdictions." [R1·C4]
  (https://www.harvey.ai/company/careers/9b7ae8f4-773e-4f83-83fa-096d157ae00d)
- **Agents — Senior ($193,400–290K) and Staff ($231–340K); hiring across Mid/Senior/Staff.**
  "design environments and actions for agentic professional work, make model
  selection decisions, manage context windows, create optimal tools, and develop
  evals"; caching / parallel tool calls / subagent patterns with the model-infra
  team. Python + LLM APIs + agent frameworks. Signal: eval-and-harness-centric
  applied-agent org. [R1·C4]
  (https://www.harvey.ai/company/careers/04eb457b-e985-4e3b-9635-0a2b867ada97 ;
  https://www.harvey.ai/company/careers/24a1df80-c1b7-4e16-b938-1cb3b129463d)
- **Developer Experience — Staff ($238–290K, 7+ YoE).** CI/CD (Buildkite,
  GitHub Actions), test/load-test frameworks, "paved road," and "apply AI
  directly to the problem of developer productivity." Signal: platform/velocity
  investment typical of a company outrunning its own tooling. [R1·C4]
  (https://www.harvey.ai/company/careers/45a49240-f928-4547-93ec-cd3bf5b0191d)
- **Staff Database Engineer ($190,720–286,080 / up to $290K, 10+ YoE).** Global
  PostgreSQL fleet, multi-region, migration governance, "build the database
  engineering function at Harvey… set the hiring bar." Vector-DB / embedding
  storage a plus. Signal: data-layer function being built from scratch. [R1·C4]
  (https://www.harvey.ai/company/careers/313d5aa8-bfc9-4057-b9a3-b73b4894f6a7)
- **Frontend — Staff (Toronto, hybrid 3+ days).** Owns the platform layer
  (notifications, permissions, feature flags) + enterprise collaboration
  (secure multi-party, cross-org workflows, admin controls). [R1·C4]
  (https://www.harvey.ai/company/careers/47d3d763-8c64-4e33-b76e-ca15f584c1fd)
- **Full-Stack — Senior (NYC) and Senior "New Verticals."** Product Engineering,
  5+ YoE, React/TypeScript/TailwindCSS/Python; New Verticals = "build new
  products… from first principles." Signal: expanding beyond the original
  legal-research surface. [R1·C4]
  (https://www.harvey.ai/company/careers/10900071-f75f-49da-bff7-7e9db5e9b1f9 ;
  https://jobsbyculture.com/jobs/harvey/senior-software-engineer-full-stack-new-verticals)
- **Security — Detection & Response Security Engineer (4+ YoE) and Senior
  Product Security Engineer (5+ YoE).** "offensive-security-minded blue teamer";
  agentic threat-detection platform built on **ClickHouse**; "we are all
  software engineers, contributing code daily… engineering-first approach";
  secure-by-default libraries; LLM-app security. Signal: security treated as an
  engineering discipline and a named early team. [R1·C4]
  (https://www.harvey.ai/company/careers/bca707ed-5c96-44d2-8430-8b6fafc35f45 ;
  https://www.harvey.ai/company/careers/50a8df2a-c50e-4326-ae90-0c9f8ee0cf1d)
- **Founding Forward Deployed Engineer (NYC).** Services-GTM motion embedded in
  BigLaw. [R1·C3]
  (https://www.builtinnyc.com/job/forward-deployment-engineer/7406694 ;
  https://app.welcometothejungle.com/jobs/2QZ53YSK)
- **Legal Engineers / Legal Engineering Managers (many; SF, NYC, Chicago, Dallas,
  Toronto).** "former practicing lawyers who bridge customers, sales, and
  product"; also "Legal Engineer – Product Specialist" (post-sales adoption).
  These are the embedded-lawyer / domain-integrated roles, not SWE. [R1·C4]
  (https://www.harvey.ai/company/careers/f4d70ed0-010e-40f5-b194-2813e55f6e0c ;
  https://www.harvey.ai/company/careers/2dd28360-5a6b-4769-adb6-e747f0f0bdcc)
- **Engineering leadership hiring:** Engineering Manager, Product (SF/NYC/Toronto)
  and Director of Engineering, Core Product (SF) both appear in the Ashby feed. [R3·C3]
  (https://jobsbyculture.com/jobs/harvey/engineering-manager-product-y1ucr ;
  https://jobsbyculture.com/companies/harvey)

**International-expansion signal.** Roles/offices now span **SF (HQ), NYC,
London, Toronto**, plus **Bengaluru/Bangalore** as a newly-established hub
(late June 2026) [R2·C3]
(https://www.wownews24x7.com/harvey-ai-establishes-bengaluru-hub-to-expand-legal-ai-ecosystem);
a June-2026 Blind thread notes India is "becoming a core engineering + product
hub, not just support" with the caveat "very little presence in India… their
engineering team is in US. Now they are expanding" [R4·C2]
(https://www.teamblind.com/post/harvey-ai-india-bangalore-how-is-engineering-comp-wlb-scj0vre7).
Weinberg (Observer, Mar 2026) confirms London + Toronto office announcements and
a new internship / early-career program + law-school partnerships (US/UK/Spain/
Australia) [R2·C3] (https://observer.com/2026/03/harvey-ceo-winston-weinberg-ai-law/).

**Dedicated recruiting build-out signal.** Harvey is hiring a "**Senior Technical
Recruiter, Security**" — "Harvey's first fully dedicated security recruiter…
build the pipelines… position Harvey competitively against other high-growth AI
and tech companies," using **Ashby** as the ATS and targeting Black Hat / DEF CON
/ BSides. Signal: security hiring is a standalone, greenfield talent function =
security is a scaling priority. [R2·C3]
(https://underprompt.com/jobs/senior-technical-recruiter-security-harvey-ai)

**Overall hiring-mix read (organized, not concluded):** early/greenfield framing
recurs on AI Platform, Database, Security, DevEx and the security-recruiter role
(= foundational teams still forming); Core Infra + Backend emphasise scale/
reliability of a live high-throughput platform (= scaling phase); Forward
Deployed + Legal Engineer roles = services-heavy BigLaw GTM; Toronto/London/
Bengaluru + New Verticals + early-career program = geographic and product
expansion.

---

### 2. Compensation (public)

Note three different measurement bases appear below — (a) Harvey's own posted
salary bands (base range, "Offers Equity"), (b) techinterview.org estimated
TOTAL comp (cash + equity), (c) Levels.fyi / jobsbyculture reported TOTAL comp.
They are not directly comparable; the ~$200–300K base + equity thesis is
confirmed by (a).

**(a) First-party posted bands (harvey.ai careers, "Offers Equity"):** [R1·C4]
- Senior SWE, AI Platform: **$220,000–$300,000**
- Staff SWE (AI Platform / Backend / Agents): **$231,000–$340,000**
- Senior SWE, Core Infrastructure: **$200,000–$250,000**
- Senior SWE, Agents: **$193,400–$290,000**
- Staff SWE, Developer Experience: **$238,000–$290,000**
- Staff Database Engineer: **$190,720–$286,080** (one page shows top of $290,000)

**(b) techinterview.org estimated total comp (2026, SF), incl. late-stage equity:** [R3·C3]
(https://www.techinterview.org/companies/harvey-interview-guide/)
- SE $185–255K · Senior SE $270–370K · Staff $385–535K · Principal $545–740K.
- A second techinterview guide gives base-plus-equity ranges: Mid $180–230K base
  → $300–450K total; Senior $230–290K base → $450–650K total; Staff $290–370K
  base → $650K–950K total. [R3·C3]
  (https://www.techinterview.org/companies/harvey-ai-interview-guide/)

**(c) Levels.fyi reported total comp (US):** SWE median **$375K**, high **$595K**;
Full-Stack SWE median **$298K**, high **$437.5K** (last updated Jun 2026). [R3·C3]
(https://www.levels.fyi/companies/harvey/salaries/software-engineer/locations/united-states ;
https://www.levels.fyi/en-gb/companies/harvey/salaries/software-engineer/title/full-stack-software-engineer)

**(d) jobsbyculture "verified compensation reports":** median SWE total comp
**~$336,500**; senior SWE **$500K+**; full-stack packages **up to $529K**;
described as "same tier as frontier AI labs like Anthropic and OpenAI, and well
above most enterprise software companies." [R3·C3]
(https://jobsbyculture.com/blog/working-at-harvey-ai-2026)

**Equity / refresh signal.** Comp narratives lean heavily on equity upside:
valuation moved $715M (2023) → $1.5B (early 2024) → $8B (Dec 2025) → **$11B
(Mar 2026)**, so early joiners' paper returns are emphasised as the draw;
Glassdoor "Compensation & Benefits" sub-score is **4.5/5**. No specific refresh-
grant policy was found (Gap). [R3·C3]
(https://jobsbyculture.com/blog/working-at-harvey-ai-2026)

**BigLaw / frontier-lab comparison note.** techinterview frames Harvey as "BigLaw-
focused premium… competitive at top of late-stage AI company bands"; the
India Blind thread offers a dissent — "their pay don't seem competitive for the
bar" — though a reply counters that "base seems to be matching FAANG-like numbers
and RSUs are quite a bit." [R4·C2]
(https://www.teamblind.com/post/harvey-ai-india-bangalore-how-is-engineering-comp-wlb-scj0vre7)

---

### 3. Engineering culture (public, verifiable)

**"Re-earn your role every ~6 months" — CORROBORATED TO PRIMARY SOURCE.**
Winston Weinberg, quoted in Fortune (26 Mar 2026): "…you have to 're-earn' your
role every 6 months" [R2·C4]
(https://fortune.com/2026/03/26/harvey-ceo-winston-weinberg-reearn-roles-career-advice-ai-tech-innovation-eleven-billion-dollar-startup-sam-altman-openai-backed/).
Verbatim on the Sequoia "Term Sheet"/podcast: "every six months you have to,
like, re-earn your position in the market. And that trickles down through the
whole company where you have to re-earn your position at the company —
including myself… every six months you absolutely have to change. And if you
don't, I think you just break." [R2·C4]
(https://sequoiacap.com/podcast/harvey-ceo-winston-weinberg-why-you-should-reinvent-yourself-every-4-months/).
BigGo/Sourcery adds his operational tooling: a "calendar audit" every ~6 months
and a "paragraph test" gate before greenlighting any non-routine initiative. [R2·C3]
(https://finance.biggo.com/news/32553845b7c1e553)

**The three stated company values (first-party, verbatim, repeated across ~every
job post):** "**Decisiveness, Simplicity, and Job's Not Finished.** We act
quickly on clear judgment over perfect information, we believe simplicity is what
scales, and we're never satisfied with where we are." [R1·C4]
(https://www.harvey.ai/company/careers/9b7ae8f4-773e-4f83-83fa-096d157ae00d)

**Senior-heavy / customer-obsessed / calmer-than-frontier-lab framing.**
techinterview: "Senior-heavy hires, customer-obsessed (BigLaw partners are
demanding), fast-shipping. **Calmer than frontier-lab pace; more
product-engineering balance.**" [R3·C3]
(https://www.techinterview.org/companies/harvey-interview-guide/). The
senior-heavy read is consistent with the first-party YoE floors (Staff Backend
10+, Core Infra Staff 10+, Database Staff 10+, AI Platform Staff 8+).

**Embedded-lawyers / domain-integrated teams (a defining, eng-relevant trait).**
Harvey deliberately co-locates former attorneys with engineers. Its own
engineering blog names "Applied Legal Researchers (ALRs)" and "Strategic
Business Development Leads (SBDLs)" — "former practicing lawyers who collaborate
closely with Engineering on product development" — inside a data-flywheel/eval
loop [R1·C4]
(https://www.harvey.ai/blog/how-agentic-search-unlocks-legal-research-intelligence).
jobsbyculture: "engineering teams include former attorneys… embedded in the
development process and participate in evaluating whether AI outputs meet the
standard of care"; "hallucination detection is a first-class concern." [R3·C3]
(https://jobsbyculture.com/blog/working-at-harvey-ai-2026). Weinberg (BigGo, Jun
2026): "~960 people across 12 offices, **more than 200 of whom are former
lawyers**. Only about 25 of those lawyers still do traditional legal work; the
rest have migrated into product, go-to-market, and other roles." [R2·C3]
(https://finance.biggo.com/news/32553845b7c1e553)

**In-person SF/NY(/London/Toronto) model.** Multiple job posts state "in-person
work model" / "hybrid, 3+ days-per-week in-person… relocation assistance." [R1·C4]
(https://www.harvey.ai/company/careers/47d3d763-8c64-4e33-b76e-ca15f584c1fd).
Built In: "not a classic 9 to 5," 3+ in-office days near hubs + 1–2 GTM trips/
month; counterweights = flexible PTO, a **4-week "Harvey Holiday" sabbatical
after 4 years, 18 weeks paid parental leave.** [R3·C3]
(https://builtin.com/company/harvey/faq/work-life-balance-wellbeing)

**AI-in-recruiting note — CONFIRMED (first-party).** Harvey job posts carry the
disclosure: "We are an AI company and we use AI to improve all of our processes,
including in the recruitment process. Whilst we do use AI to help improve
efficiency in our recruitment process, we do not rely on AI to make any automated
decisions and ensure that a human reviews AI output." [R1·C4]
(https://www.harvey.ai/company/careers/47d3d763-8c64-4e33-b76e-ca15f584c1fd)

**Tech-stack context (eng-relevant, public).** Python (ML/backend), TypeScript/
React/TailwindCSS (product), some Go (infra); Azure-centric (Azure OpenAI, AKS)
+ GCP; PostgreSQL; Kubernetes; BYOK encryption; eval infra on OpenAI Agents SDK
OpenTelemetry traces → LangSmith. [R1/R3·C3]
(https://www.harvey.ai/blog/how-agentic-search-unlocks-legal-research-intelligence ;
https://jobsbyculture.com/blog/working-at-harvey-ai-2026)

---

### 4. Employee sentiment (public, aggregated only)

**Glassdoor aggregate (via jobsbyculture; corroborated by Glassdoor overview):**
Overall **4.3/5** on **~42–44 reviews**; sub-scores — Compensation & Benefits
**4.5**, Career Opportunities **4.5** (one page shows 3.7), Culture & Values
**4.2**, Senior Management **3.6**, **Work-Life Balance 3.4**; **~81% recommend
to a friend.** [R3·C3]
(https://jobsbyculture.com/companies/harvey ;
https://jobsbyculture.com/blog/working-at-harvey-ai-2026 ;
https://www.glassdoor.com/Overview/Working-at-HARVEY-EI_IE8126873.11,17.htm).
(Minor discrepancy: a jobsbyculture job-page footer cites an "overall 3.9/5"
figure — noted, not reconciled.)

**Aggregated pro/con themes (public, de-individualized):**
- Pros: top-tier comp + equity upside; strong product-market-fit (1,000+
  customers, ~$190M+ ARR); "smart, driven, supportive" colleagues; abundant
  greenfield career growth. [R3·C3]
- Cons: "intensely long hours"/"pressure-cooker"; growing pains + internal
  politics as headcount scales; people-ops (perf reviews, growth conversations)
  lagging headcount; 3+ days in-office friction; limited remote. [R3·C3]
  (https://jobsbyculture.com/blog/working-at-harvey-ai-2026)

**A single positive IC data point (Taro/Glassdoor, SF SWE, Oct 2025):** 5.0
overall; praises "real AI for professionals," fast autonomous shipping; cons =
shifting priorities and immature career-growth/people processes. Treat as one
review. [R4·C2]
(https://www.jointaro.com/interviews/companies/harvey-ai/work-experiences/software-engineer-san-francisco-ca-october-20-2025-5-b36f2a7a/)

**Retention / attrition / stability rumor (WEAK — anonymous).** A Blind post from
a candidate weighing a Senior Backend offer relays unverified rumors of
"excessive PIPs, people disappearing from Slack all of a sudden" and asks whether
it is "cut-throat/unstable"; no corroboration was found. Report only as a
clearly-labeled weak signal / open question. [R4·C2]
(https://www.teamblind.com/post/harvey-ai-need-a-reality-check-on-the-company-culture-and-effectiveness-of-the-product-gwxr4418)

**Talent-war / competitive-poaching context (eng-relevant).** Weinberg (BigGo,
Jun 2026) names the real long-term competitors as the frontier labs — "It is not
Legora… It is OpenAI. It is Anthropic" — with three closing frontiers: well-funded
European rivals (Legora, valued ~$5.5B), frontier labs re-entering verticals, and
elite firms (e.g., Kirkland & Ellis reportedly committing $500M) building AI
in-house [R2·C3] (https://finance.biggo.com/news/32553845b7c1e553). Observer and
FT echo the Legora/CoCounsel/OpenAI competitive frame; Weinberg's stated response
is urgency on differentiated components (security, governance, memory,
integrations) and per-vertical eval frameworks. [R2·C3]
(https://observer.com/2026/03/harvey-ceo-winston-weinberg-ai-law/ ;
https://www.ft.com/content/47eafdcb-5a0a-4515-a07a-70e89ad2fa78). No specific
named engineer poaching event was found (Gap).

---

### 5. The interview process (public)

**Reported loop (techinterview.org, primary R3 source for this slice):**
Recruiter screen → **60-minute coding (Python or TypeScript)** → virtual onsite:
**2 coding, 1 system-design (LLM-flavored), 1 craft deep-dive, 1 behavioral.**
**Cycle: 3–5 weeks.** [R3·C3]
(https://www.techinterview.org/companies/harvey-interview-guide/). The second
techinterview guide frames it as 4–5 onsite rounds (1–2 coding medium, 1 system
design/LLM-app architecture, 1 ML/LLM round for relevant tracks, 1 behavioral),
and notes a **founder interview for senior+ roles.** [R3·C3]
(https://www.techinterview.org/companies/harvey-ai-interview-guide/)

**Typical questions reported (techinterview):** [R3·C3]
- "Design a **RAG pipeline over millions of legal documents** per customer."
- "Design a **contract-analysis system** that compares thousands of provisions."
- "Design an **evaluation harness for legal-correctness** (high-stakes domain)."
- Coding: "medium DSA, often with NLP or pipeline framing."
- Deep-dive question bank incl. **citation grounding** (retrieval-then-cite,
  span-extraction, no hallucinated cites), **redlining engine** (semantic diff
  of two contract drafts), 200-page MSA structured extraction (chunking /
  conflicting clauses / accuracy eval), tenant isolation in vector stores /
  matter-level access control / SOC 2, and model-provider-risk / multi-model
  strategy (the OpenAI-dependence probe).
- Behavioral: "ownership, customer empathy for lawyers, regulated-industry care."

**Independent corroboration of the loop shape (candidate reports, Taro/Glassdoor):**
"coding tech screen followed by an on-site… coding, systems design, and
behavioral"; "coding interviews were **data-structure heavy**"; one candidate flags
a system-design interviewer who was a non-native English speaker (comprehension
friction). [R4·C2]
(https://www.jointaro.com/interviews/companies/harvey-ai/work-experiences/software-engineer-san-francisco-ca-october-20-2025-5-b36f2a7a/).
Blind (India, Staff track): "technical bar seems pretty high… they asked to
implement a spreadsheet." [R4·C2]
(https://www.teamblind.com/post/harvey-ai-india-bangalore-how-is-engineering-comp-wlb-scj0vre7)

**Languages / prep priorities (techinterview):** Python dominant (ML/backend),
TypeScript/Node (product surface), some Go (infra); prep = deep RAG patterns
(chunking, embeddings, reranking, structured extraction) + legal-data-format /
privilege / audit-trail literacy. Timeline dissent: Orbyt estimates a faster
"2–3 weeks, 3–5 rounds." [R3·C3]
(https://www.techinterview.org/companies/harvey-interview-guide/ ;
https://www.orbytjobs.ai/interview-prep/harvey)

**Eng-relevant grounding on how Harvey really evaluates AI (first-party, useful
for the "eval harness" question):** Harvey open-sourced a **Legal Agent Benchmark**
and a filesystem-first harness ("harvey-labs": Run → LLM-judge Evaluate → Report;
six closed-workspace tools), and its Agentic-Search blog details tool-selection
precision moving "from near zero to 0.8–0.9" and metrics tracked (hallucination,
tool recall, retrieval recall, formatting, answer quality). Strong signal for
what a "good" eval-design answer looks like in-loop. [R1·C4]
(https://www.harvey.ai/blog/introducing-harveys-legal-agent-benchmark ;
https://github.com/harveyai/harvey-labs/blob/main/docs/architecture.md ;
https://www.harvey.ai/blog/how-agentic-search-unlocks-legal-research-intelligence)

---

## Reflection trace

- **R1 (2 searches + 1 crawl).** Search A (interview process) immediately hit both
  techinterview.org guides (full loop + questions + comp) plus the harvey-labs eval
  harness and multiple eng job posts. Search B (careers/comp) returned the
  first-party role pages with posted salary bands verbatim. Crawl pulled both
  techinterview guides in full; the harvey.ai/company/careers listing failed
  (CRAWL_NOT_FOUND) → pivoted to aggregators for role counts.
- **R2 (2 searches).** Search A (jobsbyculture + Weinberg quote + values) surfaced
  the jobsbyculture blog (Fortune-sourced "re-earn" line, Glassdoor breakdown) and
  companies page (255 open roles, sub-scores, ~700 employees). Search B (sentiment)
  returned Glassdoor aggregate, Levels.fyi medians, Built In WLB, and two Blind
  threads. Sentiment + comp now saturated.
- **R3 (2 searches + 1 crawl).** Search A corroborated the Weinberg quote to
  Fortune + the Sequoia podcast verbatim and pulled the competitive/talent-war
  frame (Legora, frontier labs, Kirkland $500M). Search B confirmed the
  AI-in-recruiting disclosure (first-party), the Security + Forward-Deployed roles,
  the dedicated security recruiter, and Bengaluru expansion. Consolidating crawl
  deepened culture (jobsbyculture blog), the forward-deployed model (getperspective),
  and WLB benefits (Built In). Marginal return had dropped to re-surfacing known
  role pages → stopped at the cap.

## Gaps and not-found

- **First-party open-role total / function breakdown:** harvey.ai/company/careers
  would not crawl; counts (255 / 292) are third-party and approximate. Exact
  per-function open-headcount is not captured.
- **Headcount is inconsistent across sources:** jobsbyculture blog ~350 and Built
  In 373 (both appear to use an early-2026 or stale figure) vs. Weinberg's ~960
  across 12 offices (BigGo, Jun 2026) and jobsbyculture companies-page "~700."
  Reported, not reconciled.
- **Equity refresh policy:** no specific refresh-grant / vesting-refresh detail
  found; only valuation-trajectory upside narrative.
- **Retention/attrition:** only anonymous Blind rumor (PIPs / "disappearing from
  Slack"); no verifiable attrition rate, no named engineer poaching event.
- **Glassdoor rating discrepancy:** 4.3 (overview + companies page) vs a 3.9
  figure in a jobsbyculture job-page footer — noted, unresolved.
- **Levels.fyi bands read oddly** (e.g., "L3 to L5 both $390K") — likely thin
  sample; treat medians ($375K SWE / $298K full-stack) as the usable figure.
- **Second techinterview guide dates the company to a "Series E / $5B+"** while
  2026 press reports $11B / Series E-plus — comp bands there may lag current
  valuation; used only as an estimate.

## Sources consulted (with grades)

**R1 — Harvey first-party (careers + eng blog + GitHub):**
- Careers role pages (AI Platform S/Staff, Core Infra S/Staff, Backend Staff,
  Agents S/Staff, DevEx Staff, Database Staff, Frontend Staff, Full-Stack Senior,
  Security ×2, Legal Engineer ×2) — salary bands, team framing, values,
  AI-in-recruiting disclosure, in-person model. (harvey.ai/company/careers/… — see
  inline URLs)
- https://www.harvey.ai/blog/how-agentic-search-unlocks-legal-research-intelligence — ALR/SBDL embedded lawyers; eval metrics; tool-selection precision.
- https://www.harvey.ai/blog/introducing-harveys-legal-agent-benchmark — open eval benchmark.
- https://github.com/harveyai/harvey-labs/blob/main/docs/architecture.md — eval harness architecture (Run/Evaluate/Report).

**R2 — established coverage:**
- https://fortune.com/2026/03/26/harvey-ceo-winston-weinberg-reearn-roles-career-advice-ai-tech-innovation-eleven-billion-dollar-startup-sam-altman-openai-backed/ — "re-earn your role every 6 months" (primary).
- https://sequoiacap.com/podcast/harvey-ceo-winston-weinberg-why-you-should-reinvent-yourself-every-4-months/ — verbatim re-earn quote + hiring/org-every-4-months.
- https://finance.biggo.com/news/32553845b7c1e553 — ~960 employees/12 offices, 200+ former lawyers, competitor frame, calendar-audit/paragraph-test.
- https://observer.com/2026/03/harvey-ceo-winston-weinberg-ai-law/ — Legora/CoCounsel competition, London/Toronto offices, early-career program.
- https://www.ft.com/content/47eafdcb-5a0a-4515-a07a-70e89ad2fa78 — staying-ahead-of-Legora/OpenAI, per-vertical eval frameworks.
- https://www.wownews24x7.com/harvey-ai-establishes-bengaluru-hub-to-expand-legal-ai-ecosystem — Bengaluru hub (Jun 2026).
- https://www.artificiallawyer.com/2026/04/07/harvey-drives-legal-agent-learning-via-harness-engineering/ — "harness engineering" (context).

**R3 — jobsbyculture / techinterview.org / Glassdoor-aggregate / Levels.fyi / Built In:**
- https://www.techinterview.org/companies/harvey-interview-guide/ — loop, questions, comp, culture one-liner.
- https://www.techinterview.org/companies/harvey-ai-interview-guide/ — deep question bank, comp estimates, OpenAI-dependence.
- https://jobsbyculture.com/blog/working-at-harvey-ai-2026 — Glassdoor breakdown, culture, comp, tech stack.
- https://jobsbyculture.com/companies/harvey — 255 open roles, sub-scores, ~700 employees, role list.
- https://jobsbyculture.com/jobs/harvey/engineering-manager-product-y1ucr ; …/senior-software-engineer-full-stack-new-verticals — role detail + culture footer.
- https://www.levels.fyi/companies/harvey/salaries/software-engineer/locations/united-states ; …/title/full-stack-software-engineer — comp medians.
- https://builtin.com/company/harvey/faq/work-life-balance-wellbeing — WLB, sabbatical, parental leave, 292 jobs.
- https://www.glassdoor.com/Overview/Working-at-HARVEY-EI_IE8126873.11,17.htm — 4.3/5 (~44 reviews).
- https://www.orbytjobs.ai/interview-prep/harvey — alt timeline (2–3 wks).
- https://underprompt.com/jobs/senior-technical-recruiter-security-harvey-ai — dedicated security recruiter / Ashby / talent-war framing.
- https://getperspective.ai/blog/harvey-ai-forward-deployed-engineers-biglaw-deployment-playbook-2026 — FDE 6–9 mo BigLaw deployment model.
- https://joblaze.com/jobs/software-engineer-agents-c89549 ; https://www.builtinnyc.com/job/forward-deployment-engineer/7406694 ; https://app.welcometothejungle.com/jobs/2QZ53YSK — role reposts.

**R4 — anonymous single posts (weak signal only):**
- https://www.jointaro.com/interviews/companies/harvey-ai/work-experiences/software-engineer-san-francisco-ca-october-20-2025-5-b36f2a7a/ — one SWE review + interview experiences.
- https://www.teamblind.com/post/harvey-ai-need-a-reality-check-on-the-company-culture-and-effectiveness-of-the-product-gwxr4418 — PIP/instability rumor.
- https://www.teamblind.com/post/harvey-ai-india-bangalore-how-is-engineering-comp-wlb-scj0vre7 — India hub / bar / comp chatter.
