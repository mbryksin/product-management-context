---
name: agile-scrum-delivery
description: Use this skill when the user is running, troubleshooting, or improving a delivery process — Scrum ceremonies, Kanban flow, sprint planning, estimation, retrospectives, scaling frameworks. Triggers — "sprint planning", "backlog grooming", "retro", "standup", "Scrum vs Kanban", "story points", "velocity", "WIP limit", "SAFe", "LeSS", "scaling agile".
---

# Agile, Scrum, and delivery — Claude skill

Use this skill when the goal is to **ship predictably and learn fast** through team process: Scrum ceremonies, Kanban flow, backlog health, estimation debates, retrospectives, and **scaling** conversations. Ground advice in the repo’s delivery overviews and templates before inventing a bespoke methodology.

## When this skill applies

- Designing, auditing, or fixing **Scrum** or **Kanban** (or hybrid) at team level.
- Facilitating or improving **sprint planning**, **backlog refinement**, **standups**, **reviews**, **retrospectives**.
- Resolving **estimation** arguments (story points, ideal days, throughput, or no estimates).
- Interpreting **flow metrics** (cycle time, lead time, WIP, CFD) and turning them into experiments.
- **Team-of-teams** delivery pain: dependencies, release trains, portfolio pressure — including when someone names **SAFe**, **LeSS**, **Scrum@Scale**, or **Spotify model**.

## When not to use this skill (redirect)

- **GTM, positioning, pricing** — use go-to-market skill and marketing overviews.
- **Pure strategy / OKR** setting without delivery mechanics — strategy overviews and OKR frameworks.
- **HR performance management** disguised as agile — that is people leadership, not ceremony design.
- **Tool-only** questions (“which Jira plugin”) when the issue is **workflow policy** — still in scope, but do not let the tool drive the answer.
- **Incident response / SRE** runbooks — adjacent but distinct; mention handoffs only.

## Repo knowledge to consult first

- `.productmap/index.md`
- `.productmap/04_delivery/agile-process/_overview.md`
- `.productmap/04_delivery/backlog-requirements/_overview.md`
- `.productmap/04_delivery/lean-experiments/_overview.md`
- `.productmap/04_delivery/development/_overview.md`
- `.productmap/09_templates/retrospective-template.md`
- `.productmap/09_templates/user-story-template.md`

Use **user-story-template** when the user’s problem is poorly sliced work disguised as “agile doesn’t work.”

## Agile Manifesto — condensed for practitioners

Values (left **over** right, not “instead of”):

- **Individuals and interactions** over processes and tools.
- **Working software** over comprehensive documentation.
- **Customer collaboration** over contract negotiation.
- **Responding to change** over following a plan.

Principles in short: deliver frequently; welcome changing requirements; business and developers work together daily; motivated individuals with trust and support; face-to-face conversation; working software is the primary measure of progress; sustainable pace; technical excellence and good design enhance agility; simplicity; self-organizing teams; regular reflection and tuning.

**Translation for teams:** cadence + transparency + working increments + continuous improvement. Anything that kills those four needs a skeptical look.

## Scrum — roles, accountabilities, ceremonies

### Roles (2020+ Scrum Guide spirit)

- **Product Owner:** maximizes product value from the backlog; accountable for **ordering** and clarity of items; one voice to the team on “what next.”
- **Scrum Master:** accountable for **Scrum effectiveness**; coaches, removes impediments **the team cannot remove alone**, fosters empirical process.
- **Developers:** accountable for creating the **Increment** each Sprint; quality, breakdown of work, adaptation within Sprint.

Anti-patterns:

- **PO as backlog secretary** for many stakeholders with no ordering authority.
- **SM as project admin** tracking tasks instead of improving system of work.
- **“Tech lead decides everything”** collapsing developer accountability into a single bottleneck.

### Ceremonies (events)

- **Sprint Planning:** why this Sprint matters (goal), what can be done, how work will be done (plan, not micro-spec every hour).
- **Daily Scrum:** inspect progress toward Sprint Goal; adapt plan for next 24 hours — **not** a status report to a manager only.
- **Sprint Review:** inspect Increment and **progress toward product goal**; collaborate with stakeholders on what’s next.
- **Sprint Retrospective:** inspect **how** the team worked; agree improvements that land next Sprint.

Anti-patterns:

- Planning without a **Sprint Goal** → busy work pile.
- Daily that is **round-robin to boss** → hides real blockers.
- Review as **demo theater** with no feedback captured or backlog impact.
- Retro that never produces **owned** actions with dates — learned helplessness.

### Artifacts (short)

- **Product Backlog** ordered, emergent, DEEP (see below).
- **Sprint Backlog** plan for Sprint.
- **Increment** meets Definition of Done — potentially releasable (even if business chooses not to release).

## Kanban — core ideas and metrics

Kanban emphasizes **visualize work**, **limit WIP**, **manage flow**, make policies explicit, implement feedback loops, improve collaboratively.

**Lead time** (customer request to delivery) vs **cycle time** (active working time once started) — define entry/exit points consistently on the board.

**Cumulative Flow Diagram (CFD):** thickness of bands shows WIP by stage; sudden widening suggests a bottleneck; narrowing may mean starvation upstream.

**Throughput:** items completed per week — useful when item sizes are reasonably homogeneous or when you track **T-shirt** classes instead of points.

Anti-patterns:

- Board that **lies** (states don’t match reality).
- No WIP limits → everything started, nothing finished.
- “Kanban” with **no policies** for ready/done per column.

## Scrum vs Kanban vs hybrid — decision tree

1. **Do you need a regular commitment boundary** for stakeholders (we ship/review every N days)? Strong yes → **Scrum** cadence often fits.
2. **Is arrival of work highly variable** (support tickets, ops, interrupt-driven)? Strong yes → **Kanban** flow often fits.
3. **Do you have both project milestones and interrupt stream?** Consider **ScrumBan**: Scrum cadence for product increments + explicit **capacity for classes of service** (expedite rules, fixed slack).
4. **Is quality/debt burning velocity?** Fix **Definition of Done** and technical practices before arguing framework.
5. **Is the real problem portfolio thrash?** No framework saves you without **WIP limits at leadership level** on concurrent initiatives.

State clearly: hybrid is fine; **policy clarity** beats purity.

## Estimation — story points, ideal time, throughput, #NoEstimates

**Story points (relative sizing):** compare effort/risk/uncertainty within a team; useful for **conversation**, dangerous as **productivity KPI** vs other teams.

**Ideal hours / days:** can work for skilled stable teams with well-known work; often gamified; management misuse risk.

**Throughput + slicing:** count small similarly-sized stories; invest in **thin vertical slices**; forecast by Monte Carlo or simple trailing windows — works well with mature backlog hygiene.

**#NoEstimates:** still **decompose** and order; replace estimation meetings with **splitting until pieces feel small** and use historical cycle time; not “no thinking.”

Guidance:

- Never use points as **individual performance** measure.
- If estimates never improve predictability, **inspect why** (ambiguous stories, dependency hell, unstable teams) before changing scale.

## Product backlog — DEEP

- **Detailed appropriately:** near-term items crisp; far-term items coarse.
- **Emergent:** discovery updates the backlog continuously.
- **Estimated** (if you estimate) at the granularity useful for ordering and forecasting — or use sizing classes.
- **Prioritized / ordered:** one ordered list; politics handled explicitly, not hidden.

Healthy backlog connects to **product outcome**, not only output.

## Retrospectives — structure, formats, template pointer

**Basic structure (45–75 minutes):**

1. **Set stage** — safety reminder, focus theme, working agreements.
2. **Gather data** — timeline, metrics snapshot, anonymized examples.
3. **Generate insights** — patterns, root causes (Five Whys sparingly and carefully).
4. **Decide experiments** — 1–3 actions, owners, dates, how you’ll know it worked.
5. **Close** — appreciation, review of retro on retros quarterly.

**Formats (rotate):**

- **Start / Stop / Continue** — fast; shallow if overused.
- **4Ls** (Liked, Learned, Lacked, Longed for) — good for release postmortem tone.
- **Lean Coffee** — emergent agenda; good when team feels scripted.
- **Sailboat** (wind, anchors, rocks, island) — surfaces risks and enablers visually.
- **Metrics-based** — start from CFD, escaped defects, lead time regressions; keeps retro factual.

**Facilitation tips:**

- Prefer **specific incidents** over character attacks.
- Capture **system** causes (handoffs, unclear ownership, missing tests) over blaming individuals.
- If the same issue recurs three retros, escalate as **organizational impediment**, not “team attitude.”

**Repo template:** `.productmap/09_templates/retrospective-template.md` — align headings if you produce a retro doc for the repo.

## Scaling frameworks — honest lens

**SAFe (Scaled Agile Framework):** heavy coordination for large enterprises; can improve dependency visibility; risks bureaucracy, role inflation, and **local optimization** if leadership treats it as compliance theater. Use when multiple trains must align on cadence and **portfolio WIP** is acknowledged as a lever.

**LeSS (Large-Scale Scrum):** fewer prescribed roles; emphasizes **whole-product focus** and Scrum at scale with minimal addition. Fit when org can tolerate **real** PO/product structure changes; still hard politically.

**Scrum@Scale:** meta-Scrum coordinating multiple Scrum teams; lighter than SAFe but needs **strong executive discipline** on priorities.

**“Spotify model” (squads/tribes/chapters/guilds):** widely misunderstood as a reorg sticker; original context included **culture and autonomy** investments copying the labels rarely copies outcomes.

**Truthful advice:** scaling fixes **thin** problems if **team-level Scrum/Kanban** is already healthy. Otherwise you scale dysfunction. Start with **dependency mapping**, **definition of ready/done**, **integration cadence**, and **single prioritized backlog** at product level where possible.

## Workflow — diagnose then experiment

1. **Qualify the pain:** predictability, quality, speed to market, morale, stakeholder trust — which is primary?
2. **Visualize:** board, release history, incident trend, lead time scatterplot if available.
3. **Hypothesize system cause:** WIP, unclear goals, weak slicing, external thrash, tech debt, missing test automation, approval chains.
4. **Pick one experiment** for 2–3 Sprints max (e.g., stricter DoR, WIP limit of 2 per dev, mob on critical defect class).
5. **Measure:** cycle time, defect rate, Sprint Goal hit rate, stakeholder satisfaction in review.
6. **Retro the experiment:** adopt, adapt, abandon — document learning in team working agreements.

## Pitfalls (common failure patterns)

1. **Velocity as a target:** incentivizes inflated points or unsafe shortcuts.
2. **Refinement starvation:** planning meetings become specification marathons.
3. **Done means “merged to main” but not releasable** — fake agility.
4. **Cross-team dependencies unmanaged** — every Sprint is heroics.
5. **Retro actions without owners** — ritual without change.
6. **Manager-only daily** — developers go quiet; real blockers move to Slack DMs.
7. **Kanban without limits** — busy appearance, little throughput improvement.
8. **Framework installation over principles** — coaches leave, old habits return instantly.
9. **Ignoring workflow for “more story points”** — optimizing the wrong curve.
10. **Scaling before team-level stability** — expensive program overhead, same slips.

## Questions to ask the user (starter set)

1. What is the **Sprint / iteration length**, and what **policy** exists for changing scope mid-Sprint?
2. What is your **Definition of Done** today, and who signs that it is enforced?
3. What is the **top recurring impediment** class (dependencies, clarity, tech debt, approvals, environment access)?
4. How do you measure **predictability** (Sprint Goal met rate, cycle time, release frequency)?
5. What **WIP limits** exist, if any, and what happens when someone breaks them?
6. Who truly **orders** the backlog, and how do stakeholder conflicts get resolved?
7. What happened in the **last three retros** — which actions completed, which died?
8. For scaling pain: is the bottleneck **architecture**, **product portfolio**, or **governance**?
9. How **thin** are typical stories (hours to days vs weeks), and what is an example of “too fat”?
10. What **template** do stories follow — does it match `.productmap/09_templates/user-story-template.md`?

## Artifacts you can produce with this skill

- **Team working agreement** (1 page): core hours, async norms, refinement rules, escalation path.
- **Definition of Ready / Done** refresh with acceptance checklist tied to quality risks.
- **Retro record** aligned to `.productmap/09_templates/retrospective-template.md` with experiments.
- **Flow metrics dashboard spec** (what to plot weekly, thresholds for action).
- **Scaling assessment memo:** what to try before adopting a heavy framework.

## Storage conventions (repo)

- Initiative-specific delivery notes: `.productmap/00_company/product/<initiative>/`
- Broader research or assessments: `.productmap/10_data/<initiative>/`
- Use `YYYY-MM-DD` in filenames when capturing dated retros or assessments.

## Story quality quick pass (when delivery is “slow”)

Before blaming capacity, inspect a sample of stories against the user-story template:

- User value stated; acceptance criteria testable; edge cases noted; dependencies called out; non-functional expectations (performance, security) explicit if relevant.

## Executive interface (short)

When leadership asks for “more roadmap certainty,” separate:

- **Forecast** (probabilistic, depends on WIP and historical throughput).
- **Commitment** (what we will optimize for this quarter).
- **Cadence** (when we review and reprioritize).

Misaligned expectations between those three create most “agile failed” narratives.

## Dependencies and integration (team-of-teams)

Practices that often help before buying scaling:

- **Scrum of Scrums** or equivalent **dependency forum** with explicit RACI on cross-team items.
- **Integration increment** at least as often as review — branches are not increments.
- **Architectural runway** as backlog items, not side folklore.

## Sprint Planning — agenda pattern (two-part spirit)

Even if you combine into one session, keep two mental passes:

**Part 1 — “What could matter this Sprint?”**

- PO presents **candidate goal** tied to outcome (not only ticket list).
- Team asks clarifying questions until shared understanding of **why** exists.
- Team selects **forecast** using historical throughput / velocity band — honest about holidays and on-call.

**Part 2 — “How will we build it?”**

- Decompose selected items into **day-sized** (or smaller) tasks if useful for your team; avoid hour-by-hour Gantt fantasy.
- Surface **dependencies and risks** early; spike or negotiate scope same day if possible.
- Confirm **Sprint Goal** in one sentence everyone can repeat.

Exit criteria: everyone knows **goal**, **first risky item** to pull, and **how we’ll demo** partial value if full scope slips.

## Backlog refinement (grooming) — healthy rhythm

- Aim to keep **next 1–2 Sprints** of work “ready enough” — not the entire roadmap at equal fidelity.
- Use **timebox** per item; if an item burns the whole session, it was not ready for refinement — split or spike.
- Capture **open questions** on the story; do not pretend unknowns vanished.
- Rotate **facilitation** so PO is not the only voice speaking.

Signals refinement is broken: only tech details, no user value; no PO; endless solution debates without decision timer.

## Daily Scrum — patterns that work

- Walk the **board right-to-left** (closest to done first) to finish work before starting.
- Explicit **blocker protocol**: who owns external chase, by when, next update channel.
- Keep **15 minutes**; deeper dives **park** with the right subset after.

If dailies feel useless, measure whether **Sprint Goal** was coherent — often the root issue is upstream.

## Sprint Review — stakeholder checklist

- Show **working** product on realistic data where possible.
- Capture **feedback** as backlog items with priority hint — not vague promises.
- Review **what changed in the market** since last review (competitors, incidents, regulation) briefly — connects delivery to reality.

Anti-pattern: only happy-path demo while known defects exist in the same area — erodes trust.

## Velocity and forecasting — use without harm

- Treat velocity as **team-local** signal for capacity planning, not a leaderboard.
- Prefer **range forecasts** (“we’ll likely finish between X and Y items this Sprint based on last 8 Sprints”) over false precision.
- If team composition changes materially, **reset** baseline rather than pretending continuity.

## Definition of Done — expand beyond “tests pass”

Consider explicit bullets appropriate to your domain:

- Code reviewed and merged; CI green; feature flagged if gradual rollout.
- **Observability:** metrics/logs/alerts updated for new paths.
- **Docs:** user-facing help or API docs updated.
- **Security / privacy:** threat surface reviewed for this change class.
- **Rollback** path understood for risky releases.

Done should match what **your org** means by releasable — negotiate with DevOps, security, and support.

## Technical practices that make agile “real”

- **Trunk-based** or short-lived branches with small PRs reduce integration risk.
- **Automated tests** at appropriate levels; manual-only regression cannot scale.
- **Pairing or mobbing** selectively on complex or high-risk areas — knowledge spread lowers WIP hidden queues.

## Flow debt vs feature debt

Teams track feature backlog but ignore **flow debt**: missing environments, flaky builds, slow reviews, unclear ownership. Dedicate **capacity** each Sprint to burn flow debt or cycle time will not improve.

## Multi-team dependency types (name them)

- **Technical:** shared library, schema, API contract.
- **Sequential:** team B cannot start until team A ships X — flag as schedule risk, not “we’ll figure it out.”
- **Organizational:** approvals, legal, procurement — need SLA or escalation owner same as technical blockers.

## When support / interrupt work shares the team

- Use **triage role** rotation so interrupt load is visible.
- Separate **classes of service** on the board (standard vs expedite) with strict expedite rules (one at a time, who can invoke).
- Capacity plan: reserve **explicit %** for sustainment or incidents — hidden tax kills forecasts.

## Quality bar for your advice

- Recommendations tie to **observed symptoms** and **metrics**, not ideology.
- Ceremonies each have a **clear purpose**; you did not add meetings without subtracting.
- Estimation guidance avoids **toxic misuse** and names tradeoffs.
- Scaling advice is **proportionate** to org maturity.
- You cited **repo paths** the user should open, including retro and story templates.

## Codex companion

For a Codex-oriented runbook and copy-paste prompt block, use `.codex/skills/agile-scrum-delivery/SKILL.md`.
