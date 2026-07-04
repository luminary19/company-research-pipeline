---
type: Gather Report
topic: company
slice: identity-history
date: 2026-07-04
rounds_run: 2
stop_reason: named gaps exhausted / diminishing returns; all four sub-questions covered with primary sources (SEC EDGAR + USPTO for identity, official harvey.ai pages for mission). Only residual not-found is the direct CA SoS / OpenCorporates entity-number lookup (bot-blocked), which SEC/USPTO primary data supersedes.
---

## Scope

GATHER slice = **identity + history + footprint** for Harvey (harvey.ai). Four sub-questions: (1) legal identity, (2) verifiable founding-story facts, (3) milestone timeline, (4) official mission/self-description. Excluded (sibling slices): funding-round table / cap table, ARR/user/customer metrics, thesis, product features, competitor detail, people-org analysis. Findings are organized, not concluded; every finding carries an openable URL and an [R·C] grade. No confidence tags assigned. Anchored to harvey.ai / Counsel AI Corporation / Weinberg + Pereyra; the separate SEC entity **"General Counsel AI, Inc." (CIK 0002036281) is NOT Harvey** and was excluded.

Grading key: R1 authoritative (SEC/registers, USPTO, official Harvey pages, primary partner press releases); R2 credible press; R3 practitioner blogs / data aggregators; R4 weak. C1 2+ independent, C2 consistent, C3 single-source, C4 contested.

---

## Findings

### 1. Legal identity

- **Legal entity (SEC): "Harvey AI Corp", formerly "Counsel AI Corp"** — SEC EDGAR registrant CIK 0001974654 lists current name **Harvey AI Corp** with formerNames **["Counsel AI Corp"]**. This is primary-source evidence of the **Counsel AI → Harvey rename** at the corporate level. `[R1·C1]` https://data.sec.gov/submissions/CIK0001974654.json | company filings: https://www.sec.gov/cgi-bin/browse-edgar?action=getcompany&CIK=0001974654&type=&dateb=&owner=include&count=40
- **State of incorporation: Delaware.** SEC entity metadata `stateOfIncorporation: DE`; Form D field `jurisdictionOfInc: DELAWARE`. `[R1·C1]` https://www.sec.gov/Archives/edgar/data/1974654/000197465424000004/xslFormDX01/primary_doc.xml
- **Year of incorporation: 2022.** Form D (filed 2024-07-30) `yearOfInc`: `withinFiveYears: true, value: 2022`. `[R1·C1]` (same Form D URL above)
- **EIN 88-3448544; SEC CIK 0001974654.** `[R1·C3]` https://data.sec.gov/submissions/CIK0001974654.json
- **Registered/HQ business address: 201 Third Street, Suite 500, San Francisco, CA 94103.** SEC business address. (Minor variants elsewhere: CB Insights lists "201 3rd Street Suite 600"; a LinkedIn aggregate lists "575 Market Street, Suite 2800" as a second SF address — treat SEC's Suite 500 as authoritative.) `[R1·C2]` https://data.sec.gov/submissions/CIK0001974654.json
- **Trademark identity — "HARVEY", owned by "Counsel AI Corporation":** two US applications both filed **2022-11-23**:
  - Serial **97690544** — Intl Class **042**, "Software-as-a-service (SAAS) services, namely, providing online non-downloadable tools for assisting with legal research and writing"; Legal Entity Type "03 - Corporation"; status "630 - New Application"; correspondent attorney **John Paul Oleksiuk**. `[R1·C2]` https://trademarks.justia.com/976/90/harvey-97690544.html (USPTO TSDR: https://tsdr.uspto.gov/#caseNumber=97690544&caseType=SERIAL_NO&searchType=statusSearch )
  - Serial **97690542** — "Legal information services", owned by Counsel AI Corporation, filed 2022-11-23. `[R1·C2]` https://trademarks.justia.com/976/90/harvey-97690542.html (Justia detail page 403'd on fetch; summary confirmed via Justia search results.)
  - Note the naming reconciliation: SEC = "Counsel AI Corp" → now "Harvey AI Corp"; USPTO owner-of-record = "Counsel AI Corporation"; Wikipedia treats "Harvey" (product) as operated by parent "Counsel AI Corporation." Same entity across sources.
- **Third-party corroboration of the rename:** CB Insights — "Harvey was formerly known as Counsel AI. It was founded in 2022 and is based in San Francisco." `[R2·C2]` https://www.cbinsights.com/company/harvey-2
- **Named after Suits' Harvey Specter.** Wikipedia: "It is named after the lead character of the legal drama Suits, Harvey Specter." (Corroborated Forbes AU, Guy Louzon.) `[R3·C1]` https://en.wikipedia.org/wiki/Harvey_(software)
- **CONFLICT (entity name suffix):** SEC uses "Corp" (now "Harvey AI Corp"); USPTO uses "Corporation" ("Counsel AI Corporation"). Recorded — likely stylistic abbreviation of the same corporation, not two entities.

### 2. Founding story — verifiable facts

- **Founders: Winston Weinberg (CEO) and Gabriel Pereyra (President).** Both listed on the SEC Form D as **"Executive Officer, Director."** Other Form D related persons: Pat Grady (Director; Sequoia), Ilya Fushman (Director; Kleiner Perkins), John LaBarre (Executive Officer, Director). `[R1·C1]` https://www.sec.gov/Archives/edgar/data/1974654/000197465424000004/xslFormDX01/primary_doc.xml ; also Wikipedia infobox `[R3·C1]` https://en.wikipedia.org/wiki/Harvey_(software)
- **When founded: 2022 (summer / July).** Wikipedia "founded in the summer of 2022"; StartupRiders "In July 2022"; SEC year-of-incorporation 2022. `[R1·C1]` (SEC, above) + https://www.startupriders.com/p/harvey-ai-growth-playbook
- **Weinberg pre-history: first-year litigation associate at O'Melveny & Myers (securities/antitrust), LA office; USC Gould School of Law.** O'Melveny confirmed by Wikipedia, TechCrunch, StartupRiders, Guy Louzon; "O'Melveny & Myers in Los Angeles" per StartupRiders; USC Gould per Guy Louzon (sole source for the law school). `[R2·C1 O'Melveny] / [R3·C3 USC Gould]` https://techcrunch.com/2025/11/14/inside-harvey-how-a-first-year-legal-associate-built-one-of-silicon-valleys-hottest-startups/ ; https://guylouzon.substack.com/p/harvey-ai-when-an-omelveny-litigator
- **Pereyra pre-history: research scientist at DeepMind / Google Brain, then Meta AI (FAIR).** Consistent across Wikipedia ("Google DeepMind and Meta"), Guy Louzon ("Meta AI… before that, Google Brain and DeepMind… Google Brain and DeepMind in 2016-2017"), StartupRiders ("DeepMind and Meta… friends from Google Brain"). Forbes AU also pins Pereyra to a **USC Computer Science** background ("the USC Computer Science major"). `[R2·C1 DeepMind/Meta] / [R2·C3 USC CS]` https://www.forbes.com.au/news/innovation/what-is-harvey-ai-the-legal-tech-decacorn-changing-how-lawyers-work/
- **Origin = cold email to Sam Altman and Jason Kwon (OpenAI GC).** Multiple sources: "We cold-emailed Sam Altman and Jason Kwon, who was the general counsel at OpenAI. We figured we had to email a lawyer because otherwise the person wouldn't know if the outputs were right." (TechCrunch; same framing Wikipedia, Guy Louzon.) `[R2·C1]` (TechCrunch URL above)
  - **Email subject line (single source):** "Did you know it was this good at legal?" — StartupRiders only. `[R3·C3]` https://www.startupriders.com/p/harvey-ai-growth-playbook
- **July 4, 2022 pitch to OpenAI C-suite; OpenAI Startup Fund became seed investor; early GPT-4 access.** Wikipedia: "on July 4, 2022, they met with OpenAI's C-suite, and OpenAI became their seed investor… early access to GPT-4." TechCrunch: "On the morning of July 4 at 10 a.m.… we made our pitch." `[R2·C1]` (Wikipedia + TechCrunch URLs above)
- **The 86/100 landlord-tenant validation test.** "We created this super long chain-of-thought prompt over California landlord-tenant statutes. We grabbed 100 questions from r/legaladvice [on Reddit]… gave the question-answer pairs to three landlord-tenant attorneys without saying anything about AI… On 86 of the 100 samples, two out of three attorneys or more said they would send it with zero edits." (TechCrunch.) Corroborated near-verbatim by Wikipedia (100 questions, three attorneys, 86 approved), StartupRiders ("86 out of 100 answers passed"), Guy Louzon. `[R2·C1]` (TechCrunch URL above)
- **CONFLICT — founding CITY (SF vs San Diego vs Los Angeles). Recorded:**
  - **San Francisco:** SEC business location = San Francisco, CA (the incorporated HQ) https://data.sec.gov/submissions/CIK0001974654.json ; TechCrunch "The San Francisco-based company…" ; StartupRiders "cold-emailed Sam Altman from their shared apartment in San Francisco" ; Forbes AU body "Harvey was founded in San Francisco in 2022" ; Wikipedia HQ "San Francisco, California."
  - **San Diego:** Forbes AU standfirst "built the legal AI platform from the living room of their San Diego sharehouse"; body "his roommate in San Diego, lawyer Winston Weinberg…"; "the San Diego roommates." https://www.forbes.com.au/news/innovation/what-is-harvey-ai-the-legal-tech-decacorn-changing-how-lawyers-work/ (Forbes AU is internally contradictory: SF founding vs. San Diego sharehouse.)
  - **Los Angeles:** Wikipedia History "Pereyra and Weinberg were roommates in Los Angeles"; Guy Louzon "It's early 2022, somewhere in Los Angeles"; Weinberg (TechCrunch/Guy Louzon) "running a Dungeons and Dragons game with friends in LA"; and Weinberg's O'Melveny job was in LA (StartupRiders).
  - Distinction worth noting: the **incorporated business/HQ is San Francisco (primary, SEC)**, while the **pre-incorporation roommate-apartment location is disputed** among SD / LA / SF across secondary sources.

### 3. Milestone timeline

- **Nov 2022 — seed round emerges from stealth (OpenAI Startup Fund-led); A&O begins trialing Harvey.** Seed reported 23 Nov 2022 (LawSites). A&O trial started Nov 2022 within its Markets Innovation Group (MIG). `[R2·C1]` https://www.lawnext.com/2022/11/stealth-legal-ai-startup-harvey-raises-5m-in-round-led-by-openai.html
- **Feb 15–16, 2023 — Allen & Overy exclusive launch partnership / firmwide rollout.** Primary partner press release: "Allen & Overy… has broken new ground by integrating Harvey… Harvey will empower more than 3,500 of A&O's lawyers across 43 offices operating in multiple languages." Trial (since Nov 2022): ~3,500 lawyers asked ~40,000 queries; used in 50 languages / 250 practice areas. `[R1·C1]` https://www.aoshearman.com/en/news/ao-announces-exclusive-launch-partnership-with-harvey ; press coverage https://www.lawnext.com/2023/02/as-allen-overy-deploys-gpt-based-legal-app-harvey-firmwide-founders-say-other-firms-will-soon-follow.html
- **Mar 15, 2023 — PwC global strategic alliance** (exclusive among the Big Four): "PwC announced a global partnership with artificial intelligence (AI) startup Harvey… access for PwC's… professionals across 100+ countries… 4,000 legal professionals." Primary PwC press release. `[R1·C1]` https://www.pwc.com/gx/en/news-room/press-releases/2023/pwc-announces-strategic-alliance-with-harvey-positioning-pwcs-legal-business-solutions-at-the-forefront-of-legal-generative-ai.html ; UK version https://www.pwc.co.uk/press-room/press-releases/corporate-news/pwc-announces-strategic-alliance-with-harvey.html
  - Later PwC expansions: PwC UK deepened alliance across Tax/Legal/Deals (5,000+ professionals, 60+ countries) https://www.harvey.ai/customers/pwc-uk ; Sep 2024 PwC adopting Harvey for lawyers in Singapore (per Wikipedia). `[R1·C2]`
- **"Lighthouse" co-development program** — Harvey partnered with a group of firms to co-develop the platform, embedding tech within organizations "like Allen & Overy and PwC." (Forbes AU is the sole namer of "Lighthouse.") `[R2·C3]` https://www.forbes.com.au/news/innovation/what-is-harvey-ai-the-legal-tech-decacorn-changing-how-lawyers-work/
- **Apr 2023 — Series A (Sequoia-led)**; **Dec 2023 / Jan 2024 — Series B**; **Jul 2024 — Series C (GV)**; **Feb 2025 — Series D**; **Jun 2025 — Series E (~US$300M, ~US$5B valuation)**; **Dec 2025 — Series F (a16z-led)** — dates only (amounts owned by funding slice). SEC Form D filing dates corroborate the cadence: 2023-04-26, 2024-01-03, 2024-07-30, 2025-02-14, 2026-04-06. `[R1·C1 for filing dates]` https://data.sec.gov/submissions/CIK0001974654.json ; Series E detail https://ca.finance.yahoo.com/news/legal-ai-start-harvey-named-110038299.html
- **May 2024 — product commercialization + Vault + Harvey on Azure.** Wikipedia: launched products on Microsoft Azure; began general commercial access (case-law models, AI assistant, specialised models, and Vault for large document collections). `[R3·C2]` https://en.wikipedia.org/wiki/Harvey_(software)
- **Product surface (names; most undated in official copy):** Assistant, Vault, Knowledge, Agents/Workflows, Harvey Mobile, Ecosystem, Contract Intelligence, Command Center, Shared Spaces; "Memory" being fine-tuned. `[R1·C2]` https://www.harvey.ai/company (product nav) ; Vault/RAG description https://www.forbes.com.au/news/innovation/what-is-harvey-ai-the-legal-tech-decacorn-changing-how-lawyers-work/
- **Office footprint / HQ:**
  - **San Francisco = global HQ** (201 Third St, Suite 500, 94103). `[R1·C1]` https://data.sec.gov/submissions/CIK0001974654.json
  - **New York and London — among Harvey's largest offices** (alongside SF). Yahoo Finance (Canadian Press, Aug 2025): "Its largest offices are in San Francisco, New York, and London." `[R2·C2]` https://ca.finance.yahoo.com/news/legal-ai-start-harvey-named-110038299.html
  - **Sydney office — opening September 2025; Sydney is the APAC HQ.** Official blog dated Jul 7, 2025: "Announcing Harvey's new office opening in September in Sydney, Australia." Forbes AU: "Sydney serves as the firm's Asia-Pacific headquarters." `[R1·C1]` https://www.harvey.ai/blog/new-harvey-sydney-office ; https://www.forbes.com.au/news/innovation/what-is-harvey-ai-the-legal-tech-decacorn-changing-how-lawyers-work/
  - **Singapore office — opened June 2, 2026.** Official blog: "Today, we're opening our Singapore office… Singapore joins Bengaluru and Sydney in our growing APAC presence." `[R1·C1]` https://www.harvey.ai/blog/harvey-opens-in-singapore
  - **Toronto office — opening October 2025** (initial 20+ hires). Yahoo Finance/Canadian Press. `[R2·C3]` https://ca.finance.yahoo.com/news/legal-ai-start-harvey-named-110038299.html
  - **Milan — team expansion** (official blog "Next Up": "Harvey is Expanding With a Team in Milan"). `[R1·C3]` https://www.harvey.ai/blog/new-harvey-sydney-office
  - **Bengaluru / India** — APAC presence; Yahoo notes growth in "India." `[R1·C2]` https://www.harvey.ai/blog/harvey-opens-in-singapore
  - **Europe: Spain and Germany** (existing footprint, per Yahoo). `[R2·C3]` https://ca.finance.yahoo.com/news/legal-ai-start-harvey-named-110038299.html
  - **CONTESTED / low-confidence:** aggregator directories (exa.ai websets, highperformr.ai) list "Newport Beach, CA" and "Amsterdam" offices with specific addresses; highperformr's leadership data is contaminated (it references Freshworks execs), so these two office claims are treated as **unreliable/unverified**. Recorded, not relied upon. https://exa.ai/websets/directory/harvey-offices
- **International reach — country count differs across sources (recorded):** "more than 50 countries" (Forbes AU); "60+ countries" (official harvey.ai/company); "operating in more than 60 countries… 700 clients across 63 countries" (TechCrunch); an 11-country figure appears in a LinkedIn aggregate (older/offices-only). CONFLICT recorded; official self-stated figure is **60+**. `[R1·C2]` https://www.harvey.ai/company ; https://techcrunch.com/2025/11/14/inside-harvey-how-a-first-year-legal-associate-built-one-of-silicon-valleys-hottest-startups/
- **Rebrand note:** No public product "rebrand" narrated by Harvey; the corporate rename is the only rename found — **Counsel AI Corp → Harvey AI Corp** (SEC) / "formerly known as Counsel AI" (CB Insights). (Distinct from the customer rename "Allen & Overy → A&O Shearman.")

### 4. Mission / official self-description

- **harvey.ai/company (official), verbatim:** "**Harvey is domain-specific AI for legal and professional services. Our products streamline workflows in areas including contract analysis, due diligence, compliance, and litigation to drive efficiency and value. Global law firms and Fortune 500 enterprises around the world use Harvey to enable faster, smarter decision-making. Backed by world-class investors including Sequoia, Kleiner Perkins, GV, OpenAI Startup Fund, Coatue, Andreessen Horowitz, and EQT, Harvey is used by 1,500+ customers in 60+ countries.**" Page header: "We're helping the world's best teams transform the way they work"; section "Designed to scale." `[R1·C1]` https://www.harvey.ai/company
- **Official values (harvey.ai/company):** Decisiveness ("deliberate action over ivory tower intellectualization… 'taking the square root of the weather'"), Simplicity ("complexity appreciates and simplicity scales"), Job's Not Finished (JNF). `[R1·C3]` https://www.harvey.ai/company
- **Homepage tagline (official):** "Harvey is AI designed for legal and professional services. Advance your expertise on a secure platform that lets you focus on high-value work." `[R1·C1]` https://www.harvey.ai/
- **Product positioning line (official, site-wide):** "Harvey Agents execute legal work end-to-end, so you can focus on what only lawyers can do." `[R1·C2]` https://www.harvey.ai/legal
- **Press-kit / boilerplate (partner press release):** "About Harvey: Harvey is a generative AI company backed by OpenAI's startup fund. We partner with elite law firms and legal service providers to augment their legal expertise with cutting edge AI. Together, we tackle the world's most complex legal challenges." (2023 PwC release.) `[R1·C2]` https://www.pwc.com/gx/en/news-room/press-releases/2023/pwc-announces-strategic-alliance-with-harvey-positioning-pwcs-legal-business-solutions-at-the-forefront-of-legal-generative-ai.html
- **Third-party definition (tertiary):** Wikipedia — "Harvey is a generative artificial intelligence (AI) product developed by the Counsel AI Corporation for the legal industry. The product has been described as a provider of customised large language models (LLMs) for law firms and in-house legal teams." `[R3·C1]` https://en.wikipedia.org/wiki/Harvey_(software)

---

## Reflection trace

- **Round 1 (broad):** 2 Exa searches (founding story + milestones) + 1 batched crawl of 7 URLs (Wikipedia, TechCrunch, StartupRiders, Forbes AU, Harvey Singapore blog, harvey.ai/about [failed CRAWL_NOT_FOUND], Guy Louzon). Crawl exceeded token cap → offloaded extraction to a subagent (read all 995 lines) to keep raw text out of context. Surfaced the SF/San Diego/LA founding-city conflict, the 86/100 test, the July-4 origin, and A&O/PwC milestones. Corporate-register direct fetches attempted in parallel: **California SoS bizfile = Incapsula bot-block; OpenCorporates = HAProxy captcha; Trademarkia = Cloudflare block** (all not-reachable via curl — search facts).
- **Pivot to primary registers:** Justia (USPTO mirror) via Exa returned the two HARVEY trademarks (owner Counsel AI Corporation, filed 2022-11-23) — first hard confirmation of the legal entity. Then **SEC EDGAR full-text + submissions + Form D** (free, primary) delivered the decisive identity data: Delaware incorporation, year 2022, EIN, CIK, HQ address, founders as officers/directors, the Counsel AI → Harvey rename, and Form D dates matching the funding cadence. This more than compensated for the blocked corporate registers.
- **Round 2 (gap = official mission + Harvey's own office footprint):** 1 Exa search + 1 batched crawl (harvey.ai/company + Sydney blog). Recovered the verbatim official mission (the /about crawl had failed; correct page is /company), values, and precise Sydney (Sept 2025) office date. Yahoo/CBInsights/LinkedIn filled the SF-NY-London-Toronto-Spain-Germany-India footprint.
- **Stop:** all four sub-questions covered with primary sources; further searching hit diminishing returns. 2 rounds.

## Gaps and not-found

- **Direct corporate-register entity number (CA SoS / Delaware / OpenCorporates): NOT REACHED.** California SoS bizfile API returns an Incapsula bot-challenge; OpenCorporates returns an HAProxy human-verification captcha; Delaware's entity search is ASP.NET/session-gated. No free-tool path succeeded. **Mitigation:** SEC EDGAR supplied superior primary identity data (CIK 0001974654, EIN 88-3448544, Delaware, year 2022) and USPTO/Justia supplied the trademark record — so the state/date/entity are established even though the register's own file number is not captured. A CA SoS entity number and the Delaware file number remain unretrieved.
- **Exact incorporation DATE (day/month) not found** — only the **year 2022** is confirmed (SEC Form D "within five years, value 2022"). Trademark filings (2022-11-23) and seed announcement (Nov 2022) bound it but do not give the incorporation date.
- **USPTO trademark current status / registration numbers not confirmed as of today** — Justia snapshot shows "630 - New Application" (as of the mirror); live TSDR status/class 045 for serial ...542 not re-verified (TSDR JSON path 404'd; Justia detail page 403'd). Serials and owner are solid; downstream registration/abandonment status is a gap.
- **New York and London office founding dates not found** — their existence and "largest offices" status are sourced (Yahoo), but no opening-date press release was located in these two rounds.
- **Newport Beach / Amsterdam offices — contested** — appear only in low-quality aggregators (exa websets, highperformr, the latter demonstrably contaminated); neither corroborated by Harvey or credible press. Flagged unreliable.
- **Series A amount conflict** (noted in passing, funding-slice territory): Wikipedia "$23M" vs Forbes AU "US$21M," both April 2023, both Sequoia-led. Recorded for the funding slice.

## Sources consulted (with grades)

Primary / authoritative (R1)
- SEC EDGAR — submissions & metadata (Harvey AI Corp / f.k.a. Counsel AI Corp, CIK 0001974654): https://data.sec.gov/submissions/CIK0001974654.json — `[R1]`
- SEC EDGAR — Form D (2024-07-30) primary_doc.xml (Delaware, year 2022, related persons): https://www.sec.gov/Archives/edgar/data/1974654/000197465424000004/xslFormDX01/primary_doc.xml — `[R1]`
- SEC EDGAR full-text search (Form D hits, inc_states DE, biz San Francisco): https://efts.sec.gov/LATEST/search-index?q=%22Counsel%20AI%22&forms=D — `[R1]`
- USPTO trademark records via Justia — HARVEY, owner Counsel AI Corporation, serials 97690544 / 97690542, filed 2022-11-23: https://trademarks.justia.com/976/90/harvey-97690544.html ; https://trademarks.justia.com/search?q=Counsel+AI+Corporation — `[R1 data via R2 aggregator]`
- harvey.ai/company (official mission, values, footprint stats): https://www.harvey.ai/company — `[R1]`
- harvey.ai homepage (tagline): https://www.harvey.ai/ — `[R1]`
- harvey.ai/legal (positioning line, legal-doc index): https://www.harvey.ai/legal — `[R1]`
- harvey.ai blog — Sydney office (Jul 7 2025; opening Sept 2025): https://www.harvey.ai/blog/new-harvey-sydney-office — `[R1]`
- harvey.ai blog — Singapore office (opened Jun 2 2026; Bengaluru/Sydney APAC): https://www.harvey.ai/blog/harvey-opens-in-singapore — `[R1]`
- harvey.ai/customers/pwc-uk (PwC UK alliance): https://www.harvey.ai/customers/pwc-uk — `[R1]`
- A&O Shearman press release — exclusive launch partnership (Feb 15 2023): https://www.aoshearman.com/en/news/ao-announces-exclusive-launch-partnership-with-harvey — `[R1]`
- PwC press release — global strategic alliance (Mar 15 2023): https://www.pwc.com/gx/en/news-room/press-releases/2023/pwc-announces-strategic-alliance-with-harvey-positioning-pwcs-legal-business-solutions-at-the-forefront-of-legal-generative-ai.html ; UK: https://www.pwc.co.uk/press-room/press-releases/corporate-news/pwc-announces-strategic-alliance-with-harvey.html — `[R1]`

Credible press (R2)
- TechCrunch — "Inside Harvey…" (Nov 14 2025; cold email, 86/100, July 4, 63 countries): https://techcrunch.com/2025/11/14/inside-harvey-how-a-first-year-legal-associate-built-one-of-silicon-valleys-hottest-startups/ — `[R2]`
- LawSites/LawNext — seed emergence (Nov 2022): https://www.lawnext.com/2022/11/stealth-legal-ai-startup-harvey-raises-5m-in-round-led-by-openai.html ; A&O firmwide (Feb 2023): https://www.lawnext.com/2023/02/as-allen-overy-deploys-gpt-based-legal-app-harvey-firmwide-founders-say-other-firms-will-soon-follow.html — `[R2]`
- LawNext podcast page (roommates/2022/SF, "1,000+ firms"): https://www.lawnext.com/2026/01/lawnext-from-roommates-to-billionaires-harveys-founders-gabriel-pereyra-and-winston-weinberg-on-building-ai-infrastructure-for-law.html — `[R2]`
- Legal IT Insider — A&O launch (founded 2022, Weinberg/Pereyra bios): https://legaltechnology.com/allen-overy-breaks-the-internet-and-new-ground-with-co-pilot-harvey/ — `[R2]`
- Forbes Australia — profile (San Diego sharehouse vs SF founding; Lighthouse; Sydney APAC HQ; 50+ countries; USC CS): https://www.forbes.com.au/news/innovation/what-is-harvey-ai-the-legal-tech-decacorn-changing-how-lawyers-work/ — `[R2]`
- Yahoo Finance / Canadian Press — Toronto office + SF/NY/London largest offices + Spain/Germany/India (Aug 2025): https://ca.finance.yahoo.com/news/legal-ai-start-harvey-named-110038299.html — `[R2]`
- Observer — Weinberg interview (cold email): https://observer.com/2026/03/harvey-ceo-winston-weinberg-ai-law/ — `[R2]`

Aggregators / practitioner blogs (R3) and weak (R4)
- Wikipedia "Harvey (software)" (entity=Counsel AI Corporation; Suits naming; milestone chronology): https://en.wikipedia.org/wiki/Harvey_(software) — `[R3]`
- CB Insights — "formerly known as Counsel AI"; HQ: https://www.cbinsights.com/company/harvey-2 — `[R3]`
- StartupRiders growth playbook (email subject line; July 2022 SF apartment; A&O 4,000-person rollout): https://www.startupriders.com/p/harvey-ai-growth-playbook — `[R3]`
- Guy Louzon Substack (LA opening scene; USC Gould; DeepMind/Google Brain timeline): https://guylouzon.substack.com/p/harvey-ai-when-an-omelveny-litigator — `[R3]`
- LinkedIn company aggregate via Exa (8 offices / 3 countries; NY/London/Sydney): https://linkedin.com/company/harvey-ai — `[R3]`
- exa.ai websets directory & highperformr.ai — office claims (Newport Beach/Amsterdam) treated as CONTESTED/unreliable (highperformr data contaminated): https://exa.ai/websets/directory/harvey-offices — `[R4]`

Registers attempted but NOT reachable (recorded as search facts)
- California SoS bizfile business search — Incapsula bot-block (POST returned Incapsula challenge). — not reached
- OpenCorporates company search "Counsel AI Corporation" — HAProxy human-verification captcha. — not reached
- Trademarkia API — Cloudflare "Attention Required" block. — not reached
- USPTO TSDR JSON status endpoint (sn97690542) — 404 at attempted path; Justia detail page for ...542 returned HTTP 403. — partial
