---
type: Dossier
subject: product
company: harvey
created: 2026-07-04
updated: 2026-07-04
version: 1.0
status: draft
primary_source: https://www.harvey.ai/blog/principles-that-helped-us-scale-agent-development
description: 'Owns what Harvey ships vs. what it markets, and the tech stack. Headline: (1) At the ENGINEERING level Harvey is clearly not a thin wrapper — a genuine multi-cloud agent runtime, production RAG (LanceDB + custom voyage-law-2-harvey embeddings), an OpenAI-Agents-SDK "Tool Bundle" architecture with eval gates, an on-demand vision system, and serious security are all real, primary-documented systems [F/90%]. (2) But the marketed-vs-shipped gap is real: "agents execute legal work end-to-end" is qualified by mandatory human-in-the-loop in Harvey''s own copy, and several 2026 marquee surfaces (Contract Intelligence, Command Center, Shared Spaces, Connector Library) are Early Access/waitlist, Memory is pre-product, and the post-trained GLM-5.1 is a benchmark result not a shipped model [F/88%]. (3) The shipped core that works — Assistant, Vault, Workflows, Word add-in, Ask LexisNexis, Deep Analysis — is a strong review-ready-first-draft engine on high-volume pattern work, with attorney verification non-negotiable. Stack: Python/Go/React-TS-Tailwind on Azure+GCP/K8s. Comp ~$200–300K + equity, SF/NY in-person.'
---

# Dossier, Product

## Owns (single source of truth)

This dossier owns **the artifact**: the product line, the marketed-vs-shipped reality of each surface, the engineering/AI architecture and tech stack, the public engineering surface (GitHub), the security architecture, and the shipped accuracy/reliability constraints. For an engineering candidate it is the core dossier.

**Does NOT own:** whether the product's approach is a durable bet (dossier-thesis owns the moat/thin-wrapper *business* argument; this dossier owns the *technical* build-reality); the entity/funding (dossier-company); who buys and pricing-as-willingness-to-pay (dossier-buyers owns ICP; this dossier records reported pricing only as a shipped-product fact); competitor feature-by-feature (dossier-competitive); launch *timing* as momentum (dossier-activity); the engineers/teams as people-signal and hiring analysis (dossier-people owns org/hiring; this dossier records team/role facts as they bear on the product and the interview).

## How to read the tags

`[X/NN%]`: **F** fact (primary-checked), **I** inference, **A** assumption. **Two dossier-wide rules:** (1) a Harvey marketing page is **R1 for "what is marketed," weak for "what ships"** — the shipped claim is graded by independent evidence; (2) usage/throughput figures are Harvey-self-reported (cap at C3). Conflicts surfaced inline. Every fact resolves to the Reference List.

---

## 1. The marketed-vs-shipped x-ray (analytical spine)

> Purpose: separate what Harvey markets from what actually ships and is generally available. This table is the spine; sections 2–7 expand it.

| Surface | Marketed as | Shipped state (2026-07-04) | GA? |
|---|---|---|---|
| **Assistant** | Ask/analyze/draft with domain AI; the "front door" | Validated shipped core; legal-tuned chat + drafting + doc analysis; API (developers.harvey.ai) | **GA** [F/90%] |
| **Vault** | Secure store + bulk analysis, "tens of thousands" of docs | Most-validated shipped surface: Review / Ask / Deep Analysis modes; live API (`ready_to_query`, review tables, 10 req/min); iManage/SharePoint/Drive sync | **GA** [F/90%] |
| **Knowledge** | Research across 100+/500+ legal/reg/tax sources | Shipped as a citation layer *on top of* Westlaw/Lexis, not a replacement | **GA** [F/82%] |
| **Workflows / Workflow Builder** | Pre-built + custom multi-step, no-code | Shipped; the real strength = constrained firm-validated automation (Paul Weiss reference) | **GA** [F/85%] |
| **Agents / Agent Builder** | "Execute legal work end-to-end"; 500+ prebuilt, 25k+ custom | Agent Builder in **Early Access** (May 2026); agents = review-ready drafts + human-in-the-loop, not autonomous | **EA** [F/85%] |
| **Deep Research / Deep Analysis** | Agentic multi-source analysis + reports | Deep Analysis GA ("available now," 445K reports); the *OpenAI* Deep Research integration was in early-access/testing | **split** [F/82%] |
| **Word add-in / M365** | Use Harvey where you work | Word add-in **GA since Dec 2024**; M365 Copilot/SharePoint routing GA | **GA** [F/88%] |
| **Ask LexisNexis** | Cited answers from Lexis inside Harvey | Shipped Aug 2025; paid add-on (~$400–600/lawyer/yr; a bundled seat ~$2,400) | **GA** [F/82%] |
| **Harvey Mobile** | Phone/tablet, dictation, doc scan | Shipped Sept 2025; Deep Analysis on Android | **GA** [F/85%] |
| **Contract Intelligence** | In-house contract lifecycle system | **Design-partner waitlist**; only testimonial is Harvey's own GC | **EA/waitlist** [F/85%] |
| **Command Center** | Adoption analytics + peer benchmarking | **Early Access / waitlist** | **EA** [F/85%] |
| **Shared Spaces** | Cross-org secure collaboration | Early access; GA "expected March 2026" (Harvey-stated) | **EA→GA** [F/80%] |
| **Connector Library** | Native + MCP connectors to the legal stack | **Mid-June Early Access** for select customers | **EA** [F/82%] |
| **Memory** | Retain matter context/preferences across work | **Pre-product** — co-build/listening-tours, entirely future tense | **not shipped** [F/88%] |
| **Own legal model (GLM-5.1 post-train)** | "Legal foundation model series" | **Benchmark/research result**, not a confirmed production model | **research** [F/85%] |

**Read of §1:** the *shipped core* (Assistant, Vault, Workflows, Word, Ask Lexis, Deep Analysis, Mobile) is real and strong; the *2026 frontier* (Contract Intelligence, Command Center, Shared Spaces, Connectors, Memory, own-model) is largely announced-but-early. This is normal for a company shipping fast, but a candidate should not mistake the roadmap for the product.

## 2. What ships and works — vs the "end-to-end" claim

> Purpose: the honest shipped capability, separated from the marketing verb.

**2.1 The strong shipped core.** Vault is the most-validated surface — three shipped modes (Review = per-file tabular answers; Ask = consolidated cross-doc; Deep Analysis = cited reports), a live API with explicit citation/verification fields, DMS sync [F/88%] (GC AI; developers.harvey.ai). Assistant is the legal-tuned "front door" [F/85%]. Workflows' real strength is **constrained, firm-validated automation** — "Harvey is not selling a model, it is selling a workflow platform with a model underneath it" [I/75%] (Ascero).

**2.2 The core marketed-vs-shipped gap: "end-to-end" ≠ autonomous.** Harvey markets "Agents execute legal work end-to-end," but **its own product copy qualifies it**: "Delegate the Work. **Own the Judgment**… You make the call"; Agent Builder ships "human-in-the-loop checkpoints as a core feature" [F/90%] (harvey.ai/agents). Every independent review converges: agents handle *volume/pattern* work (contract review, doc comparison, first-draft memos in 20–30 min vs 3–4 hrs), humans retain *judgment/novel-issue/advocacy* work [F/85%] (AI Vortex; Ascero; Latham did not deploy Harvey for advocacy). This ties directly to thesis §6.1: Harvey's own LAB shows frontier models complete **<10%** of long-horizon legal tasks end-to-end under all-pass grading [F/96% verified] — Harvey's own instrument says the agents are not yet autonomous.

**2.3 Accuracy reality — verification is non-negotiable.** No independent hallucination benchmark of the Harvey product exists (thesis §6.7); Stanford's legal-AI range is 6–33%; co-founder Pereyra concedes Harvey is "not at zero." Every serious review treats Harvey output as "a first draft that requires attorney review" [F/88%]. The shipped mitigations are real: grounded RAG with citations, all-pass eval gating, and (as an *emergent* training outcome, not a named subsystem) hallucination reduction in the GLM-5.1 post-train. The recon-era "0.2% hallucination" figure is R3-only and **not** a verified Harvey primary — do not rely on it.

## 3. The engineering architecture (the crown jewels — interview-critical)

> Purpose: the concrete AI/agent architecture, the part an engineering interview will probe. All primary from Harvey's own eng blog.

**3.1 Agent framework — deliberately not home-grown.** Harvey adopted the **OpenAI Agents SDK** rather than building its own orchestration, *because* it "explicitly left out… a 'workflow' type format… [which] forced our team to work with the strengths of the newest generation of models — calling tools in a loop" [F/88%]. Three scaling principles: (1) **No custom orchestration** — every top-level thread is an agent; (2) **Capabilities are Tool Bundles** — a Tool Bundle packages tools/sub-agents + system-prompt instructions into one portable unit (e.g., a file-system bundle = grep-like search + open + semantic search); (3) **Eval gates** — every Tool Bundle/prompt change must pass **leave-one-out validation** on benchmark datasets to deploy. The org-design insight, quotable in interview: *"You're no longer merging unit-testable code, you're merging English."*

**3.2 The own multi-cloud agent runtime + Spectre.** Harvey built its **own cloud agent runtime** across **Azure + GCP** (rather than a managed runtime) to get three things managed runtimes can't yet give it: multi-model, zero-data-retention, and cost control. Key line: *"the choice of model is just a routing decision."* Claimed **3–5× cost reduction** vs frontier-only, routing each task to the cheapest model meeting the quality bar, including self-hosted open-source [F/85% claimed]. **Spectre** is the internal collaborative cloud-agent platform: **durable runs + ephemeral workers** (the run record is the durable object, not the process), **sandboxes as the hard execution boundary**, "a harness, not a wrapper," Slack/web/CLI all pointing at one durable run, cron scheduled runs [F/85%]. The legal mapping is deliberate: repos→matters, diffs→document versions, sandbox boundaries→ethical walls.

**3.3 Multi-model routing.** Routes across **Anthropic + Google DeepMind + OpenAI + self-hosted open-source**, matched per task via BigLaw Bench + LAB (e.g., Opus-class for agentic reasoning, GPT-class for sourced long-form, Sonnet/Gemini-Flash for low-latency Vault); workspace admins can disable providers, users pick a model [F/88%]. Multi-model is framed as a moat pillar (thesis §4) *and* a reliability/failover design.

**3.4 RAG + custom embeddings.** Production RAG on **LanceDB Enterprise** (15M rows w/ metadata filtering, <2s P50, IVF-PQ), Postgres+PGVector for smaller/public data; the VectorDB can be hosted **in the customer's own private cloud bucket** [F/85%]. Custom embeddings = **`voyage-law-2-harvey`** (Voyage partnership), fine-tuned from voyage-law-2 on **20B+ tokens of US case law**, reportedly ~25% fewer irrelevant top results at 1/3 the dimensionality (NDCG@10/Recall@100) [F/82%].

**3.5 On-demand vision.** Image understanding is **a tool the agent invokes, not an indexing step**: "text-first, vision-second" gating narrows a 500-page doc to 2–3 candidate pages in ms via existing search infra, then a dedicated high-DPI rendering service does structured visual reasoning (reads chart axes, reports confidence). Economics: an image is ~50× a text response, and ~90% of images aren't needed per query [F/85%].

**3.6 File ingestion + the "Data Factory."** DMS ingestion (millions of iManage/SharePoint/Drive docs) runs on **Temporal** (checkpointed, resumes mid-100k-file run), an **in-house Redis rate limiter**, PgBouncer pooling, blob storage for large state [F/85%]. A multi-agent "Data Factory" scaled knowledge sources from 6 to 60+ jurisdictions by treating sources as **parameterized tools** (one reasoning system) rather than one sub-agent per jurisdiction [F/82%].

**3.7 The own-model post-train (research result).** With **Applied Compute**, Harvey post-trained the open-weight **GLM-5.1** via full-parameter async RL (on "AC2"), lifting rubric pass 0.853→0.913 (beating Opus 4.8 Max & GPT-5.5 xhigh on rubric pass) [F/94% verified]. Notable engineering: **GPT-5-Mini graders** (batching criteria → 40–100× cheaper grading), harness optimization, and **compaction** (90th-pct task ≈100k doc tokens; summarize-transcript-and-continue past the context window). **This is a benchmark result, not the shipped default model** [F/85%] — see thesis §5.2.

**3.8 Context management / memory as a platform concern.** The AI Platform team charter is literally "model routing, agent architecture, context management, evals" and "session state and memory that all of Harvey's agents rely on" [F/85%]. (Note: the *customer-facing* Memory feature is pre-product, §1; the *platform-level* context/memory systems are real internal work.)

## 4. Tech stack & infrastructure (quick reference)

| Layer | Stack (primary-sourced) |
|---|---|
| Languages | **Python** (asyncio, Flask/FastAPI) backend/AI; **Go** for infra; **TypeScript** product |
| Frontend | **React + TypeScript + TailwindCSS**, delivered as a **PWA** ("we use TailwindCSS," verbatim across ≥5 job posts) |
| Cloud | **Microsoft Azure** (primary host) + **GCP** (multi-cloud); Kubernetes orchestration |
| Data | **PostgreSQL** + PgBouncer; **Redis** (+ Kafka named in roles); **LanceDB Enterprise** + PGVector (vectors); blob storage |
| Orchestration | **Temporal** (ingestion); **OpenAI Agents SDK** (agents); custom model proxy/router |
| IaC / Ops | **Terraform + Pulumi**; **Datadog + Sentry**; **PagerDuty + Incident.io** |
| Model layer | Multi-model (Anthropic/Google/OpenAI/self-hosted); voyage-law-2-harvey embeddings; post-trained GLM-5.1 (research) |

Scale claim (self-reported): "billions of prompt tokens and millions of daily requests"; company-wide token use 1T→12–13T/month (Jan→May 2026) [F/80% claimed].

## 5. Security architecture

Certifications: **SOC 2 Type II + ISO 27001** (annual, audited by Schellman), plus ISO 27701, ISO 42001, GDPR, CCPA; pen-tests by NCC Group, Bishop Fox [F/88%]. Encryption AES-256 at rest / TLS 1.2+ in transit [F/85%]. **Tenant isolation is enforced at the vector-DB/storage layer by tenant ID (segmented, not filtered after the fact)** [F/85%] — an interview-relevant design choice. **ZDR + no training on customer data**, contractual and architectural; model providers contractually barred from training on customer data [F/88%]. Data residency: three processing regions (US/EU/Switzerland, EU-only, Australia) + storage in 30+ countries [F/82%]. Ethical walls / conflict-aware governance encoded in the runtime [F/80%]. This security bar is itself a barrier to entry vs consumer-grade tools (thesis §4).

## 6. Public engineering surface (GitHub — primary)

`github.com/harveyai`: **7 public repos, only `harvey-labs` (LAB) actively committed** (pushed 2026-07-01) — the real product is a **private monorepo** [F/95%] (GitHub API). LAB is substantial: **1,749 task files across 25 practice areas**, an execution harness (`agent_loop.py`, `run.py`), an LLM-judge eval, a Dockerized sandbox, **6 model adapters** (anthropic/openai/google/mistral/fireworks/baseten), MIT-licensed, dataset openly committed [F/95%]. `biglaw-bench` (168★) is the predecessor. Forks reveal stack history: `react-doc-viewer` (+1 commit "smooth scroll in pdf view for harvey," shipped to npm as `@harvey.ai/react-doc-viewer`), `teams-ai` (+2 Python commits, Teams bot), `pdfplumber` (+0, unused snapshot). **No public SDK on npm/PyPI** (positive control passed) — a developer API exists (developers.harvey.ai) but no published client library [F/90%]. Top contributors: `spencerp`, `ngrupen` (Niko Grupen — 20 commits on biglaw-bench, the primary benchmark author), `GabrielPereyra` (co-founder). *Correction to earlier recon: the GitHub "Pereyra" contributor is Gabriel, not Julio.*

**What this surface proves and doesn't:** it proves an active research/eval engineering team and a real open benchmark; it proves **nothing** about the private product's infra scale, revenue, or customers [I/85%].

## 7. Is Harvey a "thin wrapper"? The engineering vs business distinction

> Purpose: the question a candidate will be asked, answered honestly.

At the **engineering level, no** — the runtime, multi-cloud routing, production RAG with custom legal embeddings, eval infrastructure, Temporal ingestion, on-demand vision, tenant-isolated security, and RL post-training are substantial, non-trivial systems that a "ChatGPT wrapper" does not have [I/80%]. Weinberg himself concedes that in 2023–24 "a lot of the power… is honestly the model, plus front-end work," but argues the hard part is the system over 100k documents (thesis §3.2). The "thin wrapper" critique (thesis §6) is really a **business-durability** argument (does this engineering translate into a durable moat once labs commoditize the layer?), **not** an engineering-triviality argument. For a candidate the honest framing: *the engineering is real and hard; the open question is whether it compounds into durable advantage.* Both halves are defensible and both should be in your interview answer.

## Interview-relevant synthesis (engineering)

- **Teams you might join:** AI Platform (model routing, agent architecture, context/memory, evals — "early, a lot to build"), Core Infrastructure (multi-cloud, K8s, model proxy, rate limiting), Backend Platform, Product/Full-Stack/Frontend, DevEx, Security [F/85%].
- **What they test (from job posts + techinterview.org, R3):** fluency in **Python + TypeScript**; **RAG depth** (chunking, embeddings, reranking, structured extraction); **eval/agent architecture**; regulated-data care (privilege, audit trails). Reported loop: recruiter → 60-min coding → onsite (2 coding, 1 LLM-flavored system design, 1 craft deep-dive, 1 behavioral); typical system-design prompts: "design a RAG pipeline over millions of legal docs per customer," "design an eval harness for legal correctness" [I/70%, R3].
- **Comp / location:** ~$200–300K base + equity (Senior→Staff); **SF/NY in-person** with relocation; senior-heavy hiring, "calmer than frontier-lab pace" [F/80% comp; I/65% culture].
- **Talking points that will land:** the Tool-Bundle + eval-gate architecture; why they chose the OpenAI Agents SDK over custom orchestration; all-pass eval philosophy ("95%-right is wrong"); the multi-model "model choice is a routing decision" design; tenant isolation at the DB layer; the GLM-5.1 post-train as the own-model wedge; and the honest thin-wrapper-is-a-business-not-engineering question.

## Open Questions / Decisions Pending

- **GA timing** of Contract Intelligence, Command Center, Connector Library, and whether GLM-5.1 (or a successor) reaches production as a default model — unknown from outside; watch the blog.
- **Metric conflicts** (700k vs 400k daily tasks; 142k vs 100k lawyers; 100+ vs 500+ knowledge sources) are Harvey-internal inconsistencies, carried.
- **Interview-loop specifics** are R3 (techinterview.org / job aggregators), not confirmed by Harvey — treat as indicative.
- **Load-bearing tension handed to synthesis:** the engineering is genuinely strong and not a wrapper — but the shipped *autonomy* is well short of the "end-to-end" marketing, and the newest surfaces are early. The candidate's dual truth: real, hard, interesting engineering; a product whose autonomous-agent promise is still maturing.
- **Routed this session:** people (team structure, named engineers spencerp/ngrupen, comp bands, interview loop, AI Platform "early" charter); competitive (LanceDB/voyage embeddings/own-runtime as technical differentiators; the shipped-vs-EA reality vs rivals); activity (2026 launch cadence: Agent Builder Mar, Contract Intelligence/Command Center May, Connector Library/Datasite Jun, GLM-5.1 Jun); buyers (pricing ~$1–1.2k/seat, no public pricing, Ask-Lexis add-on economics; per-firm productivity claims); thesis (GLM-5.1 confirmed benchmark-not-production — reinforces §5.2).

## Key Terms

| Term | Plain meaning |
|---|---|
| Tool Bundle | Harvey's unit of agent capability — packaged tools/sub-agents + prompt instructions, portable across agents |
| Eval gate / leave-one-out | A benchmark test a capability must pass before deploy; leave-one-out isolates each capability's effect |
| All-pass grading | A task passes only if every rubric criterion passes (LAB); "95%-right is wrong" |
| Agent runtime | The system that executes an agent's tool-calling loop in a sandbox; Harvey built its own (multi-cloud) |
| Compaction | Summarizing a long agent transcript to continue past the model's context window |
| ZDR (zero data retention) | Providers keep no copy of inputs/outputs; enforced contractually + architecturally |
| Tenant isolation | Each customer's data partitioned at the storage/vector-DB layer, not filtered after retrieval |
| voyage-law-2-harvey | Harvey's custom legal embedding model (fine-tuned with Voyage on US case law) |
| PWA | Progressive web app — web app with native-like install/offline behavior |

## Reference List

- Harvey 2024–2026, engineering blog: *3 Principles That Helped Us Scale Agent Development* <https://www.harvey.ai/blog/principles-that-helped-us-scale-agent-development>; *Building Spectre* <https://www.harvey.ai/blog/building-spectre-internal-collaborative-cloud-agent-platform>; *Why we Built our own Cloud Agent Infrastructure* <https://www.harvey.ai/blog/why-we-built-our-own-cloud-agent-infrastructure>; *Why Harvey is Multi-Model by Design* <https://www.harvey.ai/blog/why-harvey-is-multi-model-by-design>; *Enterprise-Grade RAG Systems* <https://www.harvey.ai/blog/enterprise-grade-rag-systems>; *Building Image Understanding for Legal Documents* <https://www.harvey.ai/blog/building-image-understanding-for-legal-documents>; *Building a New File Ingestion System* <https://www.harvey.ai/blog/building-new-file-ingestion-system-to-scale-firm-knowledge>; *Training a Legal Agent With Applied Compute* <https://www.harvey.ai/blog/training-a-legal-agent-with-applied-compute>.
- Harvey product/marketing: *Platform* <https://www.harvey.ai/platform>; *Agents* <https://www.harvey.ai/agents>; *Introducing Agent Builder* <https://www.harvey.ai/blog/introducing-agent-builder>; *Introducing Contract Intelligence* <https://www.harvey.ai/blog/introducing-contract-intelligence>; *Introducing Command Center* <https://www.harvey.ai/blog/introducing-command-center>; *Memory in Harvey* <https://www.harvey.ai/blog/memory-in-harvey>; *Introducing Ask LexisNexis* <https://www.harvey.ai/blog/introducing-ask-lexisnexis>; *Connector Library* <https://www.harvey.ai/blog/connector-library>.
- Harvey developer docs, *Vault / Assistant guides*, viewed 2026-07-04, <https://developers.harvey.ai/guides/vault>.
- Harvey security, *Security / Trust Center*, viewed 2026-07-04, <https://www.harvey.ai/security>, <https://trust.harvey.ai/>.
- Harvey careers (role requirements + comp): AI Platform <https://www.harvey.ai/company/careers/51fb953a-c494-4a09-8fe2-8d7268b863ec>; Core Infrastructure <https://www.harvey.ai/company/careers/4a82c276-1113-41f6-baf9-a5be27e5c78f>.
- GitHub REST API, *github.com/harveyai* repos + harvey-labs tree/contributors, viewed 2026-07-04, <https://api.github.com/orgs/harveyai/repos>.
- Voyage AI 2024, *Harvey partners with Voyage to build custom legal embeddings*, <https://blog.voyageai.com/2024/07/31/harvey-partners-with-voyage-to-build-custom-legal-embeddings/>.
- GC AI 2026, *Harvey AI for Legal Teams: Review*, 29 May 2026, <https://gc.ai/blog/harvey-legal-ai-review>.
- Ascero 2026, *Harvey BigLaw AI 2026 Deployment Data*, 28 May 2026, <https://asceroai.com/news/harvey-big-law-ai-2026-deployment-data>.
- AI Vortex 2026, *Harvey Agent Builder Review* + *Does Harvey AI Hallucinate?*, 17 Apr 2026, <https://www.aivortex.io/legal/agentic-ai/harvey-agent-builder-review/>.
- techinterview.org 2026, *Harvey Interview Guide*, 6 May 2026, <https://www.techinterview.org/companies/harvey-interview-guide/>.
- jobsbyculture 2026, *Working at Harvey AI in 2026* (stack, comp, culture), 11 Apr 2026, <https://jobsbyculture.com/blog/working-at-harvey-ai-2026>.
- Law.com Legaltech News 2026, *Harvey Announces Contract Review Product, Adoption Analytics Features*, 21 May 2026, <https://www.law.com/legaltechnews/2026/05/21/harvey-announces-contract-review-product-adoption-analytics-features/>.
