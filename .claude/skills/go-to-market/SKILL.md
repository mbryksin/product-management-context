---
name: go-to-market
description: Use this skill when the user is planning or reviewing a go-to-market strategy, a product launch, a positioning exercise, or a channel strategy. Triggers — "GTM plan", "launch plan", "positioning", "messaging", "pricing strategy", "channel strategy", "PLG vs sales-led", "beachhead market", "launch tiering".
---

# Go-to-market (GTM) — Claude skill

Use this skill to structure **how** a product reaches buyers and users: positioning, messaging, pricing and packaging, segment focus, channel mix, motion choice (PLG, sales-led, and variants), and **launch execution** with tiering and measurement. Prefer **repo-first** reading from `.productmap/` before inventing frameworks.

## When this skill applies

- Planning or revising a **GTM strategy** for a new product, major release, new segment, or new geography.
- Choosing or reconciling **GTM motions** (product-led growth, sales-led, marketing-led, community-led, partner-led) and the operating model around them.
- Running a **positioning** or **messaging** exercise so sales, marketing, and product tell a coherent story.
- Designing **pricing and packaging** in service of acquisition, expansion, and channel economics.
- Picking a **beachhead** or **ICP** and mapping **buyers vs users** for campaigns and sales plays.
- Selecting **channels** under constraints (budget, brand, cycle time, compliance).
- Defining **launch tiers** (T1–T3), readiness gates, and cross-functional timelines.

## When not to use this skill (hand off instead)

- Pure **product discovery** without a near-term commercial path — pair with customer discovery and problem framing skills.
- **Deep technical delivery** planning (sprints, engineering capacity) — use agile-scrum-delivery or delivery overviews.
- **Financial modeling** as the primary goal (unit economics, LTV models) — pull unit economics overview; keep GTM linkage but do not substitute for finance rigor.
- **Legal-only** launches (compliance filings) where positioning is secondary — narrow scope.
- **Brand redesign** as aesthetics-led work without category or buyer strategy — still GTM-adjacent but may need design system or agency process first.

## Repo knowledge to consult first

Read before drafting artifacts:

- `.productmap/index.md`
- `.productmap/02_generation/marketing/_overview.md`
- `.productmap/02_generation/growth-sales/_overview.md`
- `.productmap/01_strategy/segmentation/_overview.md`
- `.productmap/01_strategy/product-market-fit/_overview.md`
- `.productmap/03_analysis/unit-economics/_overview.md`

**Related skill (PMF readiness):** When the debate is whether the product is **ready to scale** GTM spend, cross-check with `.claude/skills/product-market-fit/SKILL.md` if present in the repo, and always ground in `.productmap/01_strategy/product-market-fit/_overview.md`.

## GTM motions — definitions, fit, failure modes

### Product-led growth (PLG)

**Definition:** Users discover, activate, and expand with minimal human touch; product surfaces drive conversion, expansion, and referrals.

**Fit signals:** Short time-to-value, self-serve onboarding, clear activation metric, usage correlates with willingness to pay, low switching cost for trials.

**Failure modes:** Enterprise security or procurement blocks self-serve; complex integrations need services; sales feels “blocked” without PLG-qualified leads; vanity top-of-funnel with weak activation.

### Sales-led

**Definition:** Revenue motion centers on reps (inside, field, or hybrid) guiding evaluation, POC, and procurement.

**Fit signals:** High ACV, buying committee, RFP-heavy categories, need for bespoke demos, compliance narratives, multi-year contracts.

**Failure modes:** PLG-incompatible pricing on website confuses ICP; marketing generates MQLs sales rejects; long cycles without stage definitions; discounting hides weak differentiation.

### Marketing-led

**Definition:** Demand creation and capture through campaigns, content, events, and lifecycle programs; sales may still close but **marketing owns pipeline targets** for a slice of revenue.

**Fit signals:** Educated category, searchable pain, content can carry thought leadership, clear ICP for outbound ABM.

**Failure modes:** Message-market mismatch (traffic without ICP fit); attribution fights; over-investment before positioning clarity.

### Community-led

**Definition:** Practitioners, champions, and ecosystem (forums, meetups, OSS, advocates) drive trust, content, and referrals.

**Fit signals:** Highly engaged user persona, identity tied to craft, strong “share in public” culture, extensibility (plugins, APIs).

**Failure modes:** Community as support dumping ground; no path from enthusiast to buyer; under-resourced moderation; KPIs only on engagement not revenue support.

### Partner-led

**Definition:** Scale through agencies, resellers, marketplaces, cloud cosell, or technology integrations.

**Fit signals:** Partner accesses installed base you cannot reach; services attach rate high; regional or vertical coverage gaps.

**Failure modes:** Channel conflict; weak enablement; partners not incented on **your** differentiation; integration maintenance overload.

**Hybrid reality:** Most B2B companies blend motions. Name a **primary** motion for the next 2–4 quarters, explicit **secondary** motion, and **rules of engagement** (when sales assists PLG, when marketing hands off, partner registration).

## Positioning — April Dunford style (condensed)

Use this checklist so positioning is **comparative**, not slogan-only:

1. **Competitive alternatives:** What would customers do if you disappeared (incumbents, spreadsheets, hiring, “do nothing”)? Position against those, not a strawman.
2. **Unique attributes:** Capabilities or attributes competitors cannot credibly claim (evidence-backed).
3. **Value themes (capabilities → outcomes):** Translate attributes into 2–4 themes buyers care about (money, risk, speed, quality of life at work).
4. **Best-fit customers:** Characteristics of accounts and personas where your value spikes; include **negative fit** (who to say no to).
5. **Market category framing:** Pick a frame that **highlights strengths** without overpromising; consider **reframing** the category if incumbents own the default label.

Avoid “we’re the fastest easiest AI-powered platform for everyone.” Prefer bounded claims tied to ICP and proof.

## Messaging hierarchy

Build top-down so every asset aligns:

1. **Company / product narrative (1 paragraph):** Who it’s for, what problem, why now, why you win vs alternatives.
2. **Positioning statement (internal):** For [ICP], who [struggle], [product] is [category] that [key benefit], unlike [alternatives], we [differentiator proof].
3. **Value pillars (2–4):** Each pillar: headline, 2–3 proof points, required evidence (customer quote, metric, third-party).
4. **Use-case stories:** Situation, obstacle, outcome with metrics; map to segments.
5. **Objection handling:** Security, migration, pricing, competitor X — consistent answers for sales and CS.
6. **Channel variants:** Web one-liners, paid ad hooks, outbound sequences, partner one-pager — same pillars, different compression.

## Pricing and packaging (GTM lens)

- **Packaging:** Good-better-best vs usage vs seat vs hybrid; align packaging to **how value is perceived** in the buying center.
- **Price metric:** What scales with customer success (seats, MAU, events, revenue share) — affects land-and-expand and churn.
- **Sales friction:** Self-serve needs simple SKUs; enterprise may need private offers — avoid publishing noise that trains buyers to negotiate randomly.
- **Proof:** Pilot pricing, intro discounts, and annual prepay shape CAC payback — tie decisions to `.productmap/03_analysis/unit-economics/_overview.md` concepts.
- **Launch implications:** Price changes need internal enablement, external comms, contract amendment rules, and grandfathering policy.

## Segmentation, beachhead, ICP, buyer map

- **Segment:** Coherent group with similar buying motion, pains, and channels.
- **Beachhead:** The **first** segment you will win consecutively (sequencing), not “everyone mid-market.”
- **ICP:** Falsifiable firmographic, technographic, and behavioral bounds; disqualifiers explicit.
- **Buyer map:** Economic buyer, champion, user, blocker, IT/security — who needs which message and proof at which stage.
- **Handoff to execution:** ICP feeds ABM lists, product onboarding defaults, success plays, and roadmap prioritization.

Deep segmentation patterns: `.productmap/01_strategy/segmentation/_overview.md`.

## Bullseye channel thinking (practical)

1. **Brainstorm** all plausible traction channels (not only paid ads).
2. **Rank** by rough potential and cost for **your ICP** (not generic “LinkedIn works”).
3. **Shortlist** outer ring experiments; run cheap tests with clear success/fail metrics.
4. **Double down** on one **core** channel per motion when data supports it; protect focus.
5. **Revisit** quarterly — channels saturate; creative and offer fatigue are real.

## Launch tiering (example T1–T3)

Define tiers with **scope, risk, and ceremony** — adapt names to your org:

| Tier | Typical trigger | Cross-functional scope | Comms intensity | Examples |
|------|-----------------|-------------------------|-----------------|----------|
| **T1** | Company bet, category shift, major revenue lever | Full GTM + exec + CS + legal | External PR, events, sales kickoff | New product line, rebrand + reposition |
| **T2** | Important release, new packaging, meaningful segment | Core marketing + sales enablement + support macros | Blog, email, webinar, sales deck | Major feature with monetization |
| **T3** | Incremental improvement, narrow audience | Lightweight release notes, in-app, targeted comms | Low external blast | Bugfix batch, small UX |

For each launch: **audience**, **success metrics**, **rollback/feature flag plan**, **support readiness**, **anomaly monitoring** (conversion, latency, refunds).

## Workflow (runbook A–F)

**A. Frame the commercial context**

Confirm product maturity hypothesis, ICP draft, and “why now.” Pull PMF and segmentation overviews.

**B. Positioning sprint**

Alternatives, attributes, value themes, best-fit, category frame. Write internal positioning + pillars.

**C. Messaging + enablement**

Hierarchy down to channel snippets; build sales/partner deck outline and objection doc.

**D. Pricing and packaging decision**

SKU logic, metric, discount policy, migration for existing customers if any.

**E. Channel + motion plan**

Primary/secondary motion, Bullseye tests, 30–90-day priorities, owners, and budget bands.

**F. Launch execution**

Tier, timeline, comms calendar, readiness checklist, analytics and retro date.

## Pitfalls (common failure patterns)

1. **Launch without positioning:** Activity spikes, win rate does not; every team invents its own story.
2. **ICP “everyone”:** Channel spend spreads thin; product builds for conflicting needs.
3. **PLG theater:** Free signups without activation metric ownership and lifecycle triggers.
4. **Sales-marketing SLA vacuum:** MQL definitions drift; blame replaces pipeline math.
5. **Pricing changed midnight:** CS and finance surprised; churn and distrust spike.
6. **Partner-led without enablement:** Slide decks exist, partners cannot demo or answer security.
7. **T1 launch for T3 change:** Organizational fatigue; real T1s lose attention.
8. **No negative fit:** Bad customers consume support and distort roadmap.
9. **Message debt:** Website says X, product does Y, sales promises Z.
10. **Vanity metrics:** Impressions and meetings held without pipeline quality and win-rate follow-through.

## Questions to ask the user (starter set)

1. What is the **primary GTM motion** for the next two quarters, and what evidence supports that choice?
2. Who are the **top three competitive alternatives** from the buyer’s point of view?
3. What is the **beachhead ICP** in one sentence, and who is explicitly **out of scope**?
4. What is the **single activation or “aha” metric** that proves value in the first session or first week?
5. What **price metric and packaging** option are you testing, and what would falsify it?
6. Which **one channel** will get a disciplined experiment in the next 30 days, and what is the kill/scale rule?
7. What **launch tier** is this, and which teams must be in the war room vs async updates?
8. What **risks** (technical, legal, narrative) require rollback or staged rollout?
9. How will you measure **win rate, cycle time, expansion, and churn** for this ICP post-launch?
10. What **artifacts** must exist before sales or partners are unleashed (deck, demo script, security doc)?

## Artifact skeletons (Markdown-friendly)

**GTM one-pager**

- Context and date (`YYYY-MM-DD`)
- ICP / beachhead
- Motion(s) and rules of engagement
- Positioning summary + pillars
- Packaging / price stance (high level)
- Top channels + 30-day tests
- Launch tier + owners
- Metrics and review cadence

**Launch checklist (excerpt)**

- Product: feature flags, monitoring, rollback
- Enablement: deck, talk track, demo env, FAQs
- Marketing: comms plan, landing updates, nurture
- Sales: quotas impact, comp notes, CPQ/SKU updates
- CS: macros, health score impact, training
- Legal / security: external claims reviewed

**Channel experiment card**

- Hypothesis, ICP slice, creative/offer, sample size, duration, primary metric, guardrails, decision rule

## Storage conventions (repo)

- Initiative artifacts: `.productmap/00_company/product/<initiative>/`
- Raw interviews, launch retros, campaign results: `.productmap/10_data/<initiative>/`
- Date-stamp filenames with `YYYY-MM-DD`.

## Operating cadence (what “good” looks like after the doc)

GTM is not a one-time deck. Name a lightweight cadence so strategy turns into behavior:

- **Weekly:** Pipeline quality review (stage aging, win/loss themes, ICP fit of new opps), top channel experiment readout, product blockers affecting demos.
- **Monthly:** Messaging refresh based on objections heard in sales; win-rate and cycle-time by segment; content and campaign backlog reprioritized against ICP.
- **Quarterly:** Motion mix review (PLG vs sales assist vs partner), pricing and packaging experiment outcomes, segment sequencing (beachhead vs next wave), competitive map update.

Document **owners** for narrative (often PMM), pipeline targets (rev marketing / demand gen), enablement freshness (sales ops or enablement), and **single-threaded executive** for cross-functional tradeoffs on launch dates.

## Metrics map (connect tactics to outcomes)

Avoid measuring only top-of-funnel. Tie each motion to a **short ladder** of metrics:

- **PLG:** Visitor → signup → activation → habit use → paid conversion → expansion; instrument drop-offs by cohort and acquisition source.
- **Sales-led:** Meetings held → qualified opps → stage velocity → win rate → ASP → gross retention; segment metrics separately from “generic” pipeline.
- **Marketing-led:** Target account engagement → MQA/SQA (if used) → influenced pipeline → cost per qualified opp; keep definitions stable quarter to quarter.
- **Community-led:** Active contributors → advocate-generated pipeline (attributed) → time-to-answer for peer questions; watch support deflection vs community burnout.
- **Partner-led:** Active selling partners → registered deals → attach rate → partner-sourced revenue; track enablement completion as a leading indicator.

For launches, predefine **primary success metric** (e.g., paid conversion of trial, attach rate of add-on, win rate in ICP) and **guardrails** (latency, error rate, refund rate, NPS dip).

## Buyer journey touchpoints (planning grid)

For the beachhead ICP, sketch a simple matrix so messaging and assets line up:

- **Stages:** unaware → problem aware → solution aware → vendor shortlist → validation (POC) → procurement → onboarding → expansion.
- **Per stage:** buyer role(s), primary fear, proof required, asset type (blog, ROI calc, architecture doc, reference call), owner team, and **exit criterion** to next stage.

This grid becomes the backbone of a launch calendar and prevents “random acts of marketing.”

## Sales enablement bundle (minimum viable)

Before scaling outbound or inbound-to-sales handoff, confirm existence (even draft) of:

- **Talk track** aligned to value pillars (not feature dump).
- **Standard demo** with scripted “moments” tied to outcomes; known failure paths and recovery lines.
- **Discovery question bank** mapped to qualification criteria.
- **ROI / value framework** honest about inputs required; avoid fake precision.
- **Security story:** data flow, subprocessors, certifications status, roadmap for gaps.
- **Competitive battlecards** for top 2–3 alternatives with “when we lose” honesty.
- **Objection doc** with approved answers; legal review for risky claims.

## Positioning workshop facilitation (90–120 minutes)

Suggested flow when working live with stakeholders:

1. **Align on the goal:** “We are deciding how we want to be perceived by [ICP] vs [alternatives], not picking a tagline yet.”
2. **List alternatives** individually first, then merge (reduces groupthink).
3. **Silent sticky pass** on attributes (what we have others lack; what others have we lack) — force specificity.
4. **Cluster into value themes** — demand “so what” for each cluster until buyer language emerges.
5. **Define best-fit and negative-fit** with examples of customers you should have said no to.
6. **Category / frame debate** as a deliberate choice with tradeoffs, not a beauty contest.
7. **Homework:** Customer calls to validate language; competitive mystery shop; update positioning doc by `YYYY-MM-DD`.

Capture disagreements as **testable hypotheses** (e.g., “economic buyer is CFO” → validate with next five late-stage deals).

## Launch RACI (starter)

Roles vary by company size; adapt titles:

- **Driver (D):** Launch manager or PMM — runs timeline, standups, risks.
- **Accountable (A):** Product director or GM — makes scope and date tradeoffs.
- **Consulted (C):** Legal, security comms, finance (comp/discount), exec comms for T1.
- **Informed (I):** Broad org via changelog or town hall segment.

For T3, RACI can collapse to PM + engineer + support lead; still write it down to avoid “silent no.”

## Partner GTM addendum

If partner-led is material:

- **Tier partners** (strategic vs transactional) with different enablement depth.
- **Deal registration** rules and conflict policy published early.
- **MDF or incentives** only after messaging and demo certification milestones — paying for noise wastes budget.
- **Integration roadmap** honesty: each major integration is an ongoing product surface, not a checkbox.

## International and regulated nuance (checklist)

- Claims, subsidies, healthcare, finance, or public sector: **localize** both language and proof; involve legal early for T1.
- **Data residency** and **AI training** policies: often gating in enterprise; do not launch enterprise GTM without explicit answers in security FAQ.
- **Pricing in currency** and tax/VAT display for self-serve — operational mistakes erode trust faster than weak copy.

## Artifact: competitive battlecard skeleton

- Alternative name and positioning (how they describe themselves)
- Where they win (be honest)
- Where we win (with proof types)
- Landmines to avoid (feature debates they want)
- Landmines to set (proof points that expose their gaps for our ICP)
- **Trap questions** for discovery that surface fit
- Disqualify guidance: when to walk away or partner instead

## Artifact: 30–60–90 plan outline

- **First 30 days:** Positioning lock (good enough), ICP list v1, channel experiments launched, enablement v1 shipped, analytics events verified.
- **Days 31–60:** Kill/scale decisions on channels, first pricing/packaging readout, refine messaging from field feedback, case study or reference path started.
- **Days 61–90:** Motion tuning (e.g., sales-assist rules), partner pilot if applicable, next segment hypothesis or geographic wave.

## Quality bar before you ship recommendations

- Positioning is **comparative** and tied to **best-fit** customers.
- Motion choice implies **org design** (roles, systems, metrics) — you named those implications.
- Pricing advice acknowledges **unit economics** and existing customer fairness.
- Launch tier matches **actual risk**; comms volume matches tier.
- Every strong claim has an **evidence** path or is labeled **assumption** with a test.
- Cross-links to overviews are **used**, not decorative.

## Codex companion

For a Codex-oriented runbook and copy-paste prompt block, use `.codex/skills/go-to-market/SKILL.md`.
