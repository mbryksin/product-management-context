# Customer development hypotheses (vague idea → testable hypotheses)

## Name

`customer-development-hypotheses` — Turn a vague product idea into testable customer-development hypotheses (problem, user, value prop), prioritize riskiest assumptions, and produce a concrete test plan.

## When to use

- You have an early / vague product idea and need to make it falsifiable.
- You need to align a team on *what we’re betting* and *how we’ll learn*.
- You need a risk-ranked assumption list and a timeboxed learning plan.
- You want customer-development outputs **without** generating interview scripts or question lists.

## Inputs (ask user for these)

- Product / idea (1–3 sentences):
- Target user / segment (who, role, company type, maturity):
- Context & constraints (region, compliance, pricing constraints, channels):
- Current alternatives (what users do today):
- Evidence so far (links, notes, metrics, anecdotes) and confidence level:
- Time horizon (use absolute dates `YYYY-MM-DD`), e.g. start `2026-04-20`, decision by `2026-05-15`:
- Output preference:
  - Hypotheses only, or hypotheses + test plan, or hypotheses + test plan + artifacts location (repo path)

## Outputs

- A hypothesis set covering:
  - Problem hypotheses (pain, frequency, trigger, context)
  - User hypotheses (who, segmentation, constraints, buying center)
  - Value proposition hypotheses (promise, mechanism, differentiation)
- A ranked list of **riskiest assumptions** (impact × uncertainty) with rationale
- A **test plan** (timeboxed) mapping assumptions → tests → success/failure signals → decision gates
- Optional: recommended place to store the artifact under `.productmap/00_company/product/...` (only if user asks to write back)

## Repo knowledge to pull

- Start here: `.productmap/index.md`
- Optional framework to structure “who/what/why”:
  - `.productmap/08_frameworks/jobs-to-be-done.md`
- Optional tools to plan evidence capture + synthesis:
  - `.productmap/07_tools/research-analysis.md`
- If the user provides a specific template path under `.productmap/09_templates/`, prefer adapting it over inventing a new format.

## Detailed prompt (copy/paste)

You are a product manager doing customer development. Your goal is to convert a vague idea into **testable hypotheses** and a **learning plan**.

Constraints:
- **Do not** write interview scripts, question lists, talk tracks, or anything that resembles an interview-script workflow.
- Prefer falsifiable statements with clear observable signals and thresholds.
- Use absolute dates `YYYY-MM-DD` everywhere.
- Cite repo paths consulted (e.g. `.productmap/index.md`, optionally `.productmap/08_frameworks/jobs-to-be-done.md`, `.productmap/07_tools/research-analysis.md`).

Inputs:
- Today’s date: {{TODAY_YYYY-MM-DD}}
- Product idea: {{IDEA}}
- Target user/segment: {{USER_SEGMENT}}
- Context/constraints: {{CONSTRAINTS}}
- Current alternatives: {{ALTERNATIVES}}
- Evidence so far: {{EVIDENCE}}
- Timebox: start {{START_YYYY-MM-DD}}, decision by {{DECISION_YYYY-MM-DD}}

Output (Markdown), in this order:
1) **Idea snapshot** (2–5 bullets)
2) **JTBD (optional)**: job statement + key forces (only if helpful)
3) **Hypotheses**
   - Problem hypotheses (5–10)
   - User/segment hypotheses (5–10)
   - Value proposition hypotheses (5–10)
   Use this format for each hypothesis:
   - `H#:` We believe that **[user]** in **[context]** experiences **[problem]** causing **[undesired outcome]**.  
     We’ll consider this true if we observe **[signal]** at least **[threshold]** by **[date]**.
4) **Assumptions (risk-ranked)**
   - Table with columns: `Assumption`, `Why it matters`, `Uncertainty (1-5)`, `Impact (1-5)`, `Risk score`, `How we’ll test`, `Decision (pivot/persevere/kill)`
   - Highlight the top 3–5 “risky assumptions” and why they’re the crux.
5) **Test plan (no scripts)**
   - Table with columns:
     `Assumption`, `Test type`, `Setup`, `Who/where (participant criteria or traffic source)`, `Sample size`, `Data to capture`, `Success criteria`, `Failure criteria`, `Start date`, `End date`, `Owner`
   - Include at least one test that does **not** require 1:1 conversations (e.g., landing page, concierge MVP, prototype clickthrough with instrumentation, smoke test).
6) **Decision gates**
   - 2–4 gates with: `Gate date`, `What we decide`, `Inputs required`, `Go / No-go thresholds`
7) **Open questions**
   - Unknowns that are important but not top-risk (yet)
8) **Repo paths consulted**

## Workflow (runbook)

1. Read repo entrypoint `.productmap/index.md` for navigation and any relevant templates.
2. If helpful, pull framing from `.productmap/08_frameworks/jobs-to-be-done.md` (job, context, outcomes, forces).
3. Translate the vague idea into 3 layers of hypotheses:
   - Problem (pain, trigger, frequency, severity, constraints)
   - User/segment (who, context, buying center, ability/willingness to pay)
   - Value prop (promise, mechanism, why better than alternatives)
4. Convert each hypothesis into a falsifiable statement with:
   - Observable signal(s)
   - Threshold(s)
   - A date by which you’ll know
5. Enumerate assumptions and score them (impact × uncertainty). Pick the top 3–5 as “risky assumptions”.
6. Design a timeboxed test plan:
   - Map each risky assumption to the *cheapest credible* test
   - Define success/failure criteria and what data you’ll capture
   - Add start/end dates and owners
7. Add decision gates so the work results in a clear pivot/persevere/kill choice.
8. Final pass: ensure nothing resembles an interview script (no question lists), all dates are `YYYY-MM-DD`, and the plan is executable in the stated timebox.

## Quality checklist

- Hypotheses are specific, falsifiable, and written in a consistent format.
- Each risky assumption has a clear test with measurable success/failure criteria.
- The plan is timeboxed with absolute dates (`YYYY-MM-DD`) and named owners.
- Tests prioritize fast/low-cost learning before heavier builds.
- Includes at least one non-1:1 test approach (e.g. smoke test, landing page).
- Avoids interview scripts, talk tracks, and question lists entirely.
- References relevant repo knowledge via clickable paths (at minimum `.productmap/index.md`).
