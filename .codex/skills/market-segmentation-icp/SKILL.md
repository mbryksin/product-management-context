# Market Segmentation + ICP (Segment Matrix + Persona)

## Name
Market Segmentation + ICP (Segment Matrix + Persona Draft)

## When to use
- You need a clear set of market segments with crisp boundaries (who is in / out).
- You need an Ideal Customer Profile (ICP) to focus roadmap, messaging, pricing, and GTM.
- You need a comparable **segment matrix** (scores + rationale) to pick a target segment.
- You need a first-pass **persona draft** for the top segment (aligned to the repo’s persona template).

## Inputs
- Product snapshot: what it does, target user, key outcomes, primary use cases.
- Current customer evidence (if any): wins/losses, pipeline notes, support tickets, sales calls, onboarding notes.
- Market constraints: geos, regulated industries, price band, deployment model, security/compliance requirements.
- Differentiators: top 3–5 reasons you win; top 3–5 reasons you lose.
- GTM reality: channel(s), sales motion (PLG/self-serve/sales-led), ACV range, expected sales cycle.
- “As-of” date in `YYYY-MM-DD` (use today’s date).

## Outputs
- Segment definitions (3–8) with inclusion/exclusion rules and examples.
- ICP definition for the chosen primary segment (must be falsifiable and testable).
- Segment matrix (table) with consistent criteria, scores, and rationale per segment.
- Persona draft for the ICP-aligned persona, following `.productmap/09_templates/persona-template.md`.
- Assumptions + open questions list (tagged `ASSUMPTION` / `QUESTION`) with next-step validation plan.

## Repo knowledge to pull
- Start from the knowledge base entrypoint: `.productmap/index.md`.
- Use the repo’s persona structure as the output shape: `.productmap/09_templates/persona-template.md`.
- Optional lens for capturing “why they hire the product” (jobs, triggers, desired outcomes):
  `.productmap/08_frameworks/jobs-to-be-done.md`.
- If you’re storing artifacts, follow repo conventions (initiative artifacts under `.productmap/00_company/product/`,
  raw inputs under `.productmap/10_data/`), and date-stamp files with `YYYY-MM-DD`.

## Detailed prompt (copy/paste)
Use this prompt with the repo as context.

---
You are a product strategist. Define market segments and an Ideal Customer Profile (ICP), then produce:
1) segment definitions, 2) a segment matrix, and 3) a persona draft.

Constraints:
- Use absolute dates `YYYY-MM-DD` for anything date-like.
- Be explicit about assumptions vs evidence. Tag lines with `EVIDENCE`, `ASSUMPTION`, or `QUESTION`.
- Prefer crisp, testable criteria (avoid vague “mid-market” without numeric thresholds).
- Align the persona format to `.productmap/09_templates/persona-template.md`.
- Optionally use `.productmap/08_frameworks/jobs-to-be-done.md` to express the core “job” and success metrics.

Inputs (fill in):
- As-of date: YYYY-MM-DD
- Product: <one sentence>
- Primary use cases: <bullets>
- Current customers / leads (if any): <summary + notable examples>
- Price / packaging constraints: <if known>
- Deployment/security constraints: <if any>
- GTM motion: <PLG/self-serve/sales-led/partner; channels>
- Differentiators: <bullets>
- Main competitors / alternatives: <bullets>

Tasks:
A) Segments (3–8):
   - Name each segment.
   - Define inclusion/exclusion rules (firmographic, technographic, behavioral, “situation”).
   - Give 2–3 example companies/orgs per segment (or “archetypes” if company names aren’t appropriate).
   - List primary pains and desired outcomes.
   - Note key constraints (budget, compliance, integrations, buying committee).

B) ICP (pick one primary segment; optionally one secondary):
   - Write an ICP definition with numeric ranges where possible (e.g., employee count, ARR, team size, budget).
   - State the “must have” conditions and “deal-breakers”.
   - Describe the buying trigger(s), the internal champion, and the economic buyer.
   - Provide a short “disqualify fast” checklist (5–10 items).

C) Segment matrix:
   - Create a table with rows = segments and columns = criteria.
   - Use a 1–5 score per criterion, plus a weighted total (define weights).
   - Minimum criteria: Pain intensity, Willingness to pay, Ability to reach, Competitive intensity,
     Sales cycle complexity, Retention/expansion potential, Strategic fit.
   - For each segment, include 1–3 bullets of rationale referencing `EVIDENCE` or `ASSUMPTION`.
   - Recommend the target segment(s) and explain tradeoffs.

D) Persona draft (for the primary ICP):
   - Draft a persona that matches `.productmap/09_templates/persona-template.md`.
   - Include goals, context, pains, buying triggers, objections, and success metrics.
   - Add “JTBD” phrasing if helpful (see `.productmap/08_frameworks/jobs-to-be-done.md`).

E) Validation plan:
   - List the top 10 uncertainties as `QUESTION`.
   - For each, propose the fastest validation method (customer calls, CRM pull, landing test, etc.)
     and what “pass/fail” evidence looks like.

Output format:
1) Segments
2) ICP
3) Segment matrix
4) Persona draft
5) Assumptions / questions / validation plan
---

## Workflow (runbook)
1) Pull repo context: open `.productmap/index.md`, then the persona template at `.productmap/09_templates/persona-template.md`.
2) Collect inputs: paste a tight product snapshot + any customer evidence; set `As-of date` in `YYYY-MM-DD`.
3) Draft segments:
   - Start with 5–7 candidate segments; merge/split until each is mutually exclusive *enough* to act on.
   - Add inclusion/exclusion rules so someone else can sort accounts into segments consistently.
4) Choose an ICP:
   - Define “must-have” + “deal-breakers”.
   - Add numeric thresholds wherever possible (team size, toolchain, compliance, budget).
5) Build the segment matrix:
   - Lock criteria + weights first.
   - Score consistently; capture rationale per row; show totals and ranking.
6) Draft the persona:
   - Use `.productmap/09_templates/persona-template.md` as the structure.
   - Keep it actionable: triggers, objections, buying committee, success metrics.
7) Add validation:
   - Convert key unknowns into `QUESTION`s with a concrete test and pass/fail evidence.
8) (Optional) Store artifacts:
   - Put the deliverable under `.productmap/00_company/product/<initiative>/` as `YYYY-MM-DD-segmentation-icp.md`.
   - Put raw inputs under `.productmap/10_data/<initiative>/` with the same date prefix.

## Quality checklist
- Segments are distinct and usable (clear inclusion/exclusion; not just “SMB / Mid-market / Enterprise”).
- ICP includes numeric thresholds and deal-breakers; a salesperson could disqualify quickly.
- Segment matrix criteria are defined, weighted, and applied consistently; totals match the narrative recommendation.
- Persona draft follows `.productmap/09_templates/persona-template.md` and is tied to the ICP.
- Every major claim is tagged `EVIDENCE` or `ASSUMPTION`; open unknowns are explicitly `QUESTION`.
- All dates are in `YYYY-MM-DD`.

