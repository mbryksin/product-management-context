---
name: unit-economics
description: Use this skill when the user is modeling, improving, or reviewing unit economics — CAC, LTV, payback, contribution margin, gross margin, cohort economics. Triggers: "unit economics", "LTV:CAC", "payback period", "contribution margin", "is this business viable", "cohort economics", "CAC payback", "burn multiple".
---

# Unit economics

## When this skill applies

Use this skill when the user is **modeling, stress-testing, improving, or reviewing** how much value a business captures per customer or transaction relative to the cost to acquire and serve that unit — including CAC, LTV, payback, margins, retention economics, and capital efficiency proxies like burn multiple.

Typical triggers include: **unit economics**, **LTV:CAC**, **payback period**, **contribution margin**, **gross margin**, **cohort economics**, **CAC payback**, **burn multiple**, **“is this business viable?”**, **SaaS efficiency**, **take rate / GMV economics**.

## When this skill does not apply

- **Company-wide financial statements** without a clear “per customer” or “per order” lens (use finance forecasting / FP&A framing instead, though you may still bridge to unit drivers).
- **Pure pricing psychology** with no cost or margin structure (use pricing/packaging skills).
- **Operational metrics** with no acquisition or lifetime value story (still useful, but not “unit economics” unless tied to a unit definition).
- **Fundraising narrative only** with no underlying definitions, time windows, or segment splits (push back gently: unit economics need explicit definitions).

## Definitions (build a shared glossary before debating numbers)

### What is a “unit”?

A **unit** is the atomic economic actor you normalize on. Common choices:

- **B2B SaaS**: one **account** (company) or one **seat** (user license). Pick one and stay consistent; seat models often need both views.
- **Marketplace**: one **buyer**, one **seller**, or one **transaction** / **order** — often you need **two-sided** unit economics (supply vs demand).
- **Consumer subscription**: one **subscriber** (household or individual).
- **Transactional / e‑commerce**: one **order** or one **customer** over a defined horizon.

If the unit is ambiguous, every ratio below is meaningless.

### CAC (Customer Acquisition Cost)

**CAC** answers: *how much did we spend to win a new customer (or unit) in a period?*

- **Blended CAC**: total sales and marketing spend in a period divided by **new customers** acquired in the **same** period (or aligned lag if you model attribution delay).
- **Paid CAC**: paid marketing spend divided by customers attributed to **paid** channels (excludes organic/word-of-mouth unless you explicitly include it in the numerator).

Be explicit whether “new” means **logos**, **paid conversions**, **reactivations**, or **expansions** — mixing definitions inflates or deflates CAC.

### LTV (Lifetime Value)

**LTV** answers: *how much gross profit do we expect from a customer over their lifetime (or a bounded horizon)?*

LTV is not “all revenue ever” unless you also subtract variable costs consistently.

### Margins (do not conflate)

- **Gross margin**: revenue minus **COGS** (cost of goods sold / direct delivery cost). Common for SaaS: hosting, support load, payment fees, third-party API costs tied to delivery.
- **Contribution margin**: gross margin minus **variable costs of serving and retaining** the customer that scale with usage (sometimes overlaps with COGS; the key is **consistency** across LTV and payback).

For **unit economics**, prefer **contribution margin** for LTV when the business has meaningful variable costs per active user.

### Payback period

**CAC payback** answers: *after acquiring a customer, how many months until cumulative contribution margin repays CAC?*

Use the **same margin definition** in payback as in LTV, or you will double-count optimism.

### LTV:CAC ratio

**LTV:CAC** compares expected lifetime contribution to acquisition spend. It is a **sanity check**, not a strategy.

### Churn (types)

- **Logo churn**: customers lost / starting customers in period.
- **Revenue churn**: ARR or MRR lost from downsells and churn / starting revenue base.
- **Voluntary vs involuntary**: payment failures, cancellations, seasonality — cohort views expose this.

### NRR and GRR (SaaS expansion economics)

- **GRR (Gross Revenue Retention)**: how much revenue you **retain** from the starting cohort excluding expansion (capped at 100%).
- **NRR (Net Revenue Retention)**: starting cohort revenue including expansion, contraction, and churn — can exceed 100% in strong expansion motion.

These shape **LTV** materially; ignoring expansion in B2B SaaS often understates LTV.

### Burn multiple

**Burn multiple** (common VC framing): **net burn** divided by **net new ARR** in the same period. It measures **how much cash you burn to add a dollar of ARR**. Lower is generally better; context matters (investment mode vs efficiency mode).

### CAC efficiency (family of metrics)

“CAC efficiency” is overloaded. Clarify which proxy you mean:

- **LTV:CAC**
- **CAC payback months**
- **Magic number**-style sales efficiency (variations exist; define the formula you use)
- **S&M as % of revenue** (lagging, but sometimes requested)

## Explicit formulas (state the time window and cohort definition)

### CAC (period)

\[
\text{CAC} = \frac{\text{Sales \& Marketing spend in period}}{\text{New customers acquired in period}}
\]

If using **paid CAC**, restrict numerator and denominator to paid-attributed spend and customers.

### LTV — simple subscription sketch

Let:

- \(A\) = average revenue per account per month (**ARPA**), or MRR per account
- \(m\) = contribution margin rate (0–1) on that revenue
- \(c\) = monthly churn rate (logo churn or revenue churn — **pick one** and label it)

A common **simple** form (geometric lifetime approximation):

\[
\text{LTV} \approx A \times m \times \frac{1}{c}
\]

This assumes constant churn and margin; real cohorts violate this, so treat it as a **first-order** model.

### LTV — discounted (note)

A more defensible approach is the **present value** of expected future contribution margins:

\[
\text{LTV} = \sum_{t=1}^{T} \frac{\text{contribution margin in month }t}{(1+r)^t}
\]

where \(r\) is a monthly discount rate (or map to annual consistently) and \(T\) is a cap (e.g., 36–60 months) or until survival probability is negligible. **Document** \(r\), \(T\), and churn assumptions.

### CAC payback (months)

Let **GPcm** = gross profit or contribution profit per customer per month (consistent with LTV).

\[
\text{Payback (months)} = \frac{\text{CAC}}{\text{GPcm}}
\]

If revenue ramps (land-and-expand), use a **month-by-month** cumulative margin curve rather than a flat GPcm.

### LTV:CAC

\[
\text{LTV:CAC} = \frac{\text{LTV}}{\text{CAC}}
\]

### Burn multiple (ARR framing)

\[
\text{Burn multiple} = \frac{\text{Net burn in period}}{\text{Net new ARR in period}}
\]

Define **net new ARR** exactly (new + expansion − churn − contraction, or the subset your org uses).

## Benchmarks (rules of thumb — not laws)

Treat benchmarks as **hypotheses** until validated for your segment, ACV, and motion.

- **LTV:CAC**: many SaaS investors like **> 3:1** on **fully loaded** CAC and **contribution-based** LTV; weaker ratios can work with very fast payback or strategic reasons, but need explanation.
- **CAC payback**:
  - **SaaS (common target)**: **< 12 months** for SMB/mid-market PLG or velocity sales (many orgs aim tighter; enterprise may differ).
  - **Consumer subscription**: often expected **< 6 months** when paid acquisition dominates (varies widely by category).
- **GRR / NRR**: benchmark against **peers with similar ACV**; NRR > 100% is a major LTV lever in expansion-led B2B.

Always pair benchmarks with **payback** and **retention quality**, not LTV:CAC alone.

## Business-model lenses (what changes the model)

### SaaS (subscription)

Focus on **MRR/ARR**, **retention (GRR/NRR)**, **COGS at scale**, **S&M efficiency**, **services margin** if heavy onboarding/pro services, and **multi-year contracts** (cash vs revenue timing).

### Marketplace (two-sided)

Separate **supply CAC**, **demand CAC**, and **liquidity metrics** (match rate, time-to-first-transaction, repeat purchase). LTV often ties to **transactions × take rate × variable margin**, not subscription LTV.

### Consumer subscription

Often **high churn**, **price sensitivity**, and **paid marketing volatility**. Cohort curves and refund/chargeback costs matter. Payback targets are typically aggressive.

### Transactional / e‑commerce

Unit may be **order** or **customer**. Repeat purchase rate, return rate, shipping subsidy, and payment fees dominate. LTV may be a **12–24 month** horizon rather than “lifetime.”

## Cohort vs blended (avoid the classic trap)

- **Blended metrics** across all customers smooth curves and hide **weak cohorts** or **channel toxicity**.
- **Cohort curves** (by signup month, channel, segment, price plan) reveal true retention and spend ramps.

**Rule**: use blended for **portfolio** discussion; use cohorts for **diagnosis** and forecasting.

## Additional formulas and variants (use labels religiously)

### Magic number (sales efficiency — one common variant)

Organizations define this differently. A frequently cited quarterly form:

\[
\text{Magic number} \approx \frac{\text{Net new ARR in quarter} \times 4}{\text{Prior quarter S\&M expense}}
\]

Interpretation is contextual; treat it as a **directional** efficiency signal, not a substitute for cohort retention quality. If you use a different definition, print it verbatim in the artifact header.

### Transactional LTV (orders over a horizon)

If the unit is **orders** in a 12-month horizon:

\[
\text{LTV}_{12} \approx (\text{orders per customer per year}) \times (\text{average order value}) \times (\text{contribution margin rate}) - (\text{returns/chargebacks adjustments})
\]

Then compare to **CAC** only if CAC is defined as cost to acquire a **customer**, not an order.

### Marketplace contribution (single transaction view)

For one transaction:

\[
\text{Contribution} = \text{GMV} \times \text{take rate} - \text{variable costs of fulfillment}
\]

Separate **supply-side** and **demand-side** acquisition costs; do not collapse them without stating the subsidy strategy.

### Payback with ramping expansion (conceptual)

If month-\(t\) contribution margin is \(CM_t\) (non-constant), payback is the smallest \(k\) where:

\[
\sum_{t=1}^{k} CM_t \ge \text{CAC}
\]

This is the correct approach for land-and-expand SaaS when ARPA rises materially after month 0.

## Data dictionary (what each field must mean)

Before calculating, write a one-page **data dictionary**:

- **Customer ID** stability (CRM vs product vs billing).
- **MRR definition** (contracted vs billed vs recognized).
- **New vs resurrected** customer rules.
- **Free trials** (exclude until paid conversion?).
- **Multi-product** revenue allocation (if one customer buys two products).
- **FX and tax** handling (inclusive vs exclusive).

Most “unit economics debates” are actually **join key** debates.

## Segment and channel cuts (minimum diagnostic grid)

When data allows, compute **CAC, payback, LTV, LTV:CAC** (or the available subset) across:

- **ACV band** (micro vs mid vs enterprise).
- **Acquisition channel** (paid search, social, partner, outbound, organic).
- **Geo** (if pricing and support costs differ).
- **Plan / price tier** (if feature gating changes COGS).

If the user lacks data, output the **requested pivot table spec** (columns, filters, cohort key) so analytics can produce it.

## Business-model lenses — expanded checklists

### SaaS (subscription) — deeper checklist

- Contract terms: monthly vs annual vs multi-year; discounts and ramp deals.
- Professional services: margin dilution, delivery backlog, and whether services revenue should be excluded from “software LTV.”
- Usage-based components: minimum commits, overages, and metering latency.
- Support cost drivers: ticket rate by segment, severity SLAs, and AI-assisted deflection effects (if any).

### Marketplace (two-sided) — deeper checklist

- Subsidy policy: who is subsidized and for how long (supply promos vs demand coupons).
- Liquidity: active buyers/sellers, match rate, cancellation rate, fraud loss.
- Disintermediation risk: off-platform leakage that removes take rate from measured GMV.

### Consumer subscription — deeper checklist

- Refund windows, chargeback rates, and platform fees (app stores).
- Seasonality and cohort maturity (annual holidays, New Year’s resolution cycles).
- Creative fatigue in paid social (CAC volatility).

### Transactional / e‑commerce — deeper checklist

- Contribution margin after shipping subsidy and packaging.
- Repeat purchase cadence (category-dependent).
- Inventory risk (if relevant) and how it is excluded from “unit” contribution.

## How to narrate results without overclaiming

- Lead with **definitions**, then **baseline**, then **sensitivity**, then **decisions**.
- Separate **observed** cohort outcomes from **forecast** assumptions.
- If two margin bases are used for different audiences, print **two** payback numbers with labels—never merge silently.

## Workflow (runbook)

a) **Define the unit** (account vs seat vs order) and the **segment** (SMB vs enterprise, channel, geography).

b) **Freeze definitions** for “new customer,” revenue (bookings vs billings vs recognized), and margin (gross vs contribution).

c) **Build the baseline model** with explicit time windows (monthly/quarterly) and data sources.

d) **Layer cohort views** for retention, expansion, and payback realism; compare to blended.

e) **Stress-test** (sensitivity): churn +20%, CAC +30%, price −10%, COGS +15%.

f) **Identify levers** (see below) and pick 3–5 measurable bets with owners and dates (`YYYY-MM-DD`).

g) **Write the artifact** with assumptions, formulas, and links to evidence under `.productmap/10_data/` when raw exports exist.

## Improvement levers (prioritize by sensitivity)

- **Retention / activation**: improve time-to-value; fix involuntary churn; tighten onboarding.
- **Pricing / packaging**: raise ARPA without equal churn increase; introduce usage tiers aligned to value.
- **Channel mix**: shift spend toward channels with superior **marginal** CAC at scale (not just cheap CPA).
- **Sales efficiency**: win rates, cycle length, ramp; AE vs PLG balance.
- **COGS / variable cost**: infra efficiency, fraud/returns, payment fees, model cost for AI features.
- **Expansion motion**: cross-sell/upsell; usage-based pricing where fair.

## Pitfalls (common ways unit economics lie)

1. **Mixing bookings with revenue** in LTV while using **cash CAC** (or the reverse).
2. **Excluding fully loaded S&M** (tools, salaries, agencies) from CAC while claiming “paid CAC only” without relabeling.
3. **Using static churn** when early cohorts are immature (under-counting churn that has not happened yet).
4. **Ignoring gross margin** and calling revenue “LTV.”
5. **Attribution lag**: spend precedes conversion; misaligned windows distort CAC.
6. **Survivorship bias**: modeling only best customers or only annual plans.
7. **Blending segments** with radically different ACV and churn (hides unprofitable pockets).
8. **One-sided marketplace math** pretending supply and demand share the same “customer.”

## Questions to ask the user (if missing)

1. What is the **unit** (account, seat, order, seller, buyer)?
2. What **segment and channel** is this model for?
3. Do you want **gross margin** or **contribution margin** in LTV and payback?
4. What **time window** defines CAC spend and matched acquisitions?
5. Is churn measured on **logos** or **revenue**, and is **expansion** included in LTV?
6. Are we including **services**, **implementation fees**, and **usage overages**?
7. What is the **intended horizon** (12 months vs 5 years) and do you want a **discount rate**?
8. What **evidence** exists (cohort exports, finance actuals) and where is it stored in the repo?

## Artifacts (suggested outputs)

- **Unit economics one-pager** (definitions + baseline + sensitivity + decisions).
- **Cohort appendix** (curves, channel cuts, segment cuts).
- **Investment memo section** (LTV:CAC, payback, burn multiple with explicit formulas).

Suggested storage (if writing to the repo):

- Initiative artifact: `.productmap/00_company/product/<initiative>/unit-economics-YYYY-MM-DD.md`
- Raw exports / spreadsheets notes: `.productmap/10_data/<initiative>/...`

Use **absolute dates** (`YYYY-MM-DD`) on artifacts.

## Repo cross-references (read before contradicting local guidance)

- `.productmap/03_analysis/unit-economics/_overview.md`
- `.productmap/03_analysis/finance/_overview.md`
- `.productmap/03_analysis/kpis-metrics/_overview.md`
- `.productmap/01_strategy/business-model/_overview.md`
- Navigation index: `.productmap/index.md`

If local `_overview.md` content conflicts with generic benchmarks, **prefer the repo** and note the delta explicitly.
