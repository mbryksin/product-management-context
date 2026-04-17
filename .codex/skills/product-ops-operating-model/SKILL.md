# Product Ops Operating Model (Lightweight rituals, cadences, artifacts, RACI)

## Name

`product-ops-operating-model` — Define a lightweight product operating model (rituals, cadences, artifacts, RACI, comms, decision forums, rollout plan)

## When to use

- You need to clarify **how product work runs** (planning → discovery → delivery → launch → learning) across PM/Eng/Design/Data/GT M.
- The team is scaling (new squads, new leaders, more stakeholders) and execution is getting noisy or slow.
- Decisions feel ambiguous (who decides, which forum, what inputs are required, what “done” means).
- Meetings feel heavy but outcomes are unclear; you want a **minimal set of high-leverage rituals**.
- You need a repeatable cadence for **roadmap/OKRs**, **initiative intake**, **status comms**, and **post-ship learning**.
- You’re setting up (or rebooting) a **Product Ops** function and need a starter operating model + rollout plan.

## Inputs

Ask the user for:

- Scope:
  - Product area(s) / portfolio:
  - Teams in scope (squads, functions):
  - In/out of scope explicitly:
- Organization context:
  - Company stage (seed/growth/enterprise or equivalent):
  - Team size (PM/Eng/Design/Data/GT M):
  - Time zones / working hours constraints:
  - Delivery model (platform vs product lines; squads vs functional):
- Goals & pain points:
  - Top 3 operating problems to fix:
  - Desired outcomes (speed, quality, alignment, predictability, autonomy, compliance):
  - Success metrics (leading + lagging):
- Decision and governance needs:
  - Decision types that need a forum (prioritization, resourcing, exceptions, scope changes, launches):
  - Risk/compliance constraints (security, regulatory, brand, legal):
  - Current escalation paths (if any):
- Current rituals and artifacts:
  - Existing meeting list + cadence:
  - Current artifacts (PRD/briefs, roadmap, OKRs, ADRs, release notes, dashboards):
  - Tools (Jira/Linear, Notion/Confluence, Slack/Teams, email, BI):
- Dates (absolute):
  - As-of date for the operating model (YYYY-MM-DD):
  - Rollout start date (YYYY-MM-DD):
  - Rollout target “steady state” date (YYYY-MM-DD):
- Repo context to read (paths):
  - Any existing team process docs, templates, or examples in this repo:

If an as-of date is not provided, use the run date and write it explicitly (example: `2026-04-17`).

## Outputs

Produce a Markdown “Lightweight Product Operating Model” that includes:

- Scope, principles, and non-goals
- Rituals & cadences (calendar of forums + purpose + inputs/outputs + attendees + owners)
- Standard artifacts (what they are, when used, who owns, where they live)
- RACI (or RAPID/DACI if requested) for key recurring activities and decisions
- Comms model (channels, audiences, frequency, update templates)
- Decision forums (charters: decision rights, membership, quorum, pre-reads, decision log)
- Rollout plan (phased, with dates, training, migration steps, adoption metrics)
- “How to use this” quickstart + links to repo templates used

If the user asks you to write it back into the repo, suggest a path under:
- `.productmap/00_company/product/<area>/operating-model-YYYY-MM-DD.md`

## Repo knowledge to pull

Start here:
- `.productmap/index.md` (knowledge base entrypoint and navigation)

Optionally consult (if present / useful):
- `.productmap/07_tools/project-management.md`
- `.productmap/07_tools/meetings.md`
- `.productmap/07_tools/writing-documents.md`

Common templates to reuse (adapt, don’t reinvent):
- `.productmap/09_templates/prd-template.md` (PRD / initiative spec)
- `.productmap/09_templates/okr-template.md` (goal-setting cadence)
- `.productmap/09_templates/adr-template.md` (decision log for technical/product decisions)
- `.productmap/09_templates/retrospective-template.md` (learning cadence)
- `.productmap/09_templates/one-on-one-template.md` (manager/IC and cross-functional 1:1s)

Frameworks (only if helpful for prioritization / governance):
- `.productmap/08_frameworks/okrs.md`
- `.productmap/08_frameworks/rice.md`
- `.productmap/08_frameworks/other-frameworks.md`

## Detailed prompt (copy/paste)

You are a **Product Operations lead**. Create a **lightweight Product Operating Model** for the org described below.

Hard constraints:
- Use **absolute dates only** (`YYYY-MM-DD`). No relative dates.
- Keep it **lightweight**: prefer the minimum set of rituals and artifacts that still achieves the goals.
- Be explicit about **decision rights** (who decides, in which forum, based on what inputs).
- Use only the user’s provided info and the repository files you read; label assumptions clearly.
- Include a “Sources” section listing the **repo file paths read** (clickable paths).

Inputs (fill from user):
- Product area(s) / portfolio:
- Teams in scope:
- Company stage and team size:
- Time zones / working hours constraints:
- Current tools (Jira/Linear, docs, chat, BI):
- Current rituals (list):
- Current artifacts (list):
- Top 3 operating problems to fix:
- Desired outcomes:
- Compliance / risk constraints:
- Decision types needing governance:
- As-of date (YYYY-MM-DD):
- Rollout start date (YYYY-MM-DD):
- Steady-state target date (YYYY-MM-DD):
- Repo paths to read (existing process docs, templates, examples):

Steps:
1. Read `.productmap/index.md`, then read the user-provided repo paths. Optionally read `.productmap/07_tools/project-management.md`, `.productmap/07_tools/meetings.md`, `.productmap/07_tools/writing-documents.md`.
2. State scope + operating principles (3–7) and non-goals (2–5) aligned to the user’s pains/outcomes.
3. Propose the smallest set of **rituals/forums** needed. For each, define: purpose, decision type(s), cadence, duration, owner, attendees, required pre-reads, outputs, and where outputs are stored.
4. Standardize a small set of **artifacts** (reusing repo templates where possible). Define: owner, when created/updated, required sections, and storage location.
5. Create a **RACI** for recurring cross-functional activities and decisions (at minimum: goal-setting/OKRs, intake/triage, prioritization, roadmap changes, scope change control, launch readiness, incident/quality exceptions, post-ship learning, stakeholder comms).
6. Define **comms**: audiences, channels, frequency, update format, and who writes/sends. Include a lightweight “weekly product update” and “monthly roadmap update” template.
7. Define **decision forums**: charter(s), membership, quorum, escalation, and a decision log approach (recommend using ADR-style entries where appropriate).
8. Create a **rollout plan** from rollout start → steady-state target date:
   - Phases (Pilot → Expand → Standardize)
   - Training (who, when, what materials)
   - Migration plan for existing meetings/artifacts
   - Adoption metrics and checkpoints with dates
   - Risks and mitigations
9. End with “Open questions” (5–12) that would materially change the operating model.

Output format (Markdown):
- Title: Product Operating Model — <Org/Product Area> — As of <YYYY-MM-DD>
- 1. Executive summary (7–12 bullets)
- 2. Scope, principles, non-goals
- 3. Rituals & cadences
  - A table with columns:
    - Forum / ritual
    - Purpose
    - Decisions made (or “none”)
    - Cadence
    - Duration
    - Owner
    - Required pre-reads
    - Outputs (artifacts) + storage path
    - Attendees (required/optional)
- 4. Standard artifacts
  - Table with columns:
    - Artifact
    - When used
    - Owner
    - Template (repo path if used)
    - Storage location (repo path pattern)
    - Quality bar (definition of “good enough”)
- 5. RACI
  - Matrix: rows = activities/decisions; columns = roles (PM, Eng, Design, Data, Product Ops, Sales, CS, Marketing, Legal/Sec as relevant)
- 6. Comms model
  - Audiences + channels + cadence
  - Templates (short, copy/paste)
- 7. Decision forums (charters)
  - For each forum: remit, inputs, decision rights, quorum, escalation, decision log
- 8. Rollout plan (dated)
  - Timeline with milestones from <rollout start> to <steady-state target>
- 9. Risks & mitigations
- 10. Sources (repo paths read)
- 11. Open questions

## Workflow (runbook)

1. Confirm **scope** (teams, decisions, time zones) and collect the required **dates** (`YYYY-MM-DD`).
2. Read `.productmap/index.md`, then read any existing process docs the user provides; optionally consult the tool pages under `.productmap/07_tools/`.
3. Inventory current rituals/artifacts and map them to desired outcomes; identify what to **keep, change, remove**.
4. Draft the operating model starting with **decision forums** and **rituals**, then standardize artifacts around the smallest set of templates.
5. Draft the RACI last to ensure it matches the proposed rituals and artifacts (avoid “paper RACI” that contradicts reality).
6. Review with key roles (PM lead, Eng lead, Design lead, Product Ops sponsor) and incorporate only changes that reduce ambiguity or remove toil.
7. Produce a rollout plan with dated milestones (pilot first), adoption metrics, and a migration plan for old meetings/docs.
8. If writing back to the repo is requested, save under `.productmap/00_company/product/<area>/operating-model-YYYY-MM-DD.md`.

## Quality checklist

- Uses only absolute dates (`YYYY-MM-DD`) and includes an explicit **as-of date**.
- Rituals are **minimal** and each has clear outputs; no “meeting for meeting’s sake”.
- Every key decision type has:
  - a named forum (or explicit async process),
  - required inputs/pre-reads,
  - a decision owner,
  - and a decision log mechanism.
- Artifacts are concrete, reusable, and mapped to existing repo templates where possible.
- RACI is unambiguous (single “A” per row) and matches the rituals/decision rights.
- Comms plan distinguishes **exec/stakeholder** updates vs **team execution** updates, with templates.
- Rollout plan includes: pilot scope, training, migration steps, adoption metrics, and dated checkpoints.
- Assumptions are labeled; unknowns become explicit “Open questions”.
- Includes a “Sources” section listing repo file paths read.
