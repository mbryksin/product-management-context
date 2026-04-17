---
name: market-research-synthesis
description: Synthesize desk research and notes into an executive market brief with structure, gaps, and implications using only provided inputs plus the .productmap knowledge base.
---

# Market research synthesis (desk notes → exec-ready brief)

## Name

`market-research-synthesis` — synthesize desk research / notes into an exec-ready market brief

## When to use

- You have messy desk research (notes, interview summaries, copied snippets, internal docs) and need an executive market brief.
- You need a consistent structure: market size ranges, trends, key players, risks, implications, and a TODO list for missing data.
- You want to organize (not expand) research: no new external browsing; use only provided inputs + repo knowledge base.

## Inputs (ask user for these)

- Brief name (1 line):
- Research “as-of” date (`YYYY-MM-DD`):
- Geography / regions in scope:
- Customer segment(s) / buyer + user:
- Product category definition (what’s in / out of scope):
- Time horizon (e.g., `2026-2029` or `2026-04-17` to `2029-12-31`):
- Notes to synthesize (paste or attach):
- Internal sources to include (repo paths, docs, slides):
- Required output length (e.g., 1 page, 2 pages, 5 bullets/section):
- Decision context (what execs need to decide next):

## Outputs

- An exec-ready **Market Brief** containing:
  - Market definition + taxonomy (what is / isn’t included)
  - Market size **ranges** (TAM/SAM/SOM where possible) + assumptions + confidence
  - Growth drivers + trends (near/medium term)
  - Key players (incumbents, challengers, adjacent substitutes) + positioning
  - Buyer economics / pricing anchors (if present in notes)
- Distribution / channel dynamics (if present in notes)
  - Risks & uncertainties (data quality, structural, competitive, regulatory)
  - Implications for product strategy (what it suggests we do / avoid / test)
  - **TODO list for missing data** (what to collect next, where, and why it matters)
- Optional (if user asks to write back): store under `.productmap/00_company/product/` as `market-brief_<brief-name>_<YYYY-MM-DD>.md`.

## Repo knowledge to pull

- Entrypoint: `.productmap/index.md`
- Optional tools (use if relevant to structuring the analysis):
  - `.productmap/07_tools/research-analysis.md`
  - `.productmap/07_tools/strategy-ci.md`
- Optional templates/frameworks to look for via the index (pick only what helps; don’t invent new structures if one exists):
  - Market / competitive analysis templates under `.productmap/09_templates/`
  - Strategy frameworks under `.productmap/08_frameworks/`

## Detailed prompt (copy/paste)

You are a product strategy analyst. Synthesize the provided desk research / notes into an executive-ready **Market Brief**.

Constraints:
- Do **not** browse the web or introduce new external facts.
- Use only: (a) the notes I provide, and (b) repo knowledge from `.productmap/**` that helps structure the output.
- Use absolute dates (`YYYY-MM-DD`) everywhere.
- Where the notes are incomplete, provide **ranges** (not point estimates), label assumptions explicitly, and add a TODO.
- If the notes conflict, reconcile by listing competing claims and what would resolve them.

Steps:
1. Read `.productmap/index.md` and pull any relevant template/framework references (cite repo paths used).
2. Parse the notes into atomic claims. Tag each claim with: `Evidence` (quote/paraphrase from notes), `Source` (note identifier), and `Confidence` (High/Med/Low).
3. Define the market: scope, customer segments, use cases, substitutes, and boundary conditions.
4. Synthesize market sizing into TAM/SAM/SOM **ranges** if possible, showing the sizing logic and assumptions used (or explain why sizing is not possible from current notes).
5. Summarize trends and drivers, and list key players with a simple positioning snapshot.
6. Produce risks/uncertainties and the strategic implications for our product decisions.
7. End with a prioritized TODO list for missing data (what to collect next).

Output format (Markdown):
- Title: `Market Brief — <Brief name> — As of <YYYY-MM-DD>`
- `1) Executive summary` (5–10 bullets, decision-oriented)
- `2) Market definition & scope` (incl. in/out)
- `3) Market size (ranges)` (TAM/SAM/SOM if possible; otherwise “Not estimable from current notes” + TODO)
- `4) Trends & drivers` (near-term vs medium-term; link to implications)
- `5) Key players & landscape` (table: Player | Category | Strengths | Weaknesses | Notes)
- `6) Risks & uncertainties` (table: Risk | Why it matters | Leading indicator | Mitigation | Confidence)
- `7) Implications for product strategy` (bets, no-regrets moves, experiments)
- `8) TODOs / missing data` (table: Missing info | Why it matters | How to get it | Owner (TBD) | Due date (TBD))
- `Appendix: Notes map` (brief index of note sources used)
- `Repo paths referenced` (explicit list of `.productmap/**` files used)

## Workflow (runbook)

1. Locate structure: open `.productmap/index.md` and identify any relevant market/strategy templates; decide which to apply.
2. Ingest notes: label each input note source (e.g., `N1`, `N2`, …) so claims can be traced.
3. Extract claims: convert notes into a claim list; flag contradictions and unknowns early.
4. Draft the Market Brief using the required sections; keep it exec-readable (tight bullets, tables).
5. Add market sizing ranges only when the notes support a method; otherwise state “not estimable” and create TODOs.
6. Add a TODO list that is specific and actionable (what, why, how, and the decision it unblocks).
7. Final pass: ensure dates are absolute, assumptions are explicit, and every major assertion traces back to a note source.

## Quality checklist

- No web browsing or external facts introduced.
- Title includes an “as-of” date in `YYYY-MM-DD`.
- Market definition is explicit (scope boundaries + substitutes).
- Market sizing is expressed as ranges with assumptions and confidence (or clearly marked as not estimable).
- Trends are tied to drivers and implications (not a generic list).
- Key players list is segmented (incumbent/challenger/adjacent) and includes positioning notes.
- Risks include leading indicators and mitigations; confidence is stated.
- Implications are decision-oriented (what we should do next) and match the decision context.
- TODO list is prioritized and each item states why it matters and how to obtain it.
- “Repo paths referenced” lists the `.productmap/**` files actually used.
