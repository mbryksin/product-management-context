# Business Model Canvas (BMC) — Skill

## Name

`business-model-canvas` — Draft a Business Model Canvas (or equivalent) plus assumptions, risks, and open questions.

## When to use

- You need a fast, shared understanding of how a product/business creates, delivers, and captures value.
- You’re exploring a new product/initiative, a pivot, a new segment, or a new channel/pricing model.
- You want to surface the biggest unknowns (assumptions) and turn them into testable questions.
- You’re aligning stakeholders before writing a PRD, roadmap, or deck.

## Inputs (ask user for these)

- Initiative / product name:
- Date to label the artifact (YYYY-MM-DD) (use today’s date, e.g. `2026-04-17`, unless the user specifies otherwise):
- Stage (idea / discovery / MVP / growth / mature):
- Target customer segments (who specifically, and where):
- Context (links + repo paths to read first):
- Current strategy / constraints (budget, timeline, regions, tech, legal/compliance):
- “Equivalent canvas” preference (pick one):
  - Business Model Canvas (standard 9 blocks)
  - Lean Canvas (problem/solution centric)
  - Mission Model Canvas (if public sector / non-profit)
- Known pricing / packaging (if any):
- Known competitors / alternatives (including “do nothing”):
- Any hard requirements (non-negotiables):

## Outputs

- A draft canvas + registers in Markdown:
  - Canvas blocks (BMC or equivalent)
  - Assumptions register (testable, with confidence + impact)
  - Risks (derived from assumptions, with mitigations + leading indicators)
  - Open questions (what to learn next)
  - Suggested next steps (discovery, experiments, stakeholder reviews)
- Suggested storage location (if writing back to the repo is desired):
  - Primary artifact: `.productmap/00_company/product/<initiative>/business-model-canvas-YYYY-MM-DD.md`
  - Supporting raw inputs (if any): `.productmap/10_data/<initiative>/...`

## Repo knowledge to pull

- Start here (repo-first navigation): `.productmap/index.md`
- Strategy/testing approach (if populated): `.productmap/07_tools/strategy-ci.md`
- Useful adjacent templates (optional, if relevant):
  - Personas: `.productmap/09_templates/persona-template.md`
  - PRD (to transition after alignment): `.productmap/09_templates/prd-template.md`
  - Exec/board narrative: `.productmap/09_templates/board-deck-template.md`
- Frameworks that may help wording/structure (optional, if populated):
  - `.productmap/08_frameworks/jobs-to-be-done.md`
  - `.productmap/08_frameworks/other-frameworks.md`

## Detailed prompt (copy/paste into Codex/ChatGPT)

You are a product strategy assistant. Draft a **Business Model Canvas (or the specified equivalent)** for the initiative described below, and include an **assumptions register**, **risks**, and **open questions**. Use **repo-first** context and cite which repo paths you used.

Constraints:
- Use **absolute dates** in `YYYY-MM-DD`.
- Prefer concrete nouns, numbers, and falsifiable statements; avoid vague wording.
- If info is missing, do not invent facts—write them as assumptions or open questions.

Repo-first context to consult:
- Start at: `.productmap/index.md`
- Also read (if relevant/available): `.productmap/07_tools/strategy-ci.md`, plus any user-provided repo paths.

Initiative context (user-provided):
- Initiative / product:
- Date label (YYYY-MM-DD):
- Stage:
- Preferred canvas type (BMC / Lean / Mission):
- Target segments:
- Constraints:
- Pricing/packaging notes:
- Competitors/alternatives:
- Extra context + repo paths:

Steps:
1) Summarize the **known facts** (bullet list) and **unknowns** (bullet list) from the provided context (include repo path citations like: `(source: .productmap/...)`).
2) Produce the canvas using the chosen format:
   - If **Business Model Canvas**, fill the 9 blocks:
     - Customer Segments
     - Value Propositions
     - Channels
     - Customer Relationships
     - Revenue Streams
     - Key Resources
     - Key Activities
     - Key Partners
     - Cost Structure
   - If **Lean Canvas**, fill:
     - Problem, Customer Segments, Unique Value Proposition, Solution, Channels,
       Revenue Streams, Cost Structure, Key Metrics, Unfair Advantage
   - If **Mission Model Canvas**, adapt blocks to mission outcomes, beneficiaries,
     and mission-specific value exchange (but keep sections parallel and clear).
3) Create an **Assumptions Register** table with columns:
   - `Assumption`
   - `Why we believe this (evidence or reasoning)`
   - `Confidence (High/Medium/Low)`
   - `Impact if wrong (High/Medium/Low)`
   - `How to test / what evidence would change our mind`
   - `Owner`
   - `By date (YYYY-MM-DD)`
   Include at least 10 assumptions; flag the top 3 “make-or-break”.
4) Derive a **Risks** table (not duplicates of assumptions) with columns:
   - `Risk`
   - `Type (market/product/tech/ops/legal/competitive)`
   - `Trigger / leading indicator`
   - `Mitigation`
   - `Owner`
   - `By date (YYYY-MM-DD)`
5) List **Open Questions** (prioritized) that should be answered next to de-risk the model.
6) Add **Next Steps (14–30 days)**:
   - 3–7 concrete actions, each mapped to an assumption/risk and an output artifact.
   - If `.productmap/07_tools/strategy-ci.md` is available, express each step as a hypothesis + test + metric (Strategy CI style).

Output format (Markdown):
- Title: `<Initiative> — <Canvas Type> — YYYY-MM-DD`
- Sections in this exact order:
  1. `Context (facts + unknowns)`
  2. `Canvas`
  3. `Assumptions Register`
  4. `Risks`
  5. `Open Questions`
  6. `Next Steps (14–30 days)`
  7. `Repo paths referenced`

## Workflow (runbook)

1. Confirm scope: initiative name, canvas type, and the artifact date (`YYYY-MM-DD`).
2. Pull repo context:
   - Start at `.productmap/index.md`, then follow links relevant to the initiative.
   - Read any user-provided repo paths (docs, notes, prior strategy).
3. Draft the canvas:
   - Keep blocks tight (5–10 bullets each) and consistent (segments ↔ channels ↔ revenue).
4. Convert ambiguity into explicit assumptions:
   - Write them as falsifiable statements, then attach tests and due dates.
5. Derive risks + open questions:
   - Make risks actionable (triggers + mitigations), and questions answerable.
6. Recommend next steps:
   - Prioritize the top 3 “make-or-break” assumptions and propose fast validation.
7. (Optional) Write back to the repo:
   - Save to `.productmap/00_company/product/<initiative>/business-model-canvas-YYYY-MM-DD.md`.
   - Store raw inputs under `.productmap/10_data/<initiative>/...`.

## Quality checklist

- Canvas coherence: segments, value prop, channels, and revenue model align (no mismatches).
- Specificity: includes numbers or bounded ranges where possible (pricing, CAC drivers, costs, volumes).
- Completeness: all blocks are filled; no block is “TBD” without being captured as an assumption/question.
- Assumptions are testable: each has a clear falsification method and a due date (`YYYY-MM-DD`).
- Top risks are actionable: each has a trigger/indicator and a mitigation plan.
- Open questions are prioritized and directly reduce uncertainty in the model.
- Next steps map back to assumptions/risks and produce concrete outputs.
- “Repo paths referenced” lists all repo sources consulted (starting with `.productmap/index.md`).
