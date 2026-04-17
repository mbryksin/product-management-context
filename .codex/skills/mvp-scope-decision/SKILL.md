---
name: mvp-scope-decision
description: Define MVP goals and non-goals, release slices, de-risking experiments, and an ADR-style scope decision log using .productmap templates and data conventions.
---

# MVP Scope Decision & Slicing — Skill

## Name

`mvp-scope-decision` — Define MVP goals/non-goals, constraints, release slices, a de-risking plan, and an ADR-style decision log.

## When to use

- You need to scope an MVP (or “v1”) and avoid gold-plating.
- You need to slice a launch into sequential releases (alpha/beta/GA, regions, segments, channels).
- Stakeholders disagree on “must-have vs nice-to-have” and you need a crisp decision record.
- The team needs a de-risking plan (experiments/spikes) before committing to build.
- You’re about to write (or rewrite) a PRD and want a clear scope boundary first.

## Inputs (ask user for these)

- Initiative / product name:
- Artifact date label (YYYY-MM-DD) (use today’s date, e.g. `2026-04-17`, unless the user specifies otherwise):
- Target users / segment(s) + geography:
- Problem statement (1–2 sentences) + success definition (metrics/targets):
- Time constraints (deadline(s) in `YYYY-MM-DD` and any fixed events):
- Hard constraints (budget, headcount, tech/platform, security/compliance, legal, localization, accessibility):
- Known requirements / “musts” (if any) + “definitely not” items (if any):
- Dependencies (teams, vendors, APIs, data, approvals):
- Existing context to read first (repo paths, notes, prior PRDs/ADRs, research):
- Risk appetite + rollout preference (feature flags, phased rollout, beta cohort, region sequencing):

## Outputs

- MVP scope decision document (Markdown) containing:
  - Goals and Non-goals
  - Constraints and assumptions
  - Release slices (ordered) with acceptance criteria and “done means”
  - De-risking plan (spikes/experiments) mapped to top risks
  - Open questions and owners
  - ADR-style decision log (or references to ADR files)
- Suggested storage location (if writing back to the repo is desired):
  - Primary artifact: `.productmap/00_company/product/<initiative>/mvp-scope-decision-YYYY-MM-DD.md`
  - Decision records (ADRs): `.productmap/00_company/product/<initiative>/decisions/adr-YYYY-MM-DD-<slug>.md`
  - Raw inputs (if any): `.productmap/10_data/<initiative>/...`

## Repo knowledge to pull

- Start (repo-first navigation): `.productmap/index.md`
- Templates to anchor format:
  - PRD: `.productmap/09_templates/prd-template.md`
  - ADR: `.productmap/09_templates/adr-template.md`
- Optional (if present and relevant): adjacent frameworks/tools under `.productmap/08_frameworks/` and `.productmap/07_tools/`.

## Detailed prompt (copy/paste)

You are a product manager and delivery-focused strategy assistant. Create an **MVP Scope Decision & Slicing** document for the initiative below. Use **repo-first** context and cite which repo paths you used.

Repo-first context to consult:
- Start at: `.productmap/index.md`
- Use templates as anchors:
  - `.productmap/09_templates/prd-template.md`
  - `.productmap/09_templates/adr-template.md`
- Also read any user-provided repo paths (research, notes, prior PRDs/ADRs).

Constraints:
- Use **absolute dates** in `YYYY-MM-DD` (no “next week”, “Q3”, etc.).
- Do **not** invent facts; if something is unknown, record it as an assumption or open question.
- Prefer tight, testable statements and crisp acceptance criteria.
- Keep the scope boundary explicit: every “yes” should imply a “no” to something else.

Initiative context (user-provided):
- Initiative / product:
- Artifact date label (YYYY-MM-DD):
- Target users/segments + geography:
- Problem statement:
- Success metrics/targets:
- Deadline(s) and fixed events (YYYY-MM-DD):
- Hard constraints:
- Dependencies:
- Known must-haves:
- Known out-of-scope items:
- Rollout preference (flags/phases/regions/cohorts):
- Extra context + repo paths:

Steps:
1) Extract **Known facts** and **Unknowns** from the provided sources (bullets). Each bullet must end with a source citation like: `(source: .productmap/...)` or `(source: <user-provided path>)`.
2) Write **Goals** (3–7 bullets) and **Non-goals** (5–12 bullets). Non-goals must be concrete (what you will not build / not support in MVP).
3) List **Constraints & assumptions**:
   - Constraints (hard): budget/headcount, platforms, latency/scale targets (if any), security/compliance, regions, accessibility, data/privacy, integration limits.
   - Assumptions (testable): what must be true for MVP to succeed; include confidence (High/Medium/Low).
4) Define **Scope** as a single prioritized list of capabilities:
   - Use “capability” level, not implementation tasks.
   - For each item, include: `Why it matters`, `User value`, `Acceptance criteria`, and `Not included`.
5) Create **Release slices** (ordered, each shippable):
   - `Slice 0 (De-risk)` — minimal spikes/experiments/prototypes needed to answer top unknowns.
   - `Slice 1 (MVP)` — smallest external-value slice; define GA criteria.
   - `Slice 2 (MVP+)` and beyond — only if helpful; keep tight.
   For each slice include:
   - Target users/segment(s)
   - Rollout method (flags/cohorts/regions)
   - Included capabilities (from step 4)
   - Excluded capabilities (explicit)
   - Exit criteria (measurable) + target date (YYYY-MM-DD)
6) Build a **De-risking plan** table with columns:
   - `Risk / Unknown`
   - `Impact if wrong (High/Med/Low)`
   - `Evidence needed`
   - `Method (experiment/spike/interview/prototype/benchmark)`
   - `Owner`
   - `By date (YYYY-MM-DD)`
   Prioritize 5–10 items; call out the top 3 “make-or-break”.
7) Create an **ADR-style Decision Log**:
   - Identify 3–8 key decisions required to lock MVP scope/slices (e.g., “Which segment first?”, “Build vs buy?”, “What’s the initial platform support?”, “What’s the rollback plan?”).
   - For each decision, capture in ADR format aligned to `.productmap/09_templates/adr-template.md`:
     - `Title`, `Date (YYYY-MM-DD)`, `Status (Proposed/Accepted/Superseded)`,
     - `Context`, `Decision`, `Consequences`, and `Alternatives considered`.
   - If the user wants files written: propose ADR filenames like `adr-YYYY-MM-DD-<slug>.md` and reference them from the main document.
8) Close with **Open questions** (prioritized) and **Next actions (14–30 days)** mapped to risks/assumptions with owners and dates.

Output format (Markdown), in this exact order:
1. `Title: <Initiative> — MVP Scope Decision — YYYY-MM-DD`
2. `Context (facts + unknowns)`
3. `Goals`
4. `Non-goals`
5. `Constraints & assumptions`
6. `Scope (prioritized capabilities)`
7. `Release slices`
8. `De-risking plan`
9. `Decision log (ADR-style)`
10. `Open questions`
11. `Next actions (14–30 days)`
12. `Repo paths referenced`

## Workflow (runbook)

1. Confirm the inputs (initiative, date label `YYYY-MM-DD`, target users, success metrics, and deadline constraints).
2. Pull repo context:
   - Start at `.productmap/index.md` and follow links relevant to the initiative.
   - Use `.productmap/09_templates/prd-template.md` as the downstream handoff anchor (what will later become PRD-ready content).
   - Use `.productmap/09_templates/adr-template.md` to format decisions consistently.
3. Draft goals/non-goals first:
   - If you can’t write non-goals confidently, your scope isn’t bounded yet—loop back and clarify constraints.
4. Define capability-level scope with acceptance criteria:
   - Ensure each capability has a “not included” clause to prevent scope creep.
5. Slice the scope:
   - Each slice must be independently shippable and measurable.
   - Prefer smaller early slices that maximize learning and reduce irreversible commitments.
6. Create a de-risking plan:
   - Convert the top unknowns into time-boxed spikes/experiments with evidence criteria and dates.
7. Record decisions in ADR style:
   - Keep decisions few but high-leverage; avoid logging trivial choices.
8. (Optional) Write back to repo:
   - Save the main artifact to `.productmap/00_company/product/<initiative>/mvp-scope-decision-YYYY-MM-DD.md`.
   - Save each accepted decision as its own ADR under `.productmap/00_company/product/<initiative>/decisions/`.
9. Do a final quality pass using the checklist below.

## Quality checklist

- Goals are measurable and tied to user value (not internal tasks).
- Non-goals are concrete and prevent common scope creep (platforms, regions, edge cases, integrations, roles/permissions, analytics depth, etc.).
- Constraints are explicit and treated as binding; assumptions are labeled and testable.
- Scope is capability-level, prioritized, and each item has clear acceptance criteria and “not included”.
- Release slices are ordered, each is shippable, and each has explicit included/excluded scope + exit criteria + dates (`YYYY-MM-DD`).
- De-risking plan targets the top unknowns, defines what evidence “closes” each risk, and assigns owners + dates.
- Decision log uses ADR-style fields, includes alternatives, and explains consequences/tradeoffs.
- Open questions are prioritized and mapped to an owner and a by-date (`YYYY-MM-DD`).
- “Repo paths referenced” lists all sources consulted (starting with `.productmap/index.md`).
