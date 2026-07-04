---
type: Dossier
subject: people
company: harvey
created: 2026-07-04
updated: 2026-07-04
version: 1.0
status: draft
primary_source: https://www.harvey.ai/blog/lawyers-at-harvey-applied-legal-research
description: 'Owns the org, leadership, hiring-as-signal, and engineering culture (public-professional signal only). Headline: (1) A ~960-person, founder-controlled org (Weinberg CEO / Pereyra President) with a deep, recently-built exec bench — notably a cluster of ex-Google leaders (CSO Keith Enright ex-Google CPO, GC John LaBarre, VP Legal Eng Tammy Jih Murray), a 2026 CTO (Siva Gurumurthy) and CPO (Anique Drumright), and VP Eng Ben Liebald (ex-Figma) [F/85%]. (2) The signature org bet is domain-integrated: 200+ of ~960 staff are former lawyers, with "Applied Legal Researchers" embedded inside engineering to write evals and grade output — the human engine behind the eval moat [F/85%]. (3) For an engineering candidate: comp is frontier-lab tier (~$200–340K base + equity, ~$375K median total), the AI Platform team is explicitly "early / greenfield," the culture is high-intensity ("re-earn your role every six months," ~4.3/5 Glassdoor but WLB ~3.4, in-office SF/NY), and the interview loop is recruiter → coding → onsite (2 coding, 1 LLM system design, 1 craft, 1 behavioral). The tension: elite, well-compensated, fast-building team — in a pressure-cooker culture, competing with the frontier labs for the same talent.'
---

# Dossier, People

## Owns (single source of truth)

This dossier owns **the people and the org**: leadership roster and backgrounds, the org model, named team members, hiring-as-signal, engineering culture, compensation, the interview process, and talent dynamics — **public-professional signal only** (roles, stated history, public posts, aggregate review data).

**Does NOT own:** the founders' *strategic* decisions as bet/thesis (dossier-thesis); the funding/board *governance* facts (dossier-company owns the board/SEC facts; this dossier reads them as people-signal); product/tech built by these people (dossier-product); who they sell to (dossier-buyers); rivals' orgs (dossier-competitive); the timeline (dossier-activity).

## How to read the tags

`[X/NN%]`: **F** fact (public-verified: name+role+company match), **I** inference, **A** assumption. **Ethical line (playbook 03 §5):** public-professional only — no private-life material, no inferred psychology, no surveillance. Aggregate review data (Glassdoor) is reported as themes, not individual quotes. Conflicts surfaced inline. Every fact resolves to the Reference List.

---

## 1. Leadership & org map

> Purpose: who runs Harvey, verified by public role+background.

**1.1 Founders (control the company).** **Winston Weinberg** — CEO & Co-Founder (ex-O'Melveny litigation associate; JD USC; BA Kenyon) [F/88%]. **Gabe Pereyra** — President & Co-Founder, owns product + research (ex-Google Brain / DeepMind / Meta AI; BS CS USC); FT Law 50 "AI Enabler" (Jun 2026) [F/88%]. Both are officers + directors (dossier-company §4.1) → concentrated founder control.

**1.2 The executive bench (mostly built 2024–2026).**

| Name | Role | Background | Grade |
|---|---|---|---|
| Siva Gurumurthy | **CTO** | pre-Harvey background unverified (gap) | [F/70%] |
| Anique Drumright | **Chief Product Officer** (2026) | — | [F/78%] |
| Ben Liebald | **VP Engineering** (Oct 2024–) — owns Eng/AI/Security/ALR | ex-Figma Sr Dir Eng, ex-Branch CTO | [F/80%] |
| Alan Ghelberg | **CFO** (Feb 2024–) | ex-Aurora VP Finance, General Atlantic; MBA HBS | [F/82%] |
| Katie Burke | **Chief People Officer** (also cited as **COO** — title CONFLICT, likely CPO→COO) | ex-HubSpot CPO; MBA MIT Sloan | [F/75%] |
| Keith Enright | **Chief Strategy Officer** | **ex-Google Chief Privacy Officer**, Gibson Dunn | [F/82%] |
| John LaBarre | **General Counsel** (+ board) | ex-Google Senior Counsel | [F/85%] |
| Tammy Jih Murray | **VP Legal Engineering** | ex-Google | [F/78%] |
| Rob Saliterman | **VP Sales** (Aug 2023–) | ex-Stripe, Snap; MBA HBS | [F/80%] |
| John Haddock | **Chief Business Officer** | — | [F/70%] |
| Niko Grupen | **Head of Applied Research** (built LAB) | ex-Google Brain, PhD Cornell, ex-Apple | [F/85%] |
| Julio Pereyra | **Head of Legal Research** (leads ALRs) | ex-O'Melveny | [F/85%] |

**1.3 The ex-Google legal cluster (a signal).** Three senior legal/privacy leaders came from Google: **Enright (CSO), LaBarre (GC), Jih Murray (VP Legal Engineering)** [F/80%]. Read: Harvey is deliberately building **enterprise-grade legal/privacy/governance leadership** — consistent with the security/ethical-wall moat (product §5, thesis §4) and the malpractice-averse buyer (buyers §5.2). *Julio Pereyra shares the Pereyra surname with Gabe, but the kinship is not publicly stated and is not asserted here.*

**1.4 Possible product-leadership transition (flag).** Aatish Nayak (first PM, ex-Scale AI/Shield AI) shows a VP-Product tenure ending ~May 2026, coinciding with CPO Anique Drumright's arrival — a handoff/departure, unconfirmed [I/50%].

## 2. The signature org model — domain-integrated engineering

> Purpose: the org design that is itself the moat.

**2.1 Lawyers inside the building.** **~200+ of ~960 staff are former lawyers (~21%), of whom only ~25 still practice** (Weinberg, Fortune) [F/82%]. This is the precise basis for the recurring ">20% are lawyers" claim.

**2.2 Applied Legal Researchers (ALRs).** Elite ex-BigLaw attorneys, hired **with no prior AI experience**, embedded *inside engineering* to design evals, write the 75,000+ LAB rubric criteria, and grade model output before it ships [F/82%] (Harvey blog). **The ALRs are the human engine behind the eval-data moat** (thesis §4, S3) — the single most defensible asset in the whole engagement runs on this team.

**2.3 Other embedded roles.** **Strategic Business Development Leads (SBDLs)**, **Legal Engineers** (e.g., Nabil Virji), **Legal Innovation Partners** (e.g., Megan McMillin), and **Forward-Deployed Engineers** (~40–80, embedded in firms 6–9 months; buyers §4.1). The org is deliberately not "just product engineers" — it fuses law + engineering + deployment.

## 3. Named engineering & research people (who you'd work with)

> Purpose: for the candidate — the actual eng/research team, from public bylines.

- **Research:** Niko Grupen (Head of Applied Research, `ngrupen` — the central benchmark author, LAB + BigLaw Bench), Julio Pereyra (Head of Legal Research). Applied-Compute/GLM-5.1 post-train authors: Grupen, J. Pereyra, G. Pereyra, Rhythm Garg, Jacob Phillips, Raymond Feng [F/80%].
- **Engineering:** Joey Wang (Engineering Lead, Spectre co-author), Tom McCormick + Anna Zhang + Gary Lam (vision system), and the "3 Principles" agent-platform authors: Philip Cerles, Philip Lan, Aaron Stern, Boling Yang, Varun Nair, Kevin Ko, Billy Wan [F/80%]. GitHub `spencerp` is a top LAB contributor.
- **Security:** Tobias Boelter (Head of Security) [F/72%].
- **Product/other named staff:** David Murdter (PM, ex-Cooley associate), plus GTM names (Jorge Bestard VP EMEA Sales, Gemma Hamshar CS EMEA, Kerry Aiken GTM Systems) [F/72%].

## 4. Hiring-as-signal (analytical spine)

> Purpose: what Harvey is hiring for, and what it reveals.

- **"AI Platform is early / greenfield."** The AI Platform role text: "This team is early and there's a lot to build: model routing, agent architecture, context management, evals" ($220–340K) [F/82%]. Greenfield framing also on Database, Security, DevEx. → **signal: the core AI infrastructure is still being built — high-ownership opportunity for a joining engineer** [I/72%].
- **Scaling a live platform.** Core Infra/Backend roles emphasize "billions of tokens / millions of daily requests," model proxy, distributed rate limiting → scaling-phase hiring [F/80%].
- **First dedicated security recruiter** (sourcing at Black Hat / DEF CON) → building the security org as a differentiator [F/72%].
- **International + GTM build-out.** Toronto/London/Bengaluru eng; active Enterprise Sales hiring (AE spotlight posts); the Law School Ambassador program as an early talent + adoption funnel [F/78%].
- **Read:** the hiring mix (greenfield AI-platform + scaling infra + security + international + heavy GTM) signals a company **simultaneously building its core and scaling its distribution** — consistent with the activity §2 land-grab posture.

## 5. Engineering culture

> Purpose: what it's actually like, from public/aggregate signal.

- **High intensity, explicitly.** Weinberg (Fortune + Sequoia podcast, primary): employees must **"re-earn your position … every six months you absolutely have to change. And if you don't, I think you just break"** [F/85%]. Values: **Decisiveness, Simplicity, Job's Not Finished** [F/82%].
- **Aggregate sentiment (Glassdoor ~4.3/5, ~42–44 reviews, ~81% recommend):** Comp & Career 4.5, Culture 4.2, Senior Mgmt 3.6, **Work-Life-Balance 3.4** [F/75%, aggregate]. Themes: **top comp + greenfield growth + smart, supportive peers** vs **"pressure-cooker" hours, in-office 3+ days, growing pains/politics, lagging people-ops** [I/65%]. techinterview frames it as "senior-heavy, customer-obsessed, calmer than frontier-lab pace, more product-eng balance" [I/60%] — a mild tension with the Glassdoor WLB signal, carried.
- **Domain-integrated (culture, not just org).** Engineers work alongside embedded lawyers (ALRs) who pressure-test whether output would hold up in practice — a distinctive day-to-day for an engineer [F/78%].
- **In-person.** SF (HQ) + NY, in-office model, relocation offered [F/80%].

## 6. Compensation

Frontier-lab tier: **~$200,000–340,000 base + equity** by level (AI Platform $220–340K; Staff Backend/Frontend $238–290K) [F/80%]; Levels.fyi median SWE total **~$375K** (full-stack ~$298K); a "verified" median ~$336.5K, senior $500K+ [F/70%, aggregator]. Equity carries the $11B-valuation upside (and the dilution/valuation-compression risk from thesis §6.6).

## 7. The interview process (for the candidate)

> Purpose: the concrete loop and how to prepare. (R3 — from techinterview.org, Glassdoor/Taro reports; not Harvey-official.)

- **Loop:** recruiter screen → **60-min coding** (Python or TypeScript) → **onsite (virtual):** 2 coding, **1 LLM-flavored system design**, 1 craft/domain deep-dive, 1 behavioral; **founder interview for senior+**; cycle ~3–5 weeks [I/70%].
- **Coding:** medium DSA, often with an NLP/pipeline framing [I/65%].
- **System design (the differentiator):** "design a **RAG pipeline over millions of legal documents per customer**," "design an **eval harness for legal-correctness**," contract-analysis/redlining at scale, citation grounding, **tenant isolation**, and expect an **OpenAI-dependence / multi-model-risk** probe [I/68%].
- **Behavioral:** ownership, customer empathy for lawyers, regulated-industry care [I/65%].
- **Best prep grounding:** Harvey's own open-source **`harveyai/harvey-labs`** (LAB harness, eval-strategy + architecture docs) and its engineering blog (Tool Bundles, multi-model, RAG, Spectre) — study these to speak Harvey's own architecture back to them (product §3) [I/75%].

## 8. Talent dynamics

- **The talent rival is the labs, not Legora.** Weinberg names **OpenAI/Anthropic** as the real competition for talent (they're also entering legal — competitive §4); Kirkland & Ellis reportedly committing ~$500M to in-house AI [F/72%]. OpenAI hiring Ironclad's Boehmig (competitive §4.2) is the talent-war made concrete.
- **Retention risk** (WLB 3.4 + labs poaching + a possible product-leadership transition) is a real but not alarming signal [I/55%]. No credible mass-attrition evidence found (only anonymous Blind rumor, R4, not relied on).

## Open Questions / Decisions Pending

- **Unverified:** CTO Siva Gurumurthy's pre-Harvey background; the Katie Burke CPO-vs-COO title; whether Aatish Nayak departed. Carried.
- **Ethical-line note:** Julio↔Gabe Pereyra kinship is *not* publicly stated and is deliberately **not asserted**.
- **Headcount** now best-estimated at **~960 (Weinberg, 2026)** — backflowed to dossier-company §5.5.
- **Load-bearing tension handed to synthesis:** Harvey has assembled an elite, frontier-lab-caliber, domain-integrated team and pays for it — but runs a high-intensity, "re-earn-your-role" culture (WLB ~3.4) while competing with the very labs it depends on for the same engineers. For *you*: this is a place to do genuinely hard, greenfield AI-platform work with strong comp and smart peers, at the cost of intensity and in-office expectations — and where the eval/domain-integration work (ALRs + engineers) is the actual moat you'd be contributing to.
- **Routed this session:** company (backflow — headcount ~960, 75% AmLaw, $100M net-new-ARR-quarter, exec roster: Gurumurthy/Drumright/Enright/Liebald — already reflected in §5); activity (Toronto Maple Leafs partnership, Harvey FORUM Sydney Sept 2026, Sonnet 5 Jun 30, Korea/Australia/Poland/LatAm firmwide wins — timeline); product (David Murdter's "interactive artifacts / legal data viz" feature Jun 2026; Sonnet 5 5.8% LAB); competitive (labs as the talent rival — already in competitive §4).

## Key Terms

| Term | Plain meaning |
|---|---|
| ALR (Applied Legal Researcher) | Ex-BigLaw lawyer embedded in engineering to design/grade evals |
| SBDL | Strategic Business Development Lead — a hybrid GTM/domain role |
| FDE | Forward-Deployed Engineer — embedded in the customer's deployment |
| Hiring-as-signal | Reading a company's open roles to infer its direction/priorities |
| System design (interview) | An open-ended "design a system for X" interview round |
| Re-earn your role | Weinberg's stated expectation that everyone's role is re-justified ~every 6 months |
| Glassdoor aggregate | Averaged public employee-review scores (used as a theme signal, not fact) |

## Reference List

- Harvey 2024, *Lawyers at Harvey: Applied Legal Research*, <https://www.harvey.ai/blog/lawyers-at-harvey-applied-legal-research>.
- Harvey, *Company* (leadership, values), viewed 2026-07-04, <https://www.harvey.ai/company>.
- Harvey careers (role text + comp): AI Platform <https://www.harvey.ai/company/careers/51fb953a-c494-4a09-8fe2-8d7268b863ec>; Core Infrastructure <https://www.harvey.ai/company/careers/4a82c276-1113-41f6-baf9-a5be27e5c78f>.
- Harvey engineering blog (named authors): *3 Principles* <https://www.harvey.ai/blog/principles-that-helped-us-scale-agent-development>; *Building Image Understanding* <https://www.harvey.ai/blog/building-image-understanding-for-legal-documents>.
- Fortune 2026, *Harvey CEO Winston Weinberg on re-earning roles* (culture; ~960 staff, 200+ lawyers), 26 Mar 2026, <https://fortune.com/2026/03/26/harvey-ceo-winston-weinberg-reearn-roles/>.
- techinterview.org 2026, *Harvey Interview Guide*, 6 May 2026, <https://www.techinterview.org/companies/harvey-interview-guide/>.
- jobsbyculture 2026, *Working at Harvey AI in 2026* (comp, culture, Glassdoor themes), 11 Apr 2026, <https://jobsbyculture.com/blog/working-at-harvey-ai-2026>.
- Levels.fyi, *Harvey compensation*, viewed 2026-07-04, <https://www.levels.fyi/companies/harvey>.
- LinkedIn (Apify social-crawl, 2026-07-04): Harvey company page + Weinberg (75% AmLaw / $100M net-new-ARR-quarter, Jul 1 2026) + Pereyra (FT Law 50) — see `people/01-gather/social-linkedin.md`.
- TheOrg, *Harvey org chart*, viewed 2026-07-04, <https://theorg.com/org/harvey-ai>.
- GitHub `harveyai/harvey-labs` contributors, viewed 2026-07-04, <https://github.com/harveyai/harvey-labs>.
