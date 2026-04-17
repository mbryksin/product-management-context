---
name: product-strategy-roadmap
description: Use this skill when the user asks about product strategy, vision, roadmaps, MVP scoping, product maturity stages, time-horizon planning (now/next/later), or turning strategy into a sequenced plan. Triggers — "build a roadmap", "what's our strategy", "scope the MVP", "now/next/later", "strategic narrative", "product vision".
---

# Product strategy and roadmap

Use this skill when the conversation is about **where to play**, **how to win**, **what to build in what order**, and **how horizons connect**—not when the user only wants tactical delivery detail without strategic framing.

## When this skill applies

- The user wants a **roadmap** (outcome-based, time-horizon, or both) grounded in company context.
- They ask for **strategy**, **strategic narrative**, **positioning choices**, or **sequencing** across quarters or themes.
- They need **MVP scoping** or a defensible cut line between “must ship” and “later.”
- They reference **now / next / later**, **themes**, **bets**, or **portfolio** language.
- They want to translate **vision** into something operational (choices, outcomes, sequence).

## When it does not apply (use something else)

- **Pure execution**: sprint planning, story breakdown, acceptance criteria only—use delivery templates and engineering rituals; strategy skill adds noise.
- **Deep user research synthesis** without strategic choices—start at `.productmap/02_generation/user-research/_overview.md` and research templates.
- **Financial modeling or unit economics deep-dive**—use `.productmap/03_analysis/` overviews and finance-oriented artifacts.
- **Stakeholder negotiation or procurement**—use `.codex/skills/negotiation-prep-brief/SKILL.md` when the core ask is the conversation, not the roadmap.
- **AI feature specification**—use `.codex/skills/ai-feature-brief/SKILL.md` when the scope is model behavior, evals, and guardrails rather than portfolio sequencing.

## Core distinctions (use these words consistently)

### Vision vs strategy vs roadmap vs backlog

- **Vision**: a directional picture of the future (who we serve, what world we enable). Inspiring but not a decision log.
- **Strategy**: explicit **choices**—where we play, how we win, what we will not do, and which capabilities matter. Strategy is falsifiable and debatable.
- **Roadmap**: a **communicated sequence** of intended outcomes or initiatives over time, aligned to strategy. It is not a promise of fixed dates for every item unless you have earned that predictability.
- **Backlog**: ordered work items (often features or tasks). It implements slices of the roadmap; it should not replace strategy or outcomes language at leadership level.

If the artifact mixes these levels, readers will argue about dates instead of choices. Keep layers separate, then show linkage.

### Outcome roadmap vs feature roadmap

- **Outcome roadmap**: each horizon or theme ties to a **measurable user or business outcome** (e.g., activation rate, time-to-value, margin per order). Features are derived later.
- **Feature roadmap**: lists **shipping objects** (capabilities, integrations). Useful for engineering and dependencies; dangerous as the only leadership view because it hides tradeoffs and learning.

Default to **outcomes** for exec and cross-functional alignment; use **features** as a drill-down under each outcome or bet.

### Now / next / later vs timeline roadmap

- **Now / next / later**: buckets that communicate **uncertainty** and **focus**. “Now” is resourced and committed; “next” is prioritized but not fully committed; “later” is directionally right but uncommitted. Good when date confidence is low or discovery is high.
- **Timeline roadmap** (quarters, months): useful when release predictability, marketing beats, or compliance windows matter. Risk: false precision.

Often combine them: **N/N/L for themes** plus a **thin timeline** only for hard external dates and committed launches.

## Numbered workflow

### 1) Clarify the planning horizon and audience

- **Horizon**: Are we planning 30–90 days, one quarter, one year, or multi-year narrative?
- **Audience**: IC team, leadership, board, customers? Each needs different granularity and certainty language.
- **Maturity**: idea, MVP, growth, scale—stage changes what “roadmap” means (learning vs extraction).

Document assumptions about predictability. If the team is pre-PMF, the roadmap should foreground **learning milestones**, not only ship dates.

### 2) Read repo context before inventing structure

In order:

1. `.productmap/index.md` — navigation and links to the right overviews and templates.
2. `.productmap/00_company/product/roadmap.md` — existing roadmap intent, if populated. Treat as source of truth unless the user says it is stale.
3. `.productmap/01_strategy/` — scan overviews relevant to the question:
   - `mvp-roadmap/_overview.md` for MVP and sequencing discipline.
   - `business-model/_overview.md` for value capture and constraints.
   - `segmentation/_overview.md` for who you optimize for across horizons.

If these files are empty, say so explicitly and propose a minimal structure rather than backfilling fiction.

### 3) Lock strategic choices (where to play / how to win)

Strategy is incomplete without **tradeoffs**. Capture:

- **Where to play**: segments, geos, use cases, platforms, price tiers.
- **How to win**: differentiation, distribution, ecosystem, speed, cost position—pick the coherent theory.
- **Non-goals**: what you deprioritize or refuse for the planning window.

If the user cannot state non-goals, spend effort there; roadmaps without non-goals become “yes to everything” lists.

### 4) Map choices to outcomes (not features first)

For each strategic theme:

- **Outcome**: user behavior or economic metric moved.
- **Leading indicator**: early signal in weeks, not quarters.
- **Initiative / bet**: the container of work that pursues the outcome.

Only then attach candidate features or projects. This order preserves alignment when solutions change.

### 5) Sequence: dependencies, learning, and capacity

Sequence using:

- **Hard dependencies**: compliance, infra, data, partnerships.
- **Learning order**: cheapest tests that invalidate the riskiest assumptions first (see also `.productmap/01_strategy/mvp-roadmap/_overview.md`).
- **Capacity and focus**: fewer parallel “now” themes than teams think they can run without thrash.

Expose **critical path** and **optionality** (“if X validates, we accelerate Y”).

### 6) Pressure-test the roadmap

Ask:

- If we delivered every “now” item and nothing moved on the metrics, what failed—strategy, measurement, or execution?
- Does “next” contain disguised commitments (pre-sold to customers or sales)?
- Does “later” hide pet projects that will never die?
- Where is **single-threaded ownership** per theme?

Revise until the roadmap tells a coherent story: choices → outcomes → sequence → risks.

## Product maturity: how roadmap emphasis shifts

**Idea / pre-MVP**

- Emphasize **discovery milestones**, interview throughput, prototype tests, and technical spikes.
- Keep “now” small; protect time for learning. Dates are often **fake**; use gates and learning budgets instead of quarter-by-quarter feature promises.

**MVP / early traction**

- Split roadmap into **value path** (first successful user journey) vs **everything else**.
- Sequence work to reduce **time-to-first-value** and **retention in the core loop**; defer platform grandeur unless it blocks the loop.

**Growth**

- Roadmaps must respect **distribution**, **conversion**, and **unit economics**; product-only sequencing is insufficient.
- “Next” should include experiments with **pre-defined success metrics** and kill rules, not only shipped features.

**Scale / maturity**

- Roadmaps incorporate **reliability**, **cost of serve**, **compliance**, and **multi-segment complexity**.
- Stronger timeline views are appropriate where process and predictability exist; still keep outcomes visible to avoid local optimization.

If the user’s stage and roadmap format disagree (for example, a Gantt-first plan for a pre-MVP product), call that out and propose a better-fitting format.

## Theme and bet hygiene

A **theme** is a narrative umbrella (often customer- or business-visible). A **bet** is a scoped investment with owners, money/time box, and falsification criteria. Good roadmaps use both:

| Element | Definition | Good signal | Bad signal |
|--------|------------|-------------|------------|
| Theme | Why this cluster of work matters now | 2–4 themes max for “now”; each maps to strategy | Ten “strategic pillars” |
| Bet | A testable investment inside a theme | Kill / persevere criteria written in advance | “Strategic project” with no metric |
| Outcome | What moves if the bet works | Numerator/denominator explicit | Vague “better UX” |
| Initiative | Delivery container | Clear scope boundary and dependency list | Endless backlog under one label |

When themes multiply, you usually have a **political merge** problem, not a prioritization tool problem. Help the user collapse or sequence.

## Dependencies: three layers to scan

1. **Customer / market**: regulatory windows, seasonal demand, competitor moves, partner roadmaps.
2. **Internal product / tech**: data availability, platform limits, security review, migration risk.
3. **Org**: hiring plan, vendor procurement, sales commitments, marketing launches.

Missing any layer produces roadmaps that look logical on a slide and fail in reality. If the repo has delivery overviews under `.productmap/04_delivery/`, skim for engineering and risk practices that should inform sequencing language.

## Communication: how to present the same roadmap at three altitudes

**Leadership (10–15 minutes)**

- Choices, non-goals, outcomes for the horizon, top risks, resource focus.
- Avoid backlog granularity; offer a “drill-down path” to PRDs or epics.

**Cross-functional teams (45–60 minutes)**

- Themes, outcomes, initiative list, dependencies, decision log, open questions.
- Connect to `.productmap/09_templates/prd-template.md` triggers: when does an item earn a PRD?

**Engineering / design execution**

- Feature or epic view under each outcome, acceptance themes, technical milestones.
- Still keep the **outcome line** visible so tradeoff debates do not become taste contests.

## Review cadence (suggested defaults)

These are defaults to propose when the user has no operating model yet:

- **Weekly**: “now” execution health—unblock dependencies; no roadmap rewrites unless a gate fails.
- **Monthly**: theme progress vs leading indicators; promote/demote items between now and next.
- **Quarterly**: strategy and portfolio refresh—revisit where-to-play / how-to-win if metrics or market materially moved.

Tie cadence to **decision rights**: who can move something from “next” to “now,” and who can stop a bet.

## Artifacts (templates and skeletons)

Store initiative-specific artifacts under `.productmap/00_company/product/` unless the user specifies otherwise. Prefer adapting files from `.productmap/09_templates/` over inventing new section names.

### A) One-pager strategy

Purpose: one screen of **choices, logic, and implications** for leaders.

Skeleton (3–6 lines of structure; expand with user content):

```markdown
# <Initiative> — Strategy one-pager — YYYY-MM-DD
## Context & stakes (5 bullets max)
## Where we play / who we serve (with non-goals)
## How we win (theory + proof we need)
## Implications for product (capabilities, distribution, data)
## 90-day focus & metrics
## Top risks & early signals
```

Cross-ref: align narrative sections with `.productmap/09_templates/board-deck-template.md` if the output must become a deck; use `.productmap/09_templates/prd-template.md` when moving from strategy to scoped delivery for a concrete bet.

### B) Now / next / later roadmap

Purpose: communicate **focus and uncertainty** without fake precision.

Skeleton:

```markdown
# <Product> — Roadmap (Now / Next / Later) — YYYY-MM-DD
## Strategic themes (2–4)
## Now (committed through <date>)
- Theme → outcome → leading indicator → key initiatives
## Next (prioritized, gated by <signals>)
## Later (directional)
## Dependencies & decisions waiting
## What we are explicitly not doing (this half)
```

Cross-ref: tie outcomes language to frameworks under `.productmap/08_frameworks/` (for example prioritization or jobs thinking—see `jobs-to-be-done.md` if useful for framing problems).

### C) Outcome roadmap (by horizon or quarter)

Purpose: connect **time** to **measurable outcomes** for planning and exec review.

Skeleton:

```markdown
# <Product> — Outcome roadmap — YYYY-MM-DD
## North-star / guiding metric (define numerator & denominator)
## Horizon Q1 / H1 / FY (pick one framing)
### Outcome, baseline, target, leading indicator
### Bets & scope notes (high level)
### Risks & kill criteria
## Cross-theme dependencies
## PRD / epic triggers (link to drafting in prd-template when ready)
```

Cross-ref: when an outcome becomes a buildable scope, draft with `.productmap/09_templates/prd-template.md`.

## Pitfalls

- **Feature laundry lists** without outcomes: everyone nods; nobody agrees what “good” means.
- **Roadmap as contract** in high-uncertainty stages: destroys trust when reality changes; use language of intent and gates.
- **Strategy slides with no non-goals**: not strategy—wishful thinking.
- **Copying competitor roadmap shape** without copying constraints: mismatched org capacity and distribution.
- **Confusing vision with plan**: vision motivates; strategy and roadmap allocate scarcity.
- **Single horizon overload**: too many “now” themes guarantees slow everything and weak learning.
- **Ignoring business model constraints**: great product roadmap that breaks unit economics; read `business-model/_overview.md` alongside product plans.
- **Skipping `roadmap.md` in repo**: duplicating or contradicting the canonical file the team already maintains.

## Questions to ask the user (pick 5–8)

1. What **planning horizon** and **review cadence** is this roadmap for?
2. Who is the **primary audience**, and what decision should this artifact drive?
3. What **stage** is the product in, and how confident are we in delivery dates for “now”?
4. What are the **non-goals** or segments we refuse to optimize for this period?
5. What **outcomes** (metrics) prove the current strategy is working?
6. What **hard dependencies** (legal, tech, partnerships) constrain sequence?
7. What **bets** must be validated before expanding “next” into “now”?
8. How should this connect to the **existing** `.productmap/00_company/product/roadmap.md` (replace, append, or fork by initiative)?

## Cross-references (paths)

- `.productmap/01_strategy/mvp-roadmap/_overview.md` — MVP discipline, sequencing, and learning-first cuts.
- `.productmap/01_strategy/business-model/_overview.md` — how value is created and captured; constraints on roadmap.
- `.productmap/01_strategy/segmentation/_overview.md` — who the roadmap serves and segment tradeoffs.
- `.productmap/00_company/product/roadmap.md` — current roadmap record in this knowledge base.
- `.productmap/09_templates/prd-template.md` — from committed bet to delivery spec.
- `.productmap/08_frameworks/` — reusable lenses (prioritization, JTBD, etc.) to stress-test themes and wording.

## Operating notes for the assistant

- Use **absolute dates** (`YYYY-MM-DD`) in filenames and headers when the user or repo conventions require dates.
- **Read before write**: prefer editing existing roadmap files if they are the agreed canonical location.
- Keep tone **direct PM**: short headings, concrete bullets, explicit tradeoffs, no filler.
- If repo sections are sparse, state gaps and offer minimal scaffolding rather than inventing company facts.
- When the user asks for “the roadmap,” confirm whether they mean **customer-facing commitments**, **internal engineering plan**, or **investor narrative**—same word, different risk profile.
- Prefer **linking** to `.productmap/08_frameworks/` entries over pasting long framework tutorials; your job is application, not textbook length.
- If multiple initiatives live under `.productmap/00_company/product/`, clarify which initiative folder receives new artifacts before writing files.
- When MVP scoping conflicts with sales promises, surface the conflict explicitly and propose **scope negotiation** artifacts (dates, tiering, phased value) rather than silently cutting engineering estimates.
- For “strategic narrative,” ensure the story answers: **why now**, **why us**, **why this sequence**—missing any leg leaves the narrative vulnerable in exec review.
- If the user mixes OKRs and roadmap, separate **outcome commitments** (OKRs) from **delivery intent** (roadmap) and show mapping; avoid duplicate sources of truth without links.
- After drafting, recommend a short **decision log** section in the roadmap file: dated decisions, owner, and what changed—future you will need it.

## Quality checklist (before you ship the answer)

- Strategy contains explicit **non-goals** or segment tradeoffs.
- Every “now” theme has an **outcome**, a **leading indicator**, and an **owner**.
- Dependencies across product, GTM, and org are visible or flagged as unknowns.
- Language matches **stage** (learning vs predictability); no false precision.
- Repo paths consulted are cited so the user can audit your reasoning.
- Next recommended artifact is clear (one-pager vs N/N/L vs outcome roadmap vs PRD).
