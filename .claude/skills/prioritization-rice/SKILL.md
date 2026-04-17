---
name: prioritization-rice
description: Use this skill when the user is prioritizing features, bugs, initiatives, or experiments — or comparing prioritization frameworks. Triggers: "prioritize the backlog", "what should we build next", "RICE score", "MoSCoW", "Kano", "value vs effort", "impact vs effort", "weighted shortest job first", "opportunity scoring".
---

# Prioritization (RICE-centered)

Use this skill when the user needs **comparative ranking** of backlog items, bets, bugs, tech debt packages, or experiments—especially when trade-offs must be explained to engineering, design, and leadership.

This skill is **not** a substitute for **strategy** (where to play, how to win, which outcomes matter). Strategy sets the menu and guardrails; prioritization allocates capacity inside that menu.

## When this skill applies (and when it does not)

**Applies when**

- The team must choose **what ships next** under finite capacity and conflicting stakeholder pulls.
- You need a **transparent scoring model** or a **portfolio view** (value, risk, learning, cost).
- You are comparing **multiple frameworks** (RICE vs MoSCoW vs Kano) and want a sane decision path.

**Delegate / pair with other work**

- **Strategy discovery** (vision, segment choice, business model): use strategy skills and exec alignment first; prioritization without direction optimizes local hills.
- **Discovery research** when the list is wrong: interviewing beats scoring garbage candidates.
- **Project management** when the issue is dependency graphs and staffing—prioritization informs the plan but does not replace critical path analysis.

## Framework map (what each is for, failure modes)

### RICE (Reach × Impact × Confidence ÷ Effort)

- **Goal**: Normalize ideas into a single comparable score with explicit uncertainty.
- **Best when**: Growth/product teams can estimate reach from funnels or accounts; impact is controversial and benefits from a shared scale; effort estimates exist at “t-shirt-plus” fidelity.
- **Failure modes**: **Reach inflation** (counting users who will never see the feature); **Impact grade inflation**; **Confidence used as vibes**; **Effort as calendar time** while ignoring coordination tax; treating the score as **physics** instead of a decision aid.

### ICE (Impact × Confidence ÷ Ease) and close variants

- **Goal**: Lightweight scoring when reach is implicit or constant across items.
- **Best when**: Early-stage lists, small teams, rapid triage workshops.
- **Failure modes**: **Double counting** impact and ease; no shared rubric so numbers become **performative precision**.

### Value vs Effort (2×2)

- **Goal**: Portfolio balance (quick wins, bets, fills, time sinks).
- **Best when**: Communicating to non-numeric stakeholders; spotting **mis-scoped** monsters.
- **Failure modes**: **Value** defined only as revenue; ignoring risk reduction and learning; quadrant labels become political **brands** (“strategic”) that bypass scrutiny.

### MoSCoW (Must / Should / Could / Won’t)

- **Goal**: Timeboxed release planning with stakeholder negotiation language.
- **Best when**: Fixed-date releases; contractual commitments; dependency-heavy roadmaps.
- **Failure modes**: Everything is **Must**; **Won’t** used as a trash heap without governance; no link to **capacity** so “Should” silently becomes “Didn’t”.

### Kano (basic / performance / delighters)

- **Goal**: Classify features by how satisfaction responds to fulfillment level.
- **Best when**: UX differentiation debates; understanding **table stakes** vs **wow**.
- **Failure modes**: Misclassification from **biased surveys**; treating delighters as substitutes for broken basics; static model when category expectations **move over time**.

### WSJF (Weighted Shortest Job First)

- **Goal**: SAFe-flavored scheduling emphasizing **cost of delay** divided by job size.
- **Best when**: Flow-based delivery, train economics, many small items competing.
- **Failure modes**: **Cost of delay** becomes a political knob; job size ignores **integration** costs; applied without WIP constraints so it devolves to local optimization.

### Opportunity Scoring (e.g., OppScore-style composites)

- **Goal**: Blend importance + satisfaction gaps for market problems (common in discovery).
- **Best when**: Choosing among **customer problems** before solution design stabilizes.
- **Failure modes**: Importance measured with **leading questions**; gap scores without segment control; **double counting** the same signal in multiple factors.

### Buy-a-Feature (game)

- **Goal**: Reveal trade-offs by giving stakeholders a limited budget to “purchase” capabilities.
- **Best when**: Cross-functional alignment workshops; surfacing hidden weights.
- **Failure modes**: **Hippos** dominate budget; participants optimize for their silo; outputs treated as **statistical truth** from a game.

## Decision tree (choose a framework)

1. **Is the decision primarily about learning** (unknown problem/solution)? Prefer **discovery framing** first; if you must rank experiments, use small **ICE** or explicit **learning metrics**, not big RICE theater.
2. **Is there a fixed date release with contractual musts?** Start with **MoSCoW** plus capacity, then optionally RICE within buckets.
3. **Is UX differentiation the debate?** Add **Kano** (qualitative + thin quant) before effort-heavy build commitments.
4. **Is flow/queue economics the pain?** Consider **WSJF** if your organization already speaks cost-of-delay; otherwise keep RICE/effort explicit.
5. **Do you need one comparable backlog score across heterogeneous items?** Use **RICE** with a written rubric and calibration examples.
6. **Do you need executive storytelling without numbers?** Use **2×2** plus a short narrative; keep numeric scoring as appendix.
7. **Are stakeholders talking past each other on weights?** Run **Buy-a-Feature** once, then encode the revealed weights into a simpler model.

You may combine frameworks **sequentially** (Kano to remove table stakes from “delighter debates,” then RICE on the remainder), but avoid stacking multipliers that double-count the same underlying belief.

## RICE — definition and units

**Formula (plain)**

`RICE = (Reach × Impact × Confidence) / Effort`

Where `Confidence` is expressed as a decimal multiplier (for example, 80% → `0.8`).

**Reach**

- Definition: **How many people/events** this touches per the chosen time window (e.g., monthly active users affected, accounts, support tickets prevented).
- Units: pick one denominator and **stick to it** across the backlog for comparability (e.g., “affected MAU per month”).

**Impact**

- Use a **shared ordinal scale** mapped to multipliers:

  - **3 — Massive**: step-change in core outcome for the segment (e.g., major revenue, retention, compliance).
  - **2 — High**: clear measurable lift on a primary metric.
  - **1 — Medium**: meaningful improvement for a subset or secondary metric.
  - **0.5 — Low**: incremental quality-of-life improvement.
  - **0.25 — Minimal**: small polish, minor annoyance removal.

- Calibrate with **anchors**: write 2–3 past shipped items as examples per score.

**Confidence**

- Express as a multiplier **0.00–1.00** with standard bands:

  - **100%**: strong evidence (production data, repeated experiments, validated prototypes).
  - **80%**: good evidence (multiple customer signals, partial data).
  - **50%**: educated guess (some interviews, analogies, incomplete data).

- If confidence should be **<50%**, you usually need **discovery work**, not a prioritization meeting.

**Effort**

- Person-**weeks** or person-**months** of core team time (PM/design/engineering) as your org estimates it, including **review, rollout, and instrumentation** if non-trivial.
- Keep units consistent; document whether QA/support load is included.

## Worked example (three features, same units)

Assume: Reach = affected MAU per month; Impact uses the 3–0.25 scale; Confidence uses 1.0/0.8/0.5; Effort in person-months.

| Item | Reach | Impact | Confidence | Effort | Computation | RICE |
| --- | ---: | ---: | ---: | ---: | --- | ---: |
| **A — Onboarding checklist** | 4,000 | 1 | 0.8 | 2 | (4000×1×0.8)/2 | **1,600** |
| **B — Enterprise SSO bugfix** | 600 | 2 | 1.0 | 1.5 | (600×2×1)/1.5 | **800** |
| **C — Analytics export CSV** | 900 | 0.5 | 0.5 | 0.75 | (900×0.5×0.5)/0.75 | **300** |

**Read**

- A wins on breadth with medium impact and decent confidence.
- B is smaller reach but **high impact** and **high confidence**—often politically urgent even if RICE is mid-pack.
- C is **speculative** (low confidence) and modest impact—candidate for discovery or scope split.

Always ask: **Does the ranking violate obvious risk constraints?** (security, incidents, regulatory). Override with explicit **guardrails**, not silent fudge factors.

## Workflow (runbook a–g)

a. **Frame the decision**: horizon (quarter/month), capacity, and what “done” means for an item entering the list.

b. **Normalize the backlog item grain**: epics broken until effort estimates are comparable; spikes labeled as timeboxes.

c. **Pick the primary framework** using the decision tree; add secondary lenses only where they change decisions.

d. **Write the rubric anchors** (impact examples, reach definition, confidence evidence rules).

e. **Score independently** (blind) where politics are hot; then reconcile assumptions, not numbers first.

f. **Sensitivity check**: move confidence ±1 band and effort ±30% for top contenders—does rank order flip? If yes, clarify what evidence resolves it.

g. **Publish**: ranked list + assumptions + explicit non-goals + next validation steps; store in backlog artifact paths (see cross-refs).

## Pitfalls (common failure modes)

1. **Precision theater**: three decimal RICE scores that hide garbage assumptions.
2. **Reach as TAM**: counting theoretically addressable market instead of in-product affected users.
3. **Effort without risk**: ignoring unknown integrations, data migrations, or compliance review.
4. **Ignoring opportunity cost**: high RICE “nice” vs urgent “stop the bleeding” incidents—use separate **tier-0** lanes.
5. **Framework shopping** to ratify a preselected favorite—run blind steps first.
6. **No instrumentation**: you cannot update confidence after ship without baseline metrics.
7. **Stakeholder weights missing**: one model cannot serve exec risk reduction and growth team learning without explicit **objective mixing** (or separate lists).
8. **Moralizing scores**: people labeled “low impact” instead of items; destroys calibration honesty.

## Questions to ask the user before scoring

1. What **time horizon** and **capacity** boundary does this ranking serve (`YYYY-MM-DD` range)?
2. Are we prioritizing **customer-visible outcomes**, **platform reliability**, or a **mixed portfolio**—and what split is intended?
3. What is the **Reach definition** denominator (users, accounts, events, money)?
4. What **evidence** exists for top items (analytics links, support volume, contracts)?
5. What **non-negotiables** override scoring (security, legal, incidents)?
6. Who **owns** estimates (engineering effort, PM impact calls), and how will disagreements be resolved?
7. What **success metrics** will confirm impact after delivery?
8. Should results be written back to the repo backlog path, and under which initiative folder?

## Artifacts (skeletons)

### RICE scorecard (Markdown table)

Columns:

- Item
- Reach (# + definition note)
- Impact (3/2/1/0.5/0.25 + 1-line rationale)
- Confidence (100/80/50% + evidence bullets)
- Effort (# + unit + scope notes)
- RICE (computed)
- Dependencies / risk flags
- “If wrong” test (what would falsify the score)

### Portfolio commentary (short)

- **Top 5** by RICE with narrative “why safe / why risky”
- **Overrides** (incidents, commitments) listed explicitly
- **Learning backlog** items that should not be RICE-compared to production features without normalization

### Workshop one-pager (MoSCoW + capacity)

- Must bucket with **capacity check** (hours/story points)
- Should/Could with **pull rules** (how items advance)
- Won’t with **review date** (`YYYY-MM-DD`)

## Repo cross-references (read before writing)

- `.productmap/08_frameworks/rice.md`
- `.productmap/08_frameworks/other-frameworks.md`
- `.productmap/04_delivery/backlog-requirements/_overview.md`
- `.productmap/00_company/product/backlog.md`

Navigation entrypoint when unsure where content lives: `.productmap/index.md`.

## Conventions

- Use **absolute dates** (`YYYY-MM-DD`) when recording prioritization decisions and review cadences.
- Treat scores as **hypotheses**; pair with **instrumentation** and post-ship review.

## Advanced notes (optional, keep short in outputs)

- **Normalize across teams** by publishing two example score sets per quarter (“gold standard references”).
- For **bugs**, consider reach as incident rate × blast radius, impact as customer severity, confidence from reproduction quality.
- For **tech debt**, split “interest payments” (incident reduction) from “option value” (velocity); mixing without labels confuses stakeholders.

## ICE (compact variant) for comparison

`ICE = (Impact × Confidence) / Ease`

Use ICE when reach is intentionally **held constant** (same funnel surface, same customer list) or when you are ranking **discovery bets** where “who is affected” is not yet defined. If you later define reach, re-home the item into RICE to avoid comparing ICE-ranked bets with RICE-ranked shipping work without a **translation note**.

## Calibration workshop (60–90 minutes, suggested flow)

1. **Agree units** (reach denominator, effort units, time window) before any scores.
2. **Review anchors** for impact multipliers using past shipped work examples.
3. **Silent scoring** on a short list (5–10 items), then reveal ranges (min/median/max).
4. **Debate assumptions** for the widest spreads first—those are where information value is highest.
5. **Assign evidence tasks** (who pulls what metric, by which `YYYY-MM-DD`) before re-scoring contentious items.
6. **Lock v1 ranking** with a review date; schedule **post-ship confidence updates**.

## Governance (keep scoring honest)

- Publish a **change log** when rubrics shift; do not stealth-edit historical scores.
- Separate **tier-0 work** (incidents, regulatory) from discretionary RICE lists so teams do not “score” emergencies.
- Require a **single owner** per item for estimates (usually EM for effort, PM for impact hypothesis, DS/PM for reach analytics).
- When leadership overrides the model, capture **reason in writing** next to the item to preserve learning.

## Quality bar

- Rubric anchors exist; scores are **debated as assumptions**, not argued as personality.
- Rank order flips under sensitivity analysis are **resolved with evidence plans**, not hidden weights.
- Overrides are **explicit**; the model is not silently bent to match politics.
