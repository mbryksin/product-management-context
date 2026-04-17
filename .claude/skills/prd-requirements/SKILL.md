---
name: prd-requirements
description: Use this skill when the user is writing, reviewing, or scoping a PRD, spec, user story, or requirements document — including AI-feature specs and acceptance criteria. Triggers: "write a PRD", "draft a spec", "user story", "acceptance criteria", "scope this feature", "review my spec", "AI feature spec", "tech spec vs PRD".
---

# PRD and requirements

## When this skill applies

Use this skill when the user is **writing, revising, reviewing, or decomposing** product requirements — from a **one-pager** to a **full PRD**, from **user stories** and **acceptance criteria** to **technical specifications** and **ADRs**, including **AI/ML-assisted features** where evaluation, failure modes, and operational constraints matter.

Typical triggers: **write a PRD**, **draft a spec**, **user story**, **acceptance criteria**, **scope this feature**, **review my spec**, **AI feature spec**, **tech spec vs PRD**, **non-functional requirements**, **rollout plan**, **experiment spec**.

## When this skill does not apply

- **Pure discovery** with no intent to ship a defined change (use discovery/research framing first; you may still produce a “discovery brief,” not a PRD).
- **Architecture-only decisions** with no user-visible behavior (prefer an **ADR**; link it from the PRD if the feature triggers it).
- **Marketing copy** or **brand narrative** without acceptance-ready behavior (different artifact).
- **Bug fixes** that are one-line behavior changes (a ticket + test may suffice unless risk/compliance demands a fuller spec).

## Document types (use templates; do not duplicate them here)

Pick the lightest artifact that still **de-risks delivery and alignment**. The canonical structures live in the repo:

- **One-pager / short spec**: start from `.productmap/09_templates/prd-template.md` and collapse sections intentionally (still cover risks and success criteria).
- **Full PRD**: `.productmap/09_templates/prd-template.md` (follow its headings and level of rigor).
- **User story + acceptance criteria**: `.productmap/09_templates/user-story-template.md`.
- **AI / ML feature PRD**: `.productmap/09_templates/ai-prd-template.md` (adds evaluation, monitoring, and failure-mode rigor).
- **ADR (architecture decision record)**: `.productmap/09_templates/adr-template.md` when the decision is a **durable technical fork** with trade-offs.
- **Tech spec / implementation spec**: often a companion doc; should reference the PRD’s **what/why** while owning **how** (interfaces, data models, migration, performance budgets). Avoid duplicating product narrative verbatim; **link** and summarize.

If the user is unsure which type to use, recommend a **default path**:

1) Problem + outcome one-pager → 2) PRD or AI PRD → 3) stories + AC → 4) ADRs as needed.

## Anatomy of a strong PRD (product-facing)

These are **outcomes**, not a mandate to use every heading on every feature.

### Problem and context

- **Who** is impacted (segment, persona, internal role) and **why now** (trigger, urgency, compliance deadline).
- **Evidence** pointers (research links, tickets, metrics) rather than unattributed claims.

### Goals and non-goals

- **Goals** are measurable or at least **observable** (“reduce time to X by …” or “enable Y workflow end-to-end”).
- **Non-goals** prevent scope creep and clarify what you are **not** fixing in this iteration.

### User scenarios and scope

- Primary flows, edge cases, **permissions**, and **empty states**.
- **Internationalization**, accessibility expectations, and platform constraints if relevant.

### Functional requirements

- Requirements are **testable** (“system must …”) and avoid solution dictation unless constrained.

### Non-functional requirements (NFRs)

- Performance, reliability, security/privacy, auditability, data retention, supportability, and cost ceilings (especially for AI).

### Analytics and success metrics

- **Primary metric** + **guardrails** (what must not regress).
- Event naming or analytics tickets, if your org separates that workstream.

### Rollout, migration, and risk

- Feature flags, phased rollout, backwards compatibility, comms plan, rollback triggers.

### Open questions and decisions

- Explicit owners and **decision due dates** (`YYYY-MM-DD`).

## User stories: INVEST and acceptance criteria

### INVEST (quick quality bar)

- **Independent**: deliverable without hard-tangling every other story (or document dependencies).
- **Negotiable**: story states outcome; not a frozen UI spec unless required.
- **Valuable**: ties to user/business value.
- **Estimable**: enough clarity for sizing; spikes called out.
- **Small**: fits iteration cadence.
- **Testable**: AC can be verified.

### Acceptance criteria shapes

Use **Given / When / Then** when behavior branching is clearer in scenario form:

- **Given** a precondition and context
- **When** the user or system action occurs
- **Then** expected observable results (including errors, telemetry, side effects)

For data-heavy features, include **fixtures** or example records in the ticket appendix (or link to `.productmap/10_data/`).

## AI feature PRDs: what changes

AI specs fail in predictable ways; the AI PRD template exists to force the right conversations. In addition to normal PRD sections, emphasize:

### Outcomes over model details

Start from the **user-visible behavior** and **quality bar**, not the model name. Model choice belongs in design notes once requirements are clear.

### Evaluation design

- **Offline metrics** (accuracy proxies, human rubric, golden sets) vs **online metrics** (task success, latency, cost).
- **Representative test sets** and **red-team / abuse** cases for user-facing generation.

### Failure modes and degraded behavior

- Hallucination, omission, toxicity, bias, tool misuse, unsafe recommendations.
- **Fallback UX**: human review, refusal templates, retrieval grounding, deterministic mode.

### Prompting and determinism (where applicable)

- Whether prompts are **versioned** like code, who owns changes, and how you detect **silent drift** from upstream model updates.
- Logging policy for prompts/outputs (PII constraints).

### Cost and performance envelopes

- Token budgets, caching, batching, rate limits, worst-case latency targets.

### Monitoring and incident response

- Dashboards, alerts, kill switches, rollback to prior prompt/model versions.

### Human-in-the-loop and compliance

- Domains with legal exposure (medical/financial/legal): extra scrutiny, disclaimers, audit trails.

## Workflow (runbook)

a) **Clarify the decision**: PRD vs one-pager vs tech spec vs ADR; pick the template(s) from `.productmap/09_templates/`.

b) **Pull repo context**: read `.productmap/04_delivery/backlog-requirements/_overview.md` and the chosen template end-to-end before drafting.

c) **Draft for alignment first**: problem, goals/non-goals, scope boundaries, risks—then details.

d) **Make requirements testable**: rewrite vague phrases into AC and measurable metrics.

e) **Run the review checklist** (below); fix high-severity gaps before slicing stories.

f) **Slice for delivery**: vertical increments, dependencies, feature flag plan, analytics tasks.

## Review checklist (use as a gate before “ready for eng”)

1. **Problem statement** names a real user and a concrete pain; not only an internal task.
2. **Goals** include at least one **measurable** or **observable** success signal; guardrails listed.
3. **Non-goals** exist and are specific enough to prevent scope creep.
4. **Primary user flows** cover happy path + critical error/empty states.
5. **Permissions / roles** are explicit (or explicitly “same as today”).
6. **Data model implications** called out (new fields, migrations, PII classification).
7. **NFRs** include performance, reliability, security/privacy as applicable.
8. **Analytics** defines what to learn and what must not regress.
9. **Rollout** includes risk controls (flag, phased rollout, rollback triggers).
10. **Dependencies** on other teams/services are listed with owners.
11. **Open questions** have owners and decision dates (`YYYY-MM-DD`).
12. **Acceptance criteria** are testable and aligned to stories (no orphan AC).
13. **AI features** include evaluation, failure modes, monitoring, cost envelope (if AI applies).
14. **Out of scope** experiments are captured as follow-ups, not hidden scope.
15. **Repo references** cite templates used and any supporting data paths under `.productmap/10_data/`.

## Pitfalls (common spec failures)

1. **Solution-first writing** that skips the user outcome (“build Kafka…”) without a requirement trace.
2. **Ambiguous adjectives** (“fast,” “easy,” “smart”) without measurable thresholds.
3. **Implied scope** buried in comments or Slack threads, not in the doc body.
4. **Analytics as an afterthought**, making success unmeasurable post-launch.
5. **Missing negative cases** (offline mode, timeouts, partial permissions, corrupt input).
6. **Mismatched granularity**: PRD duplicates every implementation detail (belongs in tech spec) or tech spec re-litigates product strategy (belongs in PRD).
7. **AI features** without evaluation sets and failure-mode UX (over-trust in model correctness).
8. **Acceptance criteria** that assert implementation (“uses library X”) instead of behavior.
9. **Migration** assumed to be trivial; data backfill and dual-write periods undocumented.
10. **Compliance** discovered late because PII flows were not mapped.

## Questions to ask the user (if missing)

1. **Who** is the primary user and what is their **job-to-be-done** in this flow?
2. What **outcome** must be true for this to be a success (metric or observable)?
3. What is explicitly **out of scope** for this release?
4. What are the **hardest edge cases** you already know about?
5. What **platforms** and **roles** are in scope?
6. What **deadlines or compliance** constraints exist?
7. What **data** is created, read, updated, deleted (including PII)?
8. How will we **roll out** and **roll back**?

## Artifacts (suggested outputs)

- **PRD** or **one-pager** (Markdown) aligned to `.productmap/09_templates/prd-template.md`.
- **Story list** with **INVEST** sizing notes and dependencies.
- **AC appendix** using Given/When/Then for high-risk flows.
- **AI addendum** using `.productmap/09_templates/ai-prd-template.md` sections when ML/generation is involved.
- **ADR** for major technical forks, linked from the PRD.

Suggested storage (if writing to the repo):

- Initiative artifacts: `.productmap/00_company/product/<initiative>/prd-<feature>-YYYY-MM-DD.md`
- Raw research/interviews: `.productmap/10_data/<initiative>/...`

Use **absolute dates** (`YYYY-MM-DD`) in filenames and decision logs.

## PRD vs tech spec: division of labor (practical)

- **PRD** owns **why**, **what**, and **acceptance** from a product perspective (users, outcomes, scope, metrics, rollout).
- **Tech spec** owns **how** to implement safely: APIs, schemas, algorithms, performance plan, test plan, migration, observability hooks.
- **ADR** owns **decision record** for forks with long-lived consequences.

Cross-link documents; do not fork two sources of truth for the same requirement.

## Story slicing patterns (short guidance)

- Prefer **vertical slices** that deliver user value each increment.
- Separate **foundational** work only when it truly blocks everything; otherwise keep slices end-to-end thin.
- If a story is “too big,” split by **user outcome**, not by layer (unless risk forces a spike).

## Non-functional requirements prompts (starter set)

- **Performance**: p95 latency targets, payload sizes, cold start constraints.
- **Reliability**: SLO/SLA, retries, idempotency keys, deduplication.
- **Security**: authn/z, threat model notes, secrets handling, audit logs.
- **Privacy**: data minimization, retention, deletion, consent, regional constraints.
- **Cost**: infra budget, per-request model cost caps for AI features.

## Stakeholder alignment tips (keep specs usable)

- Put **decisions** adjacent to **trade-offs** (“we chose A over B because…”).
- Keep the **first page** readable by busy executives: problem, outcome, risks, timeline.
- Use appendices for long tables, API examples, and research dumps.

## Repo cross-references (read before drafting)

Templates and delivery context:

- `.productmap/09_templates/prd-template.md`
- `.productmap/09_templates/user-story-template.md`
- `.productmap/09_templates/ai-prd-template.md`
- `.productmap/09_templates/adr-template.md`
- `.productmap/04_delivery/backlog-requirements/_overview.md`
- Navigation index: `.productmap/index.md`

If template guidance conflicts with stakeholder requests, **surface the conflict explicitly** and propose options with trade-offs.

## Quality bar (definition of “ready for review”)

A spec is “ready for review” when a competent engineer can:

- Explain the **user outcome** without guessing.
- Identify **scope boundaries** and **non-goals**.
- Draft a **test plan outline** from the AC.
- Spot **major risks** (data, security, performance, AI evaluation) without inventing them from thin air.

If those are not true, the document is still a **draft**: label it as such and list missing inputs.

## Optional appendix patterns (use when helpful)

### Risk table (lightweight)

Columns: `Risk`, `Likelihood`, `Impact`, `Mitigation`, `Detectability`, `Owner`, `By date (YYYY-MM-DD)`.

### Decision log snippet

Bullets of `Decision`, `Rationale`, `Date`, `Approver` — especially useful across revisions.

### “Test notes” section

Links to QA environments, feature flag keys, seed accounts, and example payloads.

## Handoff to engineering (minimum package)

- PRD (or one-pager) + linked ADRs
- Story list with AC
- Analytics events list (or ticket IDs)
- Rollout plan + rollback triggers
- Open questions with due dates and owners

## Handoff to design (minimum package)

- User flows + states (empty/loading/error)
- Content requirements and constraints (legal, tone)
- Accessibility expectations (keyboard, focus, contrast targets if your org defines them)

## Traceability (requirements → delivery)

Strong specs make downstream work obvious:

- Map **PRD sections** to **epics/stories** explicitly when ambiguity is high.
- For regulated domains, map requirements to **controls** (who attests, what evidence is produced).
- For experiments, map hypotheses to **instrumentation** and **decision thresholds** before launch.

If your toolchain supports it, prefer **single identifiers** (ticket keys) for cross-linking rather duplicating paragraphs across systems.

## Cross-functional ticket prompts (what often gets forgotten)

Even if tickets live outside the repo, the PRD should **name** the workstreams:

- **Design**: flows, states, component scope, content needs.
- **Analytics**: event schema, dashboards, experiment readouts.
- **Legal/Trust**: disclosures, consent, data processing agreements if new processing occurs.
- **Support/Success**: help articles, macros, internal talking points for known sharp edges.
- **Sales** (if applicable): packaging changes, pricing impacts, demo scripts.

Skipping these does not remove the work; it just moves it to launch week chaos.

## Continuous revision rules

- When scope changes, update **goals/non-goals** and **AC** in the same edit pass.
- When learning arrives from beta, append a short **“What changed”** section dated `YYYY-MM-DD` rather than silently rewriting history without traceability.

## Glossary discipline (avoid semantic drift)

Define terms on first use in the PRD body, especially:

- **Customer**, **account**, **workspace**, **seat** (if your product uses multiple layers).
- **Active** (logged in? used core action? paid?).
- **Admin** vs **member** capabilities.
- **Beta**, **GA**, and **internal-only** scopes.

Keep the glossary short (5–12 terms). Long glossaries belong in a product lexicon doc, linked once.

## Conflicts and precedence (when stakeholders disagree)

When product, design, legal, and engineering constraints conflict, document:

- **Options** (A/B/C), **trade-offs**, **recommendation**, and **decision owner**.
- The **default** if no decision arrives by the due date (usually safest/lowest-risk path).

This prevents “silent decisions” made only in implementation.

## Where AI assistance helps (and where it hurts)

- **Helps**: turning rough notes into structured sections, generating AC permutations, finding ambiguous wording, drafting test ideas.
- **Hurts**: inventing users, metrics, compliance constraints, or “industry standard” numbers without sources.

If the model proposes facts, mark them **UNVERIFIED** unless the user confirms or repo data supports them.
