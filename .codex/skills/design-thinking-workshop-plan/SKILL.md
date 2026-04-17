# Design thinking workshop plan (plan + facilitate)

## Name

`design-thinking-workshop-plan` — Plan and facilitate a design thinking workshop (agenda, exercises, materials, facilitation tips, and output artifacts) for a specific product problem.

## When to use

- You need a structured, timeboxed workshop to align on a problem and generate/test solution directions.
- You’re kicking off discovery for a new initiative and need shared context + prioritized opportunities.
- You have too many ideas and need convergent decision-making (criteria, votes, RICE, next steps).
- You need a repeatable facilitation plan (roles, timing, prompts, risks, and follow-ups).

## Inputs

(Ask the user for these.)

- Workshop goal (1 sentence): problem definition, opportunity discovery, ideation, concept selection, experiment planning, or alignment
- Product / area + scope boundaries:
- Target users / segment(s) and key personas (if known):
- Current evidence (links/notes/metrics) + where it lives in repo (paths):
- Constraints (regions, compliance, technical, budget, timeline):
- Timebox:
  - Workshop date: `YYYY-MM-DD`
  - Duration (e.g. 90m / 2h / half-day / full-day)
  - Prep due by: `YYYY-MM-DD`
  - Follow-up due by: `YYYY-MM-DD`
- Participants:
  - Roles needed (PM, Design, Eng, Data, Sales/CS, Ops, Exec sponsor)
  - Count + seniority mix
  - Remote / in-person / hybrid + tools available (Zoom, Miro/FigJam, whiteboard)
- Decision needed:
  - What must be decided by end of workshop (and what explicitly will *not* be decided)?
- Output location preference (if writing back):
  - Initiative folder under `.productmap/00_company/product/...` (or provide a specific path)

## Outputs

- A complete facilitation plan (Markdown) including:
  - Pre-work checklist and reading pack
  - Agenda with minute-by-minute timing
  - Exercise instructions + prompts to read verbatim
  - Materials / templates list (links + what to prepare)
  - Facilitation tips (bias control, participation, conflict, timekeeping)
  - Roles (facilitator, scribe, decider, timekeeper) and responsibilities
- Workshop artifacts to produce (and suggested repo paths if writing back), typically:
  - Problem framing: context, goals, non-goals, constraints
  - Customer snapshot: proto-personas and/or key segments
  - Journey / workflow (current state) + pain points
  - “How might we” (HMW) opportunity list (clustered + named themes)
  - Idea set (sketches or concept one-pagers) + top concepts selected
  - Decision criteria + decision log
  - Experiment / next-steps backlog (owners + dates)

## Repo knowledge to pull

- Start here (navigation): `.productmap/index.md`
- Optional (meeting mechanics): `.productmap/07_tools/meetings.md`
- Optional (design collaboration norms): `.productmap/07_tools/design.md`
- Optional (deck/storytelling): `.productmap/07_tools/presentations.md`
- Optional (if you want to turn outcomes into follow-on artifacts):
  - Persona: `.productmap/09_templates/persona-template.md`
  - PRD: `.productmap/09_templates/prd-template.md`
  - Decision record (ADR): `.productmap/09_templates/adr-template.md`
  - Prioritization: `.productmap/08_frameworks/rice.md`
  - Problem framing lens: `.productmap/08_frameworks/jobs-to-be-done.md`

## Detailed prompt (copy/paste)

You are a senior product + design facilitator. Your job is to produce a **ready-to-run design thinking workshop plan** with a tight agenda, clear exercises, and explicit outputs.

Constraints:
- Use absolute dates `YYYY-MM-DD` everywhere.
- The plan must work for the given duration and format (remote/in-person/hybrid).
- Include facilitation details that reduce common failure modes (scope creep, HIPPO bias, silent participants, bikeshedding).
- Propose concrete output artifacts and (if asked) suggest repo storage locations under `.productmap/00_company/product/...`.
- Cite repo paths consulted (at minimum `.productmap/index.md`; optionally `.productmap/07_tools/meetings.md`, `.productmap/07_tools/design.md`, `.productmap/07_tools/presentations.md`, and any templates/frameworks used).

Inputs:
- Today: {{TODAY_YYYY-MM-DD}}
- Workshop date: {{WORKSHOP_YYYY-MM-DD}}
- Duration: {{DURATION}} (e.g. 90m, 2h, half-day, full-day)
- Format: {{FORMAT}} (remote / in-person / hybrid)
- Workshop goal: {{GOAL_1_SENTENCE}}
- Product/area + scope boundaries: {{SCOPE}}
- Target users/segments: {{USERS}}
- Evidence so far + repo paths: {{EVIDENCE_AND_PATHS}}
- Constraints: {{CONSTRAINTS}}
- Participants (names/roles if known): {{PARTICIPANTS}}
- Decider / decision rule (if any): {{DECIDER_AND_RULE}}
- Prep due by: {{PREP_DUE_YYYY-MM-DD}}
- Follow-up due by: {{FOLLOWUP_DUE_YYYY-MM-DD}}
- If writing back, artifact base path: {{ARTIFACT_BASE_PATH_OR_BLANK}}

Output (Markdown), in this order:
1) **Workshop snapshot**: goal, date, duration, format, desired decisions, anti-goals (3–7 bullets)
2) **Participant plan**:
   - Roles: facilitator, timekeeper, scribe, decider
   - Invite list guidance (who must be in the room vs optional)
3) **Pre-work (due {{PREP_DUE_YYYY-MM-DD}})**:
   - Reading pack (links + repo paths)
   - Pre-reads summary (2–6 bullets)
   - Async inputs to collect (e.g. pains, examples, screenshots, metrics)
4) **Agenda (minute-by-minute)**:
   - Include time, activity name, objective, and output
5) **Exercises (run instructions)**:
   For each exercise include: purpose, setup, prompt (verbatim), steps, timebox, outputs, facilitation tips, and common pitfalls.
6) **Materials & logistics**:
   - Tools, templates, room/AV needs, board setup, sticky-note conventions, naming scheme for artifacts
7) **Output artifacts**:
   - List each artifact with: description, owner, completion criteria, due date (`YYYY-MM-DD`), and (if provided) suggested repo path
8) **Risks & mitigations**:
   - At least 8 risks with prevention and in-the-room mitigations
9) **Follow-up plan (by {{FOLLOWUP_DUE_YYYY-MM-DD}})**:
   - Synthesis steps, decisions to confirm, communications plan, and next actions
10) **Repo paths consulted**

Also include two variants:
- **90-minute “compressed” version** (if the main plan is >90m)
- **Full-day version** (if the main plan is <4h)

## Workflow (runbook)

1. Pull repo context
   - Start at `.productmap/index.md`.
   - If helpful, reference `.productmap/07_tools/meetings.md`, `.productmap/07_tools/design.md`, `.productmap/07_tools/presentations.md`.
2. Confirm the workshop intent
   - Clarify: discovery vs ideation vs convergence vs experiment planning.
   - Define explicit decision(s) and anti-goals to avoid scope creep.
3. Choose a format + agenda shape (match timebox)
   - 90m: align → frame → HMW → quick ideation → vote → next steps.
   - 2–3h: add journey/pain mapping + concept one-pagers.
   - Half-day: add proto-personas + concept critique + experiment planning.
   - Full-day: add deeper current-state mapping + multiple concept rounds + prioritization (e.g. RICE).
4. Prepare exercises (recommended “design thinking” sequence)
   - **Frame**: context, goals, constraints, success signals
   - **Empathize**: proto-personas + “day-in-the-life” assumptions
   - **Define**: problem statement + key moments + HMWs (clustered)
   - **Ideate**: divergent generation (silent first), then share/merge
   - **Decide**: criteria + dot voting + decider call
   - **Plan**: experiments / next steps with owners and dates
5. Set facilitation controls
   - Start with silent writing to reduce anchoring.
   - Use timeboxes and parking-lot for out-of-scope items.
   - Use “1-2-4-All” or round-robin to balance voices.
   - Protect psychological safety; separate critique of ideas from people.
6. Define artifact outputs + storage
   - If asked to write back, store initiative artifacts under `.productmap/00_company/product/...`.
   - Store raw inputs (screenshots, exports, interview notes) under `.productmap/10_data/...`.
7. Produce the final workshop plan
   - Ensure agenda timing sums correctly to the duration.
   - Ensure every exercise produces a concrete artifact or decision.
   - Ensure all dates are `YYYY-MM-DD` and owners are named (or role placeholders).

## Quality checklist

- Agenda is executable in the stated duration and includes breaks (if >90m).
- Each exercise has: purpose, setup, verbatim prompt, steps, timebox, and explicit outputs.
- Convergence mechanics are defined (criteria + voting + decider rule) to avoid “endless ideation”.
- Includes facilitation tactics for common failure modes (HIPPO bias, quiet voices, bikeshedding, scope creep).
- Output artifacts are specific, have owners, completion criteria, and due dates (`YYYY-MM-DD`).
- References repo knowledge with clickable paths (at minimum `.productmap/index.md`; optional tools pages).
- Follow-up plan turns workshop outputs into next actions (decisions, experiments, PRD inputs).
