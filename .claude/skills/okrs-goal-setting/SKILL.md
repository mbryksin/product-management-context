---
name: okrs-goal-setting
description: Use this skill when the user is writing, reviewing, or grading Objectives and Key Results (OKRs), or setting product/team goals. Triggers — "write OKRs", "draft quarterly goals", "grade OKRs", "key results", "aspirational vs committed", "KPIs vs OKRs", "goal-setting for the team".
---

# OKRs and goal setting

Use this skill when the user wants to **draft**, **review**, **align**, or **grade** Objectives and Key Results (OKRs), or translate strategy into **quarterly goals** for product or engineering teams. Ground every answer in this repository’s templates and overviews before inventing structure.

## When this skill applies (and when it does not)

### Applies

- Quarterly or half-year **goal cycles** for product, platform, or cross-functional teams.
- Turning **strategy** or roadmap themes into measurable outcomes.
- **Calibration** conversations: committed vs stretch, dependency risk, resourcing.
- **Mid-quarter** check-ins and **end-of-quarter grading** with evidence.
- Clarifying **terminology** (Objective vs Key Result vs initiative vs KPI).

### Does not apply (use adjacent skills or templates instead)

- **North Star / KPI catalog design** without an OKR wrapper — use the product metrics skill and KPIs overview.
- **Roadmap prioritization** without explicit OKR linkage — still use OKRs, but pair with roadmap and delivery practices.
- **Individual performance reviews** framed as HR appraisals — OKRs inform context but are not a substitute for people management frameworks.
- **Pure project plans** (milestones only, no measurable outcomes) — convert milestones into outcome hypotheses or keep them outside the OKR set.

## Repo-first cross-references (read before drafting)

Consult these paths in order; cite them in written artifacts when used.

- OKRs topic overview: `.productmap/01_strategy/okrs/_overview.md`
- OKR framework notes: `.productmap/08_frameworks/okrs.md`
- OKR template (canonical structure): `.productmap/09_templates/okr-template.md`
- Roadmap alignment surface: `.productmap/00_company/product/roadmap.md`
- KPIs and metrics context (avoid confusing KPIs with KRs): `.productmap/03_analysis/kpis-metrics/_overview.md`
- Navigation index: `.productmap/index.md`

If the user names an initiative, prefer storing drafts under `.productmap/00_company/product/<initiative>/` per repository conventions.

## Core taxonomy

### Objective

- A **qualitative**, **time-bound**, **directional** statement of what you intend to achieve.
- Should be **memorable** and **aligned** to company or product strategy — not a task list.
- Typically **one verb + outcome + strategic intent** (for example: “Win in <segment> by delivering <differentiator> customers trust”).

### Key Result (KR)

- A **measurable** outcome that proves the Objective was achieved (or how far you got).
- Must be **observable**, ideally **end-state** oriented (not activity).
- Good KRs read like **evidence in court**: if numbers move as stated, a reasonable stakeholder agrees the Objective moved.

### Initiative (project, epic, bet)

- The **work** you ship to move KRs — **not** a KR itself.
- Initiatives belong in **backlogs, roadmaps, and delivery plans**; they **nest under** KRs.
- Common failure: listing “Ship feature X” as a KR without a measurable customer or business outcome.

### OKR set

- A **small** number of Objectives (often **2–4** per team per cycle) each with **2–5** KRs.
- If everything is “P0,” you have **no strategy** — you have a wishlist.

## OKRs vs KPIs vs V2MOM vs SMART

### OKRs

- **Purpose**: Align and stretch the organization on **outcomes** over a fixed horizon (often quarterly).
- **Cadence**: Written, reviewed, and **graded** each cycle; some KRs may roll if still strategic.
- **Tone**: Mix of **committed** (must hit) and **aspirational** (unlikely full score) depending on org norms.

### KPIs (health metrics)

- **Purpose**: Monitor **ongoing business health** (reliability, margin, quality, satisfaction baselines).
- **Cadence**: Continuous dashboards; thresholds and SLOs rather than quarterly “grades.”
- **Relationship to OKRs**: KPIs can **inform** which OKRs matter; a KR might **move** a KPI, but “keep uptime at 99.95%” is usually a **SLO/KPI**, not an aspirational OKR unless you are deliberately improving from a worse baseline.

### V2MOM (Vision, Values, Methods, Obstacles, Measures)

- **Purpose**: Executive **alignment** document (Salesforce-originated) — broader than a single team OKR sheet.
- **Use**: Good for **cascading narrative**; pair with OKRs where Methods/Measures map to KRs.

### SMART goals

- **Purpose**: Sanity-check any single goal (Specific, Measurable, Achievable, Relevant, Time-bound).
- **Use**: Apply SMART to **each KR**; OKRs add **portfolio discipline** (few Objectives, explicit trade-offs, grading ritual).

## Anatomy of a strong OKR

1. **Objective**: Outcome-oriented, qualitative, aligned, time-implicit or explicit.
2. **KRs**: Each has a **baseline**, **target**, **unit**, and **measurement method** (where the number comes from).
3. **Dependencies**: Cross-team or data dependencies called out early.
4. **Initiatives**: Listed **under** KRs — enough to show plausible path, not so many that work replaces outcomes.
5. **Grading rubric**: Agreed **scoring** (for example 0.0–1.0) and what **evidence** counts.

## Aspirational vs committed (Google-style 0.7)

- **Committed KRs**: The business **depends** on delivery; missing them is a **failure** — expect scores **near 1.0** when executed well.
- **Aspirational (stretch) KRs**: Chosen so that **full success is unlikely** in one cycle; a “good” outcome might be **~0.7** average on stretch KRs **if** teams aimed high enough.
- **Operational hygiene**: Label each KR **Committed** or **Stretch** to avoid grading debates.
- **Anti-cheating**: If everything scores 1.0 every quarter, either goals were **sandbagged** or grading is **inflated**. If everything scores 0.2, goals were **unreachable** or execution measurement is broken.

## Examples: two strong OKRs

### Example A — B2B SaaS growth (good)

- **Objective**: Become the default choice for <ICP> teams replacing spreadsheets in <workflow>.
- **KR1 (Committed)**: Increase **weekly active teams** in ICP from **X → Y** by `YYYY-MM-DD` (definition: ≥1 meaningful session per week, product analytics).
- **KR2 (Stretch)**: Improve **4-week retention** of activated ICP teams from **A% → B%** by `YYYY-MM-DD` (definition: cohort from first “aha” event).
- **KR3 (Committed)**: Reduce **P1 incidents** per month from **N → ≤M** by `YYYY-MM-DD` (definition: incident taxonomy in ops tool).

Why it is good: Clear ICP, mix of committed reliability and growth, definitions anchor measurement.

### Example B — Platform reliability (good)

- **Objective**: Earn customer trust through predictable performance during peak season.
- **KR1**: **p95 API latency** for core read path ≤ **T ms** for **≥ 99%** of weeks in the quarter (telemetry).
- **KR2**: **Error budget** consumed for checkout ≤ **B%** for the quarter (SRE reporting).
- **KR3**: **Support tickets** tagged “slow/failed checkout” per 1k orders down from **u → v** (support system).

Why it is good: KRs are measurable, map to trust, and use existing operational signals.

## Examples: two weak OKRs (and how to fix them)

### Example C — Activity masquerading as outcomes (bad)

- **Objective**: Ship lots of features customers want.
- **KR1**: Ship **new billing UI**.
- **KR2**: Close **20 Jira epics**.
- **KR3**: Run **12 customer interviews**.

Why it is bad: KRs are **outputs**, not **results**; “customers want” is unbounded.

**Fix**: Rewrite KRs around **adoption**, **conversion**, **retention**, **time saved**, or **revenue** with baselines; put UI/epics/interviews under **initiatives**.

### Example D — Unmeasurable aspiration (bad)

- **Objective**: Delight customers everywhere.
- **KR1**: Make onboarding **amazing**.
- **KR2**: Improve **quality**.
- **KR3**: Increase **love**.

Why it is bad: No **instrument**, no **baseline/target**, no **segment**.

**Fix**: Pick **one** primary segment and **one** primary journey; define **activation**, **task success rate**, **TTV**, **NPS/CSAT** with methodology and targets.

## Workflows

### Workflow 1 — Writing quarterly OKRs (facilitation order)

1. **Restate strategy** for the quarter in one page (or link to existing strategy doc in repo).
2. **Choose 2–4 Objectives** that together imply real **trade-offs** (what you will not chase).
3. For each Objective, draft **2–5 KRs** with **baseline/target**, **unit**, **data source**, **owner**, **dependencies**.
4. Classify each KR **Committed vs Stretch**; sanity-check stretch with **aspirational 0.7** intent.
5. Map **initiatives** under KRs; ensure roadmap `.productmap/00_company/product/roadmap.md` does not contradict resourcing.
6. **Peer review**: dependency risks, metric gaming, double counting across teams.
7. **Finalize** using `.productmap/09_templates/okr-template.md` structure.

### Workflow 2 — Grading OKRs (end of cycle)

1. For each KR, capture **final value**, **link to evidence** (dashboard, finance close, research synthesis).
2. Assign **score 0.0–1.0** with agreed rules (linear interpolation vs tiered).
3. Write a **short narrative**: what worked, what surprised, what you would **keep/change** next quarter.
4. Separate **execution failure** from **bad hypothesis** from **external shock** — each implies different next actions.
5. Roll learning into **next quarter’s** Objectives; avoid “zombie KRs” that persist without strategic relevance.

## Anti-patterns (avoid)

1. **KR laundry lists** — more than ~5 KRs per Objective dilutes focus and hides failure.
2. **Sandbagging** — targets you will hit without changing behavior; grades always ~1.0 on stretch-labeled KRs.
3. **Metric without baseline** — “Increase signups” without from/to or time window.
4. **Vanity metrics** — numbers that rise without creating **value** (pageviews without conversion, logins without outcomes).
5. **Confusing KPIs with OKRs** — putting every health metric in the OKR sheet so nothing is prioritized.
6. **Unowned KRs** — “the company” owns it; no single accountable lead for measurement.
7. **Cross-team doubles** — two teams claim the same KR number without shared instrumentation.
8. **Initiatives as KRs** — shipping is necessary but not sufficient; measure **impact** of shipping.

## Questions to ask the user (pick 5–8 each session)

1. What **cycle dates** apply (`YYYY-MM-DD` start/end), and is the org on **calendar** or **fiscal** quarters?
2. Which **Objectives** are **committed** vs **stretch**, and what happens if a committed KR slips?
3. What **segments** and **surfaces** are in scope (who is the customer of these outcomes)?
4. What **baselines** exist today for each KR (or what discovery is needed to set them)?
5. What **dependencies** exist on other teams, data, compliance, or launches?
6. How will you **measure** each KR (tooling, event definitions, finance sign-off)?
7. What **roadmap** bets consume capacity this quarter — do they map to KRs or should scope change?
8. What **grading rubric** will you use so mid-quarter and end-quarter reviews do not devolve into debate?

## Artifact skeletons (Markdown outlines)

### Skeleton A — Quarterly OKR sheet (team)

Use sections aligned to `.productmap/09_templates/okr-template.md` (extend if the template is minimal):

```markdown
# <Team> — OKRs — <YYYY-MM-DD> to <YYYY-MM-DD>

## Strategy link
- Summary / links:

## OKRs

### Objective 1 — <name>
- Context / why now:

| KR | Type (C/S) | Baseline | Target | Unit | Definition | Owner | Evidence URL |
|----|------------|----------|--------|------|------------|-------|----------------|

#### Initiatives (non-KRs)
- ...

### Objective 2 — <name>
...

## Dependencies & risks
- ...

## Grading (end of quarter)
| KR | Score | Evidence | Notes |
```

### Skeleton B — OKR review memo

```markdown
# OKR review — <Team> — graded <YYYY-MM-DD>

## Summary
- Average scores (C vs S):
- Top wins:
- Top misses:

## KR-by-KR
### <KR name>
- Target vs actual:
- Evidence:
- Diagnosis (execution vs hypothesis vs external):
- Next quarter change:

## Implications for roadmap
- ...
```

## Quality checklist (before calling OKRs “done”)

- Each Objective is **outcome-oriented** and **aligned** to stated strategy.
- Each KR has **baseline**, **target**, **definition**, **owner**, and **data source**.
- Initiatives are **nested**, not mislabeled as KRs.
- Committed vs stretch is **explicit**; grading rules are **explicit**.
- KPIs/SLOs are **classified** correctly — not every health metric is an OKR.
- Dependencies and **measurement risk** are visible on the page.
- Repo paths used are **cited** for traceability.

## Detailed agent instructions (operational)

- Always use **absolute dates** (`YYYY-MM-DD`) in artifacts and filenames.
- Read `.productmap/01_strategy/okrs/_overview.md`, `.productmap/08_frameworks/okrs.md`, and `.productmap/09_templates/okr-template.md` first when drafting.
- When the user mixes **KPIs** and **OKRs**, separate **health** metrics from **change** metrics and propose a minimal OKR set that drives the quarter.
- When grading, insist on **evidence links** or query paths, not feelings.
- If information is missing, output **assumptions** and **questions** rather than fabricating baselines.

---

This skill complements delivery and analytics material in the same repo; keep OKR documents **small**, **measurable**, and **honest** about trade-offs.
