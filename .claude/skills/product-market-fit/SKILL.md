---
name: product-market-fit
description: Use this skill when the user asks how to measure, reach, or diagnose product-market fit (PMF). Triggers — "do we have PMF", "measure PMF", "Sean Ellis test", "retention curve", "40% rule", "leading indicators of PMF", "why isn't it growing", "is this market big enough".
---

# Product–market fit (PMF)

PMF is not a vibe. It is a **repeatable pattern** where a defined market **pulls** the product—retention, engagement, and organic demand show that the product is **right enough** for **someone specific**, not everyone.

## When this skill applies

- The user asks whether they **have PMF**, how to **measure** it, or how to **get** to it.
- They mention **Sean Ellis**, **very disappointed**, **40%**, or **PMF scorecards**.
- They show **retention curves**, **cohorts**, or growth stalls and want diagnosis.
- They ask **“why isn’t it growing”** in a way that implies product–market mismatch, not only channel optimization.
- They ask if the **market is big enough** relative to observed retention and willingness to pay.

## When it does not apply (use something else)

- **Pure growth / paid acquisition tuning** (creative, bidding, attribution) without a retention or PMF hypothesis—start with `.productmap/02_generation/growth-sales/_overview.md` and treat PMF as a prerequisite check, not the whole answer.
- **Narrative strategy or sequencing** without PMF measurement—use `.claude/skills/product-strategy-roadmap/SKILL.md` (or `.codex/skills/product-strategy-roadmap/SKILL.md`).
- **Deep pricing/packaging strategy** as the primary question—use business model and finance-oriented material under `.productmap/01_strategy/business-model/_overview.md` and `.productmap/03_analysis/`.
- **Hiring, org design, or stakeholder negotiation** as the core ask—use people/ops skills and overviews, not PMF instrumentation.
- **Technical reliability or delivery throughput** as the only bottleneck—PMF diagnosis may be secondary to engineering and incident work; be explicit so you do not blame “the market” for execution failure.

## Definitions (use precisely)

### Problem–solution fit

Evidence that a **painful problem** exists and your **solution concept** relieves it in prototype or concierge form. Necessary early signal; **not** PMF by itself. PMF requires sustained behavior in the wild at scale appropriate to your stage.

### Product–market fit

A state where target users **get recurring value**, **stay**, and **pull** the product (usage, retention, organic acquisition, or willingness to pay—depending on model). Operational definition varies by business model, but the pattern is the same: **retention + resonance in a defined segment**.

### Product–channel fit

The product is **compatible** with a scalable acquisition motion (e.g., paid search, PLG, sales-led). You can have PMF in a narrow channel and still fail to scale if the product does not fit economically viable channels.

### Product–business-model fit

Unit economics work at the **margin structure implied by the product** (COGS, support intensity, sales motion). PMF without business-model fit produces revenue that destroys cash.

When the user conflates these, separate them before recommending experiments.

## Quantitative signals (and how to interpret thresholds)

Thresholds are **heuristics**, not laws. Segment, ACV, geography, and category baseline matter. Always compare to **meaningful cohorts** and honest denominators.

### Sean Ellis “very disappointed” (PMF survey)

- **Method**: Ask active or recent users how they would feel if they could no longer use the product (see verbatim questions in Artifacts).
- **Heuristic**: Roughly **≥40%** answering **“Very disappointed”** among **qualified users** (those who experienced core value, not random signups) is often cited as a **strong PMF signal** for consumer-ish and many SMB products.
- **Caveats**: B2B with forced rollout can skew; narrow ICP increases score; bloated denominators (every free signup) depress signal quality.

### Retention curve shape

- **Good**: Cohort retention **flattens** to a stable plateau (not asymptoting to zero) for your core action or revenue cohort.
- **Bad**: Continuous **linear-ish decline** toward zero with no plateau in the window that matters for your cycle.
- **Caveats**: Seasonality, annual contracts, and sparse usage products need adjusted windows; define the **core action** or **contract renewal** explicitly.

### Net Promoter Score (NPS) and satisfaction bands

- NPS alone is a weak PMF test; use as **supplementary** signal with segment cuts.
- Directionally, **strong PMF** products often show **materially positive** NPS in their **ICP** with enough sample; **deeply negative** NPS in ICP is a red flag even if headline revenue grows.

### Organic growth and pull

- Rising **organic / direct / branded** traffic, **referral loops**, **invites**, or **expansion revenue** without proportional marketing spend often indicates pull.
- Contrast with **paid-only** growth: can mask PMF gaps until CAC rises or budgets cut.

### Payback and monetization (when revenue matters)

- **CAC payback** within a range that matches your funding and margin profile (varies widely by ACV).
- **Net revenue retention (NRR)** above 100% in B2B SaaS for strong expansion motion—segment carefully.

### Leading indicators (early proxies)

Before long retention windows close, use:

- **Activation rate** to “first successful outcome”
- **Frequency** in the natural usage interval (daily/weekly/monthly appropriate to category)
- **Depth of use** (features tied to value, not vanity counts)
- **Repeat purchase / refill / renewal intent** signals

Leading indicators **do not replace** retention; they **predict** it. Validate which leading indicators actually correlate in *your* data.

## Qualitative signals

- **Spontaneous advocacy**: users refer without prompts; champions emerge in accounts.
- **Pain language**: users describe the product as **“must-have”** for their job or life context in interviews (triangulate with quant).
- **Willingness to endure friction**: they tolerate gaps because core value is strong—**dangerous** if you treat that as permission to ignore quality forever.
- **Shrinking sales cycle or lighter sell** in ICP: easier closes for the same value story.
- **Concrete switching costs** users accept because value outweighs migration pain.

Qualitative without quantitative produces false confidence; quantitative without qualitative hides **why** retention breaks.

## Numbered diagnostic workflow

### 1) Define the “market” slice you are testing

Use `.productmap/01_strategy/segmentation/_overview.md` and any ICP notes. PMF is **segment-specific**. “Everyone” is not a market for diagnosis.

### 2) Confirm the core value unit and event

What is the **one outcome** the product must deliver, and what **user action** proves it? Write it in one sentence. If you cannot, measurement will be noise.

### 3) Pull existing evidence from the repo and data locations

Read when available:

- `.productmap/01_strategy/product-market-fit/_overview.md`
- `.productmap/03_analysis/kpis-metrics/_overview.md`
- Qualitative: `.productmap/10_data/interviews/`, `feedback/`, `research/` (paths as present in repo)

Note what is missing (baseline, cohort definitions, survey recency).

### 4) Run quant triage in this order

1. **Cohort retention** (or renewal) for ICP vs non-ICP
2. **Activation** and time-to-value
3. **Sean Ellis** or proxy satisfaction among **activated** users
4. **Organic / unpaid** share of new demand if applicable
5. **Unit economics** sanity (payback, margins) if scaled acquisition is the goal

### 5) Run qual triangulation

- Replay **5–10 recent interviews** or feedback themes; tag must-have vs nice-to-have.
- Check for **forced usage** (enterprise mandate) vs **chosen usage**.

### 6) Diagnose the failure mode

Pick the closest primary failure (often more than one):

- **No acute problem** (problem–solution gap)
- **Problem real, solution weak** (value gap)
- **Value real, wrong segment** (ICP too wide or wrong beachhead)
- **Value + segment OK, broken activation** (onboarding / time-to-value)
- **PMF in one channel only** (product–channel gap)
- **Retention OK, economics broken** (business-model fit)
- **Competitive replacement** eroding wedge

### 7) Decide the next 14–30 day plan

Choose **one** primary lever aligned to the diagnosis (segment narrow, sharpen core loop, fix activation, change packaging, prove retention in one geo, etc.). Avoid ten parallel “PMF initiatives.”

## Path to PMF when you are pre-PMF

- **Narrow the ICP** until metrics improve; widening is for post-PMF scale, not early proof.
- **Instrument the core loop** before building broad roadmaps; if you cannot measure retention, fix analytics first.
- **Ship smallest slices** that complete the core outcome end-to-end; partial features across many jobs delay learning.
- **Talk to users weekly**; store notes under `.productmap/10_data/interviews/` with dates and segment tags.
- **Pre-register falsification**: what evidence would prove this segment is wrong and force a pivot?

Framework lens: `.productmap/08_frameworks/jobs-to-be-done.md` helps restate PMF as **job fulfillment** vs feature lists.

## B2B vs B2C: what changes in PMF measurement

**B2B (especially sales-led or high ACV)**

- **Renewal and expansion** often matter more than early frequency; align windows to **contract length** and onboarding to **first value in production**, not first login.
- **Champion vs economic buyer**: PMF can look good in one persona and fail in procurement; segment interviews and usage by role.
- **Forced adoption** can inflate activity; pair usage with **outcome metrics** tied to customer business results where possible.

**B2C or prosumer**

- **Habit formation** matters; pick retention windows tied to expected return interval (daily, weekly).
- **Organic and referral** signals are often earlier indicators than in enterprise.
- **Sean Ellis** is frequently more actionable earlier in lifecycle if you screen for users who completed the core journey.

**Marketplace / platform**

- PMF is often **two-sided**; diagnose supply and demand separately, then **liquidity** metrics (match rate, time to fulfill, repeat transactions).

If the user’s model is hybrid (PLG into enterprise), explicitly split diagnostics so one side does not drown the other.

## Cohort hygiene (non-negotiable for PMF work)

Before interpreting any chart:

- **Start event**: signup, first purchase, first key action—pick one and stick to it.
- **Universe**: include or exclude trials, invites, sandbox accounts—state the rule.
- **Segmentation**: at minimum **ICP vs non-ICP** once ICP exists; geography and acquisition channel are common cuts.
- **Window honesty**: if you do not have enough calendar time for M6 retention, do not pretend; use leading indicators and smaller windows with labeled uncertainty.

Document these choices in the scorecard so the team does not re-debate definitions every month.

## What “good enough to scale spend” means (practical gate)

Scaling acquisition before PMF usually wastes money. A practical gate (still context-dependent) is:

- **Retention plateau** visible in the ICP for the window that matters, **or**
- A **validated leading-indicator stack** that historically predicted that plateau in analogous products—state the analog explicitly if you use this shortcut.

Pair with **unit economics**: if payback doubles when you leave narrow channels, say so; that is product–channel fit, not moral failure.

## Pitfalls

- **Surveying the wrong denominator** (all mailing list subscribers) and declaring PMF failure or success incorrectly.
- **Treating Sean Ellis 40% as magic** without segment cuts and qualitative follow-up.
- **Optimizing acquisition** on a leaky bucket: PMF work is often retention and activation first.
- **Confusing revenue with PMF**: revenue can be bought; retention cannot be rented long term.
- **Ignoring product–channel fit**: PMF exists in a lab channel but dies at scale CAC.
- **Ignoring product–business-model fit**: great usage, no path to margin.
- **Overfitting vanity metrics** (logins) instead of outcome events tied to value.
- **Single metric tyranny**: use a small **scorecard** (retention + leading + qual + economics) instead of one number.

## Questions to ask the user (pick 6–8)

1. Who is the **ICP** for this PMF assessment, and who is explicitly out?
2. What is the **core value event** and how is it instrumented?
3. What **cohort definition** and **time window** define “retained” for your product?
4. Do you have **Sean Ellis** or equivalent results among **activated** users—how fresh?
5. Is growth **mostly paid**—what happens to retention and organic if spend drops?
6. What is your **natural usage interval** (daily/weekly/etc.), and does product design match it?
7. What **failure** are you seeing (stall at signup, activation, habit, renewal, expansion)?
8. What **economic constraint** must PMF satisfy (payback months, gross margin floor)?

## Artifacts

### PMF scorecard skeleton

Store under `.productmap/00_company/product/` or initiative folder; raw surveys in `.productmap/10_data/`.

```markdown
# PMF scorecard — <Product> — YYYY-MM-DD
## ICP definition (1 paragraph + exclusions)
## Core value event (definition + SQL or analytics source)
## Retention: definition, window, latest cohort chart summary
## Activation: definition, rate, trend
## Sean Ellis: % very disappointed (qualified base definition), n=
## Leading indicators: table (metric, target, actual, owner)
## Qualitative: top 5 themes from interviews/feedback (paths cited)
## Economics: CAC payback / margins (if relevant)
## Diagnosis (1 primary failure mode + evidence)
## Next 30 days (single primary lever + kill criteria)
```

### Segment retention table skeleton

```markdown
# Segment retention — <Product> — YYYY-MM-DD
| Segment | n (cohort) | D1 / W1 / M1 (pick windows) | Core event rate | Notes |
|---------|------------|-----------------------------|-----------------|-------|
| ICP A   |            |                             |                 |       |
| ICP B   |            |                             |                 |       |
| Non-ICP |            |                             |                 |       |
```

### Sean Ellis PMF survey — four questions (verbatim)

Use these wording patterns (replace `[Product]` with your product name):

1. How would you feel if you could no longer use `[Product]`?
   - Very disappointed
   - Somewhat disappointed
   - Not disappointed
   - N/A – I no longer use `[Product]`

2. What type of people do you think would benefit most from `[Product]`?

3. What is the main benefit you receive from `[Product]`?

4. How can we improve `[Product]` for you?

**Analysis note**: The PMF heuristic focuses on the share of **qualified respondents** who choose **Very disappointed** for question 1; questions 2–4 inform ICP sharpening and messaging.

## Cross-references (paths)

- `.productmap/01_strategy/product-market-fit/_overview.md` — canonical PMF framing in this knowledge base.
- `.productmap/01_strategy/segmentation/_overview.md` — who PMF is measured for.
- `.productmap/02_generation/user-research/_overview.md` — discovery practice feeding PMF qual.
- `.productmap/03_analysis/kpis-metrics/_overview.md` — metric discipline and definitions.
- `.productmap/10_data/interviews/` — raw interview storage (create dated subfolders as needed).
- `.productmap/10_data/feedback/` — inbound feedback artifacts.
- `.productmap/10_data/research/` — research notes and synthesis inputs.
- `.productmap/08_frameworks/jobs-to-be-done.md` — JTBD lens on demand and value.

## Operating notes for the assistant

- State **segment**, **cohort**, and **definitions** before interpreting any percentage.
- If data is missing, **design the measurement** instead of guessing PMF status.
- Never claim legalistic certainty (“you have PMF”) from heuristics—communicate **confidence**, evidence, and what would change your mind.
- For “market big enough,” combine **segment retention** with **bottom-up** market math and honest penetration assumptions; point to analysis overviews under `.productmap/03_analysis/` when doing economics.
- Keep recommendations **single-lever biased** for pre-PMF teams to preserve focus.
- Use **absolute dates** when labeling artifacts or referencing study freshness (`YYYY-MM-DD`).

## Quality checklist

- ICP named; denominator for surveys and cohorts explicit.
- At least two **quant** and two **qual** lines of evidence referenced or requested.
- Retention window matches **natural usage** of the category.
- Failure mode stated; next steps map to that mode.
- Repo paths cited for any material claim drawn from this knowledge base.
