---
name: product-metrics-kpis
description: Use this skill when the user is choosing, defining, instrumenting, or reviewing product metrics and KPIs. Triggers — "what metrics should we track", "north star metric", "activation metric", "AARRR pirate metrics", "HEART framework", "input vs output metrics", "leading vs lagging indicators", "define KPI".
---

# Product metrics and KPIs

Use this skill when the user needs to **choose**, **define**, **instrument**, **dashboard**, or **review** product metrics and KPIs — including **North Star**, **activation**, **retention**, and framework-led metric design (**AARRR**, **HEART**, **funnel**, **growth loops**). Read repository overviews before proposing a bespoke taxonomy.

## When this skill applies (and when it does not)

### Applies

- Designing or auditing a **metrics stack** for a product surface, funnel, or lifecycle stage.
- Picking or reframing a **North Star** and supporting **input** metrics.
- Defining **activation** and **retention** with event semantics and cohort rules.
- Explaining **leading vs lagging** indicators and **input vs output** metrics for planning.
- Mapping user problems to **measurable** outcomes for OKRs or discovery readouts.

### Does not apply

- **Pure OKR facilitation** without deep metric definitions — use `okrs-goal-setting` alongside this skill; OKRs still need KRs, but the conversation may stay at grading level.
- **Financial close / accounting KPIs** owned solely by Finance — collaborate, but source of truth is finance policy and ERP, not product analytics alone.
- **Infra-only SRE metrics** without product outcomes — pair with platform SRE practice; product skill still helps frame **user-visible** reliability metrics.

## Repo-first cross-references

Consult and cite these paths when advising or drafting artifacts:

- KPIs and metrics overview: `.productmap/03_analysis/kpis-metrics/_overview.md`
- Analytics practice overview: `.productmap/03_analysis/analytics/_overview.md`
- Unit economics (ties metrics to business viability): `.productmap/03_analysis/unit-economics/_overview.md`
- Raw analytics exports and notes (when user has data): `.productmap/10_data/analytics/`
- OKRs alignment (KRs must point to defined metrics): `.productmap/01_strategy/okrs/_overview.md`
- PMF and survey-style evidence (discrete “must-have” and segment strength): `.productmap/01_strategy/product-market-fit/_overview.md`, `.productmap/01_strategy/product-market-fit/opportunity-assessment.md`
- Navigation index: `.productmap/index.md`

Store initiative-specific metric specs under `.productmap/00_company/product/<initiative>/` or raw tables under `.productmap/10_data/analytics/` as appropriate.

## Taxonomy (shared vocabulary)

### North Star metric

- A **single** primary indicator of **delivered customer value** that correlates with **sustainable business** for the current strategy.
- Should be **actionable** by product (not only a lagging revenue line unless that is truly the best proxy).
- Often supported by **3–6** input metrics that predict movement in the North Star.

### KPI

- A **key performance indicator** — usually a **stable** management metric with a **target band** or threshold (conversion, retention, cost to serve, quality).
- KPIs can be **leading** or **lagging**; the “key” label implies **executive** or **operating** attention.

### Leading vs lagging

- **Leading**: moves **before** the outcome (example: activation rate in week 1 predicts later retention).
- **Lagging**: confirms value **after** the fact (example: net revenue retention for the quarter).

### Input vs output

- **Output**: customer or business **result** (retention, revenue, margin).
- **Input**: **drivers** the team pulls (funnel volume, feature adoption depth, latency, support response time) — often controllable **earlier** in the chain.

### Instrumentation primitives

- **Event**: user or system action with schema, properties, and time.
- **Property**: dimensions for segmentation (plan, region, role).
- **Cohort**: a group defined by a **start condition** and tracked over calendar or relative time.
- **Definition doc**: the **legal** meaning of a metric (numerator, denominator, filters, latency handling).

### HEART dimensions (operational reminders)

- **Happiness**: attitudinal measures (CSAT, NPS proxies) — tie to **moments** after success, not random intercepts.
- **Engagement**: **intensity** or **frequency** of meaningful use — define “meaningful” per product.
- **Adoption**: breadth of **features** or **journeys** used when that predicts retention or expansion.
- **Retention**: returning use at the **right cadence** for the product’s job.
- **Task success**: completion, time-on-task, error rate for **critical workflows** — excellent for B2B tools.

Pick **one primary** HEART dimension per initiative plus **one** supporting dimension to avoid dilution.

## Framework map (when to use which)

### AARRR (“pirate metrics” — Dave McClure)

- **Acquisition**: how users arrive (channels, CAC context).
- **Activation**: first **meaningful** use — must be defined per product (not “signed up”).
- **Retention**: users return to **core value** on a useful cadence.
- **Revenue**: monetization behavior and expansion where relevant.
- **Referral**: organic growth loops and viral coefficient proxies.

Use AARRR for **full-funnel** consumer or self-serve products where lifecycle stages are clear.

### HEART (Google — Happiness, Engagement, Adoption, Retention, Task success)

- Strong for **UX quality** and **task-based** products (tools, workflows).
- Pairs **qualitative** (surveys, usability) with **quantitative** proxies; pick **1–2** dimensions per release, not all five every time.

### McClure funnel framing

- Practically overlaps **AARRR**; emphasize **narrowest step** diagnosis — where volume drops and **why** (intent, usability, performance, trust).

### Reforge-style growth loops

- Model **inputs** that feed **stored state** (inventory, content, relationships, data) and **outputs** that attract new users — useful for **marketplaces**, **UGC**, **collaboration**, and **data network effects**.

Use loops when **acquisition is partially a function of existing usage** (not only paid media).

Common loop **archetypes** (pick labels that match your narrative; metrics follow):

- **Acquisition loop**: usage generates **referrals**, **UGC**, or **SEO surface** that brings new users.
- **Engagement loop**: usage improves **personalization**, **notifications**, or **habit** that increases frequency.
- **Economic loop**: scale improves **unit economics** (marginal cost, liquidity) that funds reinvestment.

### Compact framework comparison

| Framework | Best when | Primary risk if misapplied |
|-----------|-----------|----------------------------|
| AARRR / McClure funnel | Self-serve lifecycle; channel mix | Over-indexing top-of-funnel vanity |
| HEART | Task tools; UX-led releases | Survey overload; vague “happiness” |
| Growth loops | Network effects; UGC; marketplaces | Pretty diagrams without state variables |
| North Star only | Exec alignment | Star metric too lagging or not actionable |

## Choosing a North Star (process)

1. **Value hypothesis**: What **job** is done better because of the product (JTBD or positioning statement)?
2. **Proof of value**: What **user behavior** proves the job succeeded on a recurring basis?
3. **Business bridge**: What **unit economics** or strategic constraint must move (margin, depth, frequency)?
4. **Actionability test**: Can a product squad move this metric in **90 days** with believable levers?
5. **Integrity test**: Could the metric rise while **users suffer** (goodhart risk)? If yes, add **guardrails** (quality, latency, complaints).

Document the North Star in a **definition table** with numerator/denominator, exclusions, and **segmentation defaults**.

## North Star examples (illustrative patterns)

### B2C habit product (example pattern)

- **North Star**: **Weekly active users** completing **core action** ≥ once per week.
- **Why**: Recurring value; correlates with retention and ad or subscription surfaces.
- **Inputs**: new user activation in D7, core action success rate, notification efficacy (opt-in and CTR), latency.

### B2B SaaS team workflow (example pattern)

- **North Star**: **Weekly active teams** (or seats) performing **collaborative task** tied to revenue seats.
- **Why**: Land-and-expand motion ties usage depth to expansion and churn risk.
- **Inputs**: invite acceptance, integration connected, time-to-first-shared-artifact, admin health.

### Marketplace (example pattern)

- **North Star**: **Successful matches** per week (or GMV with quality filters) — pick one primary.
- **Why**: Balances supply, demand, and transaction quality; loops often tie to **liquidity**.
- **Inputs**: supply activation, buyer conversion, search-to-fill, repeat rate, cancellation rate.

Always replace placeholders with **definitions** and **baselines** for the user’s actual product.

## Activation and retention (depth)

### Activation

- Define **“activated user”** as the earliest point where the user has **experienced core value** (not onboarding completion alone).
- Specify: **start event**, **required events**, **time window** (example: within 7 days of signup), **segment cuts** (mobile vs web).
- Track **activation rate** and **time-to-activate**; investigate **drop-off steps** with funnel and qualitative research.

### Retention

- Choose **cadence** that matches natural usage (daily / weekly / monthly).
- Use **cohort charts** (by signup week, by acquisition channel, by plan).
- Separate **curiosity churn** (never activated) from **post-value churn** (activated then left) — interventions differ.

## PMF measurement cross-reference (Sean Ellis-style)

- The **“must-have”** survey and **segment** disaggregation help decide if growth spend is **premature** — see `.productmap/01_strategy/product-market-fit/_overview.md` and `.productmap/01_strategy/product-market-fit/opportunity-assessment.md`.
- Do not confuse **PMF sentiment** with **product quality** metrics; combine **qual + quant**.

## Workflow A — Metric inventory

1. List **all** metrics currently reported (dashboards, finance, support).
2. Tag each as **North Star candidate**, **supporting input**, **health/KPI**, or **diagnostic**.
3. Remove duplicates and **conflicting definitions**; pick canonical definitions.

## Workflow B — North Star workshop (90 minutes)

1. Align on **customer** and **job**.
2. Brainstorm **candidate** metrics; shortlist by **actionability** and **integrity**.
3. Pick **one** North Star; define **3 inputs** max for the next planning horizon.
4. Assign **owners** for data definitions and **instrumentation gaps**.

## Workflow C — Definition doc for one metric

1. Name, **business question**, and **non-goals**.
2. Formula, **filters**, **window**, **latency** tolerance.
3. **Event** sources and **edge cases** (bots, tests, refunds).
4. **QA** procedure and **backfill** plan.

## Workflow D — Funnel diagnostic

1. Choose **cohort** and **steps** (AARRR or custom).
2. Quantify **largest leaks** and **rates** (not only absolute drops).
3. Pair with **qual** (session replay, interviews) for **why**.

## Workflow E — Dashboard review

1. For each tile: **decision** it supports — if none, remove or demote.
2. Check **segmentation** defaults (avoid blended lies).
3. Add **guardrails** for Goodhart risk (quality, fraud, latency).

## Workflow F — OKR / metric alignment

1. For each proposed KR, attach **metric definition doc** or link to query.
2. Confirm **baseline** and **data freshness** acceptable for grading.
3. See `.productmap/01_strategy/okrs/_overview.md` for OKR-specific ritual.

## Pitfalls (avoid)

1. **Vanity metrics** that rise without value (raw downloads, empty “sessions”).
2. **Blended averages** hiding weak segments (region, plan, role).
3. **Overfitting** one metric until quality or trust collapses (Goodhart).
4. **Activation = signup** — conflates intent with value receipt.
5. **No event spec** — analysts and PMs compute different numbers forever.
6. **Too many primaries** — everything is “critical,” nothing moves.
7. **Lagging-only dashboards** — teams cannot tell **what to try** next week.
8. **Ignoring unit economics** — growth metrics disconnected from `.productmap/03_analysis/unit-economics/_overview.md` reality.

## Questions to ask the user (pick 5–8)

1. What **customer** and **job** are we optimizing for this half?
2. What **natural usage cadence** should retention reflect (D/W/M)?
3. What **event instrumentation** exists today (tooling, warehouse, naming)?
4. What **segments** must be reported separately for decisions?
5. What **trust or quality** risks could rise if we maximize the headline metric?
6. What **financial** constraints tie to metrics (CAC, margin, payback)?
7. What **decisions** will each dashboard tile drive in the next sprint?
8. What **evidence** would convince you the North Star is **wrong** and should change?

## Artifact skeletons

### Skeleton A — Metrics catalog (team)

```markdown
# Metrics catalog — <Product> — <YYYY-MM-DD>

## North Star
| Metric | Definition | Owner | Cadence | Notes |

## Supporting inputs
| Metric | Definition | Hypothesized lever | Owner |

## Health KPIs / guardrails
| KPI | Threshold | Rationale |

## Funnels / cohorts
- Default cohort definition:
- Key funnels:

## Data sources
- Warehouse tables / events:

## Open gaps
- Instrumentation needed:
```

### Skeleton B — Single metric definition

```markdown
# Definition — <Metric name> — v<semver> — <YYYY-MM-DD>

## Question
## Formula
## Events and properties
## Filters and exclusions
## Latency and backfill
## QA checklist
## History of changes
```

## Quality checklist

- North Star passes **actionability**, **integrity**, and **business bridge** tests.
- Activation and retention have **written** definitions with **time windows**.
- Framework choice (**AARRR**, **HEART**, **loops**) matches business model.
- Inputs are **few**, **owned**, and **instrumented** or flagged as gaps.
- Dashboards map to **decisions**; junk tiles removed or archived.
- Cross-links to **OKRs**, **PMF**, **unit economics**, and **analytics** paths are explicit when used.

## Detailed agent instructions

- Use **absolute dates** in filenames and doc headers.
- Read `.productmap/03_analysis/kpis-metrics/_overview.md` and `.productmap/03_analysis/analytics/_overview.md` before proposing a stack from scratch.
- When users ask “what should we track,” respond with a **small** set and **definitions**, not a hundred-metric laundry list.
- Prefer **cohorts** and **funnels** with **segment cuts** over global aggregates.
- If data is missing, specify **what to log** next and **minimum** viable definition for decisions.

---

Strong metrics discipline is **definition discipline**; frameworks only organize the work.
