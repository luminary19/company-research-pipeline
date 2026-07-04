---
type: Gather Report
topic: company
slice: traction-metrics
date: 2026-07-04
rounds_run: 3
stop_reason: Coverage saturated across all 5 sub-questions; max rounds reached; diminishing returns (later sources merely repeat Harvey-self-reported figures). Headcount conflict and full ARR trajectory both resolved.
---

## Scope

Traction and growth metrics for Harvey (harvey.ai), the legal-AI startup founded 2022 by Winston Weinberg (CEO) and Gabriel/Gabe Pereyra. Captures revenue/ARR trajectory, customer counts, users/usage, headcount, and growth/efficiency signals — each metric with its source, publication date, and the as-of date of the figure, flagging every figure that originates with Harvey (self-reported, unaudited).

**Critical caveat carried through this whole report:** essentially every traction figure below traces to Harvey itself (blog posts, press releases, or CEO/co-founder interviews) and is repeated by third-party outlets. Under the grading rule, **any figure originating from Harvey alone caps at C3** (self-reported, single origin) even when many outlets echo it. R1 here means "R1 that *Harvey claims it*," not that it is audited. Only where a genuinely independent third party generated the number (e.g., GetLatka's own $65.8M 2024 estimate, or scraper headcounts) is it noted as such.

EXCLUDED per brief: funding-round table / valuations, legal identity/offices, product-feature depth, competitors, people-dossier org analysis.

---

## Findings

### 1. Revenue / ARR trajectory

All ARR figures are Harvey-self-reported unless flagged otherwise.

| As-of date | Figure | Exact wording | Source (date) | Origin |
|---|---|---|---|---|
| Founding (Nov 2022) | $0 | "launched in November 2022 with zero revenue" | GetLatka (2025-08-05) | 3rd-party framing |
| April 2022 → Dec 2023 | "10x" growth | "increased revenue over 10x in 2023"; "revenue has climbed 10x since April to around $10 million" | OpenAI post (openai.com/index/harvey); Zaven blog (2023-12-22) | **Harvey-self-reported** |
| End 2023 | ~$10M ARR | "By the end of 2023, they hit $10 million in annual recurring revenue" | GetLatka (2025-08-05) | 3rd-party (GetLatka) |
| FY2024 | "4x ARR growth" | "In 2024, we saw 4x annual recurring revenue (ARR) growth" | **Harvey Series D blog** (2025-02-12) | **Harvey-self-reported (R1 for the claim)** |
| FY2024 (conflict) | $65.8M | "Harvey reached $65.8 million – a 558% year-over-year increase, according to GetLatka data" | GetLatka (2025-08-05) | 3rd-party estimate (GetLatka) |
| August 2025 | $100M ARR | "$100m ARR"; "surpassed $100 million in annual recurring revenue as of August" | Artificial Lawyer (2025-08-04); TechCrunch (2025-11-14) | **Harvey-self-reported** |
| Jan 2026 / "end of 2025" | $190M ARR | "hitting $190m ARR since its launch three years ago"; "hit an annual recurring revenue rate of $190 million by the end of 2025, founder CEO Winston Weinberg shared on LinkedIn"; "hit $190 million ... in January, up from the $100 million figure it announced in August" | Artificial Lawyer (2026-01-08); TechCrunch (2026-02-09); CNBC (2026-03-25) | **Harvey-self-reported (Weinberg LinkedIn)** |
| "$100M → $190M" | ~doubling in ~4–6 months | "nearly double the contracted revenue in less than six months"; "nearly doubling revenue in five months" | TechCrunch (2026-02-09); multiple | Harvey-derived |
| March 2026 | ">$200M annualized" | "had more than $200 million in annualized revenue at the time" (Business Insider, March) | Startup Fortune (2026-06-19), citing Business Insider | Harvey via Business Insider |
| ~June 2026 | "$300M ARR" | "At $300M ARR and an $11 billion valuation, the legal AI company has moved past the pilot phase" | Startup Fortune (2026-06-19) | **Aggregator framing — LOW confidence, uncorroborated; treat as a claim, not confirmed** |

**CONFLICT on FY2024 ARR:** Harvey's own Series D blog says "**4x** ARR growth" in 2024 (≈$40M if applied to the ~$10M end-2023 base). GetLatka's independent estimate says Harvey hit **$65.8M** in 2024, a "**558%** (≈6.6x) YoY increase." Both are recorded; Harvey's is the self-reported growth multiple, GetLatka's is a third-party dollar estimate. The brief's "~$50M ARR (2024?)" sits between these two and is not directly sourced to any single primary statement.

**Note on the $300M June-2026 figure:** appears only in a Startup Fortune headline/lede (aggregator). The same article's own body cites Business Insider for ">$200M annualized" as of March 2026. Flag as unverified / possibly the outlet's extrapolation.

### 2. Customers

**Customer-count trajectory (org-level "customers/clients," not seats):**

| As-of | Count | Exact wording | Source (date) | Origin |
|---|---|---|---|---|
| Start of 2024 | 40 | "expanded from 40 customers to 235 customers in 42 countries" | Harvey Series D blog (2025-02-12) | **Harvey-self-reported** |
| End 2024 | 235 (in 42 countries) | same as above; "including the majority of the top 10 US law firms" | Harvey Series D blog (2025-02-12) | **Harvey-self-reported** |
| Aug 2025 | 500+ (in 54 countries) | "more than 500 customers in 54 countries" | Artificial Lawyer / Harvey (2025-08-04) | **Harvey-self-reported** |
| Nov 2025 | 700 (in 63 countries) | "the startup now claims 700 clients across 63 countries" | TechCrunch (2025-11-14) | **Harvey-self-reported** |
| Dec 2025 | 700+ | "More than 700 leading law firms and enterprises ... representing over 74,000 attorneys" | SiliconANGLE Series F (2025-12-04) | **Harvey-self-reported** |
| Jan 2026 | 1,000 | "reached 1,000 clients in total" | Artificial Lawyer (2026-01-08) | **Harvey-self-reported** |
| Mar 2026 | 1,300+ (in 60+ countries) | "More than 100,000 lawyers across 1,300 organizations"; "used by 1,300+ customers in 60+ countries" | Harvey $11B blog (2026-03-25) | **Harvey-self-reported** |
| ~mid-2026 | 1,500 firms/enterprises | "used by more than 100,000 lawyers across 1,500 law firms and enterprises" | Startup Fortune (2026-06-19), citing Harvey/Business Insider | **Harvey-self-reported** |
| Live (fetched 2026-07-04) | 1,500+ organizations | "More than 142,000 lawyers across 1,500+ organizations in 60 countries" | harvey.ai/customers (live) | **Harvey-self-reported** |

**What counts as a "customer":** organization-level (law firm or enterprise/in-house team), NOT seats. Harvey consistently reports "customers"/"clients"/"organizations" separately from "lawyers"/"professionals" (the seat/user count). The customers page header (live) explicitly pairs "142,000+ lawyers" (users) with "1,500+ organizations" (customers).

**AmLaw-100 penetration — CONFLICT (all three values captured):**
- **"42% of the AmLaw 100"** — "$100m ARR and over 500 customers globally, including 42% of the AmLaw 100 law firms" — Artificial Lawyer / Harvey (2025-08-04). Also repeated by StartupIntros. **Harvey-self-reported.**
- **"50 of the top 100" / "over 50%" / "more than half"** — "Top Firms Trust it — 50 of AmLaw 100" (XYZEO, 2026-02-02); "74,000+ attorneys across 50 of the AmLaw 100" (PulseMark, 2026-01-06); "used by more than half of the 100 largest law firms in the country" (CNBC Disruptor 50, 2026-05-19); "over 50% of AmLaw 100 law firms" (LeadIQ boilerplate). **Harvey-self-reported (echoed).**
- **"majority of the AmLaw 100"** — "now partnering with the majority of the AmLaw 100" — Harvey $11B blog (2026-03-25). **Harvey-self-reported.**
- Reconciliation note: these are consistent with a rising trajectory (42% Aug 2025 → ~50% winter 2025/26 → "majority" Mar 2026), not necessarily contradictory — but the exact figure and date differ by source, so all three are surfaced.

**Magic Circle / global-firm penetration:** "majority of the top 10 US law firms" (Series D blog Feb 2025; TechCrunch Nov 2025). A&O Shearman (ex-Allen & Overy) was first major enterprise customer (beta Nov 2022, firmwide Feb 2023, ~3,500 → ~4,000 lawyers post-merger). Named global/Magic-Circle-adjacent logos: A&O Shearman, Latham & Watkins (~3,600 lawyers), Paul Weiss (early adopter, began testing Jan 2023), Ashurst (~4,000 lawyers + business services), CMS (firmwide across 21 member firms in 50+ countries, Dec 2025; "95% adoption" case study), Cuatrecasas, Reed Smith, DLA Piper International, Corrs Chambers Westgarth, McCann Fitzgerald (firmwide 2026), WongPartnership (first SE-Asian firm to test, Sept 2024), Hengeler Mueller, Gleiss Lutz, A&L Goodbody, Maples Group, Macfarlanes, O'Melveny, LPHS.

**In-house / corporate legal counts:**
- "over 500 in-house teams" / "over 500 in-house legal teams" — Harvey blog "Helping Law Firms and Companies Collaborate" (2026-03-13) and $11B blog (2026-03-25). **Harvey-self-reported.**
- "50 asset management firms" — $11B blog (2026-03-25). **Harvey-self-reported.**
- Live customers page (2026-07-04) also shows "20+" in-house legal teams stat block (ambiguous — likely a specific sub-segment, not total; homepage lists "20+" adjacent to "142,000+" and "60"). Recorded but flagged as ambiguous.
- Named marquee in-house/enterprise logos: HSBC (strategic AI partnership, Global Legal, Jan 2026), NBCUniversal (2026), Comcast, Verizon, AT&T, Cox, Koch, KKR, Bridgewater, Carvana, PwC (tax/legal partnership), Deutsche Telekom, Dentsu, Dentsu.

### 3. Users / usage

| As-of | Metric | Exact wording | Source (date) | Origin |
|---|---|---|---|---|
| Aug 2025 | WAU 4x / 6x | "Our Weekly Active Users (WAU) grew 4x in the past year and 6x the year prior" | Artificial Lawyer / Harvey (2025-08-04) | **Harvey-self-reported** |
| Aug 2025 | Monthly queries 5.5x | "Monthly queries grew 5.5x in the past year" | Artificial Lawyer / Harvey (2025-08-04) | **Harvey-self-reported** |
| Aug 2025 | Active files 36x (268K → 9.75M) | "active files stored in Harvey grew 36x in the past year from 268K to 9.75M" | Artificial Lawyer / Harvey (2025-08-04) | **Harvey-self-reported** |
| Nov/Dec 2025 | 74,000+ attorneys | "More than 700 leading law firms and enterprises ... representing over 74,000 attorneys"; "74,000+ active lawyers" | SiliconANGLE (2025-12-04); XYZEO/PulseMark (Jan–Feb 2026) | **Harvey-self-reported** |
| Mar 2026 | 100,000+ lawyers, 60 countries | "More than 100,000 lawyers around the world run their most critical work on Harvey"; "100,000 lawyers across 1,300 organizations" | Harvey $11B blog + Sequoia quote (2026-03-25) | **Harvey-self-reported** |
| Mar 2026 | 25,000+ custom agents | "More than 25,000 custom agents operate on Harvey" | Harvey $11B blog (2026-03-25) | **Harvey-self-reported** |
| ~May–Jun 2026 | 100,000+ lawyers / 1,500 firms / 60+ countries | "used by more than 100,000 lawyers across 1,500 law firms and enterprises" spanning "more than 60 countries" (WSJ) | Startup Fortune (2026-06-19) via Business Insider/WSJ | **Harvey-self-reported** |
| Live (2026-07-04) | 142,000+ professionals | "More than 142,000 lawyers across 1,500+ organizations in 60 countries"; homepage "142,000+"; "Professionals using Harvey 142,000+" | harvey.ai/customers + harvey.ai (live) | **Harvey-self-reported** |

**Prompt/token volume & task throughput (mid-2026):**
- **1 trillion tokens in January (2026) → 12–13 trillion tokens in May (2026)** — "CEO Winston Weinberg said on the Sourcery with Molly O'Shea podcast that Harvey used 1 trillion tokens in January and was on pace for 12 trillion to 13 trillion tokens in May" — Startup Fortune / Yahoo Finance (2026-06-19), citing Business Insider. Yahoo headline: "AI usage jumped from 1 trillion tokens a month to 12 trillion." **Harvey-self-reported (CEO).**
- **700,000+ agent-powered tasks/day** — "Harvey users run more than 700,000 agent-powered tasks a day" — Business Insider via Startup Fortune (2026-06-19); AI Vortex separately says "processes over 700,000 tasks daily." **Harvey-self-reported.**
- **Hours in software per user +75% over four months** — "hours spent in the software per user rose 75% over four months" — Business Insider via Startup Fortune (2026-06-19). **Harvey-self-reported.**
- ~500 AI agents rolled out + redesigned Agent Builder (May 2026, Business Insider).
- The brief's phrasing "billions of prompt tokens, millions of daily requests" was NOT found verbatim; the closest sourced figures are the trillions-of-tokens/month and 700K tasks/day above (an order of magnitude larger). Flagged in Gaps.

### 4. Headcount over time — CONFLICT RESOLVED (with a second conflict on 2026)

**Editorial / self-reported trajectory (consistent):**
| As-of | Headcount | Exact wording | Source (date) |
|---|---|---|---|
| Founding (Nov 2022) | 5 | "just 5 employees"; KP: "scaled their spectacular team from 5 to over 50" | GetLatka (2025-08-05); Kleiner Perkins (2023-12-19) |
| ~end 2023 | "over 50" | "from 5 to over 50" in the past year | Kleiner Perkins (2023-12-19) |
| ~end 2023 / early 2024 | "over 100" | "They've grown to a team of over 100 people" | **OpenAI post** (openai.com/index/harvey) |
| March 2024 | 82 | "grew from 5 employees at founding to 82 by March 2024" | GetLatka (2025-08-05) |
| Mid-2025 | 340+ / "over 350" | "over 340 by mid-2025"; "a team of over 350 people"; "340+ employees, plans to double" | GetLatka; Artificial Lawyer (2025-08-04); mmntm (2025-12-15) |
| Aug 2025 | 350 | "350 employees, 500 customers, $100M revenue" | TBPN Digest (2025-08-05) |
| Nov 2025 | ~400 | "With around 400 employees, how close are you to break-even?" | TechCrunch (2025-11-14) |
| Early 2026 | ~350 | "~350 employees"; "grew from roughly 100 employees to ~350 in a single year" | JobsByCulture (2026-04-11); StartupIntros |

**Reconciling the brief's conflict:** The brief's "~82 [websets, early 2025]" matches GetLatka's "**82 by March 2024**" (the same data-provider snapshot; the *date* attribution differs — GetLatka puts it at Mar-2024, not early-2025). The "~100 [OpenAI post, 2023]" and the "82 [Mar 2024]" are close in time and mildly conflict (OpenAI's "over 100" vs the scraper's 82) — both recorded. "~350 [mid-2025]" is well-corroborated. So the clean editorial trajectory is: **5 (2022) → ~50–100 (end 2023) → 82 (Mar 2024) → 340–350 (mid-2025) → ~400 (Nov 2025) → ~350 (early 2026)**. Harvey stated (twice) intent to "double headcount" after the Series B (Dec 2023) and again after the Series E (June 2025).

**SECOND CONFLICT — scraper aggregators vs editorial (2026):** Data-provider scrapers report far higher 2026 headcounts than editorial sources:
- LeadIQ: "approximately **1.1K** employees as of March 2026" (1001–5000 band).
- Tracxn: "**1,441** employees as of May 31, 2026."
- vs JobsByCulture/StartupIntros editorial: "**~350** as of early 2026."
This is a large unreconciled gap (~350 self-reported/editorial vs 1,100–1,441 scraped). Likely the scrapers over-count (LinkedIn profiles listing Harvey, contractors, or lag), but it is not resolvable from these sources. Both surfaced; scrapers graded R4.

**">20% are lawyers" claim:** Not found as a precise percentage. Closest sourced: Weinberg to Fortune (via GetLatka, 2025-08-05): "We have tons of lawyers on staff designing and evaluating the product, and they're all from large law firms or from large in-house teams." The specific ">20%" figure is NOT sourced here — flagged in Gaps.

### 5. Growth / efficiency signals

**Revenue mix / expansion (law firm vs corporate) — a clear expansion signal, Harvey-self-reported:**
- Weinberg (TechCrunch, 2025-11-14): "At the beginning of this year [2025], about **4% of our revenue was from corporates and 96% from law firms**. Right now, **33%** of our revenue is from corporates, and my gut says, by the end of the year, that looks closer to **40%**."
- TBPN Digest headline (2026-01-08): "Harvey CEO Winston Weinberg on expanding beyond big law as **41% of revenue now comes from corporates**."
- Named renewals/expansions (proxy for net expansion): CMS, Hengeler Mueller, DLA Piper ("renewals and expansion with the likes of CMS and Hengeler Mueller and DLA Piper" — Weinberg, Artificial Lawyer 2026-01-08); CMS firmwide across 21 member firms / 50+ countries (Dec 2025); DLA Piper International "expanding their work"; McCann Fitzgerald "going firmwide."
- **No explicit net revenue retention (NRR) / dollar-based expansion percentage was reported** in any source found — flagged in Gaps.

**Usage-intensity signals (all Harvey-self-reported):** WAU 4x/6x; monthly queries 5.5x; active files 36x (268K→9.75M) [all Aug 2025]; token consumption ~12–13x (1T→12–13T tokens/mo, Jan→May 2026); hours/user +75% over 4 months; 700K agent tasks/day. Adoption stats on live customers page: "Monthly adoption rate 92%" (customers page) / "95% adoption" (CMS case study) / "20+ hours saved per user per month" (aiforautomation: "Average user saves 20+ hours per month"; customers page: "25+" hours saved per typical user/month — note internal inconsistency between the two figures).

**Revenue-per-employee (DERIVED from sourced figures — arithmetic and inputs stated; not reported by Harvey):**
- Aug 2025: $100M ARR (Harvey, Aug 2025) ÷ 350 employees (TBPN Digest, Aug 2025) = **~$286K ARR/employee**.
- Nov 2025: $100M ARR (as of Aug) ÷ ~400 employees (TechCrunch, Nov 2025) = **~$250K ARR/employee**.
- Jan 2026: $190M ARR (Harvey, Jan 2026) ÷ ~350–400 employees (early-2026 editorial range) = **~$475K–$543K ARR/employee**.
- These are back-of-envelope from non-simultaneous inputs (ARR and headcount reported weeks apart) and use editorial headcounts, NOT the scraper figures (which would cut the ratio ~3–4x). Directional only.

**Burn / runway commentary (Harvey-self-reported, Weinberg TechCrunch 2025-11-14):**
- "Fundraising large rounds is not something we have planned anytime soon. **We don't need that much money, and we aren't burning a crazy amount.** The reason I did a lot of fundraising this year is there are research directions that are going to require a lot of compute."
- On margins: "Our margins **look very good on a token basis**, but they're worse because we have to spend so much on **upfront compute** across so many jurisdictions [60+ countries with data-residency laws]. That will get solved over time."
- Weinberg on the cost question (Business Insider via Startup Fortune, 2026-06-19): "I just spent $1 billion on tokens. Where's my ROI?" — framed as the open pricing/margin question; the outlet notes Harvey's risk is pricing (seat-based) not capturing per-matter value.
- Artificial Lawyer (Aug 2025) context: investors "are not at all expecting to hit profitability any time soon" given the scale of VC investment (~$600M raised that year at that point).

---

## Reflection trace

- **Round 1** (2 searches + 1 crawl): search A (ARR/$190M/CNBC/Sequoia) and search B (customers/AmLaw/users) returned nearly the entire spine — $100M (Aug 2025) and $190M (Jan 2026) ARR, customer trajectory to 1,300+/1,500+, AmLaw conflict (42% vs 50 vs majority), 74,000/100,000/142,000 users, 350-employee figure. Crawled the 5 richest primary/detailed sources (Harvey $11B blog, both Artificial Lawyer pieces, live customers page, TBPN Digest) at 1M chars → captured exact wording, the Aug-2025 usage stats (WAU/queries/files), and surfaced the "41% corporate revenue" lead.
- **Round 2** (2 searches + 1 crawl): targeted the *early* trajectory + usage volume + headcount. Landed the OpenAI post ("10x, over 100 people"), Series B/D specifics, and crucially the **1T→12–13T token** surge, **700K tasks/day**, and the **4%→33%→41% corporate revenue mix**. Crawled Series D blog (primary: 40→235, 4x ARR 2024), TechCrunch Nov-2025 (primary: ~400 employees, 700 clients/63 countries, burn/margin commentary, corporate-mix quote), Startup Fortune (token surge, $300M-ARR framing), SiliconANGLE (Series F: 74,000 attorneys).
- **Round 3** (1 search): headcount reconciliation. GetLatka delivered the clean trajectory (5 → 82 Mar-2024 → 340+ mid-2025) AND a 2nd revenue estimate ($65.8M 2024, conflicting with Harvey's "4x"). Also exposed the scraper-vs-editorial 2026 headcount conflict (LeadIQ 1.1K / Tracxn 1,441 vs editorial ~350). Stopped: all five sub-questions saturated, remaining sources merely re-echo Harvey figures.

## Gaps and not-found

- **"Billions of prompt tokens, millions of daily requests"** (brief's phrasing): not found verbatim. Sourced volume is far larger and framed differently — trillions of tokens/month and 700K agent-tasks/day (mid-2026). The brief's phrasing may be an older/different framing; not corroborated.
- **">20% of staff are lawyers":** precise percentage not sourced. Only the qualitative "tons of lawyers on staff" (Weinberg/Fortune) was found.
- **Net revenue retention / dollar-based expansion %:** not reported by any source; only qualitative renewal/expansion signals (named accounts) and the corporate-mix shift.
- **FY2024 ARR exact dollar figure:** conflicting — Harvey's own "4x growth" (implies ~$40M) vs GetLatka's "$65.8M." No single primary $-figure for end-2024 ARR from Harvey directly.
- **$300M ARR (June 2026):** appears only in a Startup Fortune aggregator header; the same article's body cites ">$200M annualized" (Business Insider, March). Treat as unverified.
- **2026 headcount:** unresolved 3–4x gap between editorial (~350) and scrapers (1,100–1,441). Business Insider/WSJ/Fortune primary interviews were reached only secondhand (via aggregators/Yahoo syndication), not fetched directly — a follow-up could pull the Business Insider "Sourcery" coverage and the WSJ pieces firsthand.
- **In-house "20+" vs "500+":** the live homepage "20+" in-house stat conflicts with the blog's "over 500 in-house teams" — likely different segment definitions; not reconciled.
- **Hours-saved stat:** customers page "25+/month" vs aiforautomation "20+/month" — minor internal inconsistency.

## Sources consulted (with grades)

**Primary / Harvey-official (R1 for the claim; C3 cap — self-reported, unaudited):**
- Harvey $11B blog, harvey.ai/blog/harvey-raises-at-dollar11-billion-valuation... (2026-03-25) — 25,000 agents, 100,000 lawyers, 1,300 orgs, majority AmLaw 100, 500+ in-house, 50 asset mgmt, 60 countries. [R1·C3]
- Harvey Series D blog, harvey.ai/blog/harvey-raises-series-d (2025-02-12) — 4x ARR 2024, 40→235 customers/42 countries, majority top-10 US firms. [R1·C3]
- Harvey Series B blog, harvey.ai/blog/series-b (2023-12-19). [R1·C3]
- Harvey Series A blog, harvey.ai/blog/sequoia-and-openai-back-harvey... (2023-04-26). [R1·C3]
- Harvey customers page, harvey.ai/customers (live, fetched 2026-07-04) — 142,000+ lawyers, 1,500+ orgs, 60 countries, 92% adoption, 25+ hrs saved. [R1·C3]
- Harvey homepage, harvey.ai (live, 2026-05/07) — 142,000+, 60, "20+" in-house. [R1·C3]
- Harvey "Helping Law Firms and Companies Collaborate" blog (2026-03-13) — 1,000+ customers/60 countries, 50% AmLaw 100, 500+ in-house teams. [R1·C3]
- OpenAI post, openai.com/index/harvey — "10x revenue 2023," "over 100 people." (Harvey figures via OpenAI, a partner/investor.) [R2·C3]
- Kleiner Perkins, kleinerperkins.com/perspectives/harvey-ai (2023-12-19) — "5 to over 50," "revenue 10x." (Investor.) [R2·C3]

**Independent reporting of Harvey figures (R2; still C3 where the number originates with Harvey):**
- CNBC, "$200M at $11B valuation" (2026-03-25) — $190M ARR (Jan), up from $100M (Aug). [R2·C3]
- CNBC Disruptor 50 #24 (2026-05-19) — "more than half of the 100 largest law firms." [R2·C3]
- TechCrunch, "Inside Harvey" (2025-11-14) — ~400 employees, 700 clients/63 countries, $100M ARR Aug, corporate-mix 4%→33%→~40%, burn/margin. [R2·C3]
- TechCrunch, "$11B ... months after $8B" (2026-02-09) — $190M ARR by end-2025 (Weinberg LinkedIn), ~doubling. [R2·C3]
- Artificial Lawyer, "$100m ARR + 42% AmLaw 100" (2025-08-04) — $100M ARR, 500+ customers/54 countries, WAU 4x/6x, queries 5.5x, files 36x, 350 people. [R2·C3]
- Artificial Lawyer, "$190m ARR + Memory" (2026-01-08) — $190M ARR, 1,000 clients, renewals CMS/Hengeler/DLA. [R2·C3]
- Artificial Lawyer, "CMS expands ... 50+ countries" (2025-12-10). [R2·C3]
- SiliconANGLE, Series F (2025-12-04) — 700+ firms, 74,000+ attorneys, $8B. [R2·C3]
- Yahoo Finance, "1 trillion → 12 trillion tokens" (2026-06-19) — CEO on Sourcery podcast. [R2·C3]

**Trade press / interview digests / aggregators (R3):**
- TBPN Digest (2025-08-05) — 350 employees/500 customers/$100M; (2026-01-08 headline) 41% corporate revenue. [R3·C3]
- Startup Fortune, "12x token surge" (2026-06-19) — 1T→13T tokens, 700K tasks/day, +75% hrs/user, 1,500 firms, "$300M ARR" (aggregator framing), ">$200M annualized" via Business Insider. [R3·C3, $300M figure C4]
- GetLatka, "$100m in 36 months" (2025-08-05) — $10M (2023), $65.8M (2024, GetLatka est.), 5→82(Mar-2024)→340+ headcount, "lawyers on staff" quote. [R3; GetLatka's own $ estimate 3rd-party]
- StartupIntros, startupintros.com/orgs/harvey — ~350 employees, 40→235, 100,000+ pros, 42% AmLaw. [R3·C3]
- mmntm.net deep dive (2025-12-15) — 340+ mid-2025, 42–50% AmLaw, $100M+ ARR. [R3·C3]
- JobsByCulture (2026-04-11) — ~350 employees, ~100→350 in a year, $190M ARR. [R3·C3]
- PulseMark (2026-01-06), XYZEO (2026-02-02), AI Vortex (2026-04-17) — 74,000 attorneys, 50 of AmLaw 100, 700+ firms, 700K daily tasks. [R3·C3]
- SaaS Sentinel, TechStartups, AI for Automation, AI Business Weekly, AI Automation Global, JuggerInsight, Silicon Valley Investclub, TechFundingNews — echo $190M ARR / 100,000 lawyers / 1,300 orgs. [R3·C3]
- Zaven blog (2023-12-22), AiCoin (2024-01-04) — ~$10M ARR / 10x since April. [R3·C3]

**Scraper / directory aggregators (R4 — headcount only, conflicting):**
- LeadIQ — ~1.1K employees (Mar 2026). [R4]
- Tracxn — 1,441 employees (May 31, 2026). [R4]
- Bitscale, PitchBook — profile/headcount (no usable headcount detail returned). [R4]
