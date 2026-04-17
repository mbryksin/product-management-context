---
name: negotiation-prep-brief
description: Prepare negotiations with BATNA, targets, concessions, stakeholder map, and a one-page brief for scope, pricing, timeline, or cross-functional commitments.
---

# Negotiation Prep Brief (BATNA, targets, concessions, stakeholder map)

## Name

`negotiation-prep-brief` — Negotiation preparation pack + 1-page brief

## When to use

- You’re about to negotiate scope, price, timeline, resourcing, SLA/SLOs, contract terms, or cross-functional commitments.
- You need a clear BATNA/target/walk-away before entering a customer, vendor, partner, or internal negotiation.
- You want to align a team (PM/Eng/Legal/Sales/Finance/etc.) on issues, trades, and authority/approvals.
- You have multiple stakeholders and need a map of incentives, influence, and negotiation roles.
- You need a concise, shareable **1-page brief** to bring into the meeting.

## Inputs

Ask the user for:

- Negotiation name:
- Counterparty / parties involved (names + orgs):
- Negotiation type: Customer / Vendor / Partner / Internal
- Primary objective (1 sentence):
- Decision deadline(s) (YYYY-MM-DD) and key meeting times (if any):
- Context and constraints:
  - Scope / product area:
  - Budget / pricing constraints:
  - Policy/legal/compliance constraints:
  - Non-negotiables:
- Issues to negotiate (initial list if known):
- Proposed deal outline (current offer / ask):
- Stakeholders (internal + external):
  - Roles, incentives, influence, and approval authority
- Known relationship history (if any) and risks:
- Source files to read (repo paths), if any:
- As-of date for this prep (YYYY-MM-DD). If not provided, use the run date and write it explicitly (example: `2026-04-17`).

## Outputs

Produce a Markdown “Negotiation Prep Brief” that includes:

- Scope & assumptions (including **as-of date** and sources used with repo paths)
- **BATNA** (best alternative), plus how to strengthen it before the negotiation
- **Target** outcome (aspirational-but-plausible) and “good” outcome range
- **Walk-away** (reservation point) + conditions that trigger it
- **Issues list** (issue-by-issue interests, positions, options, evidence, and risks)
- **Concessions plan** (what you can trade, sequencing, and what you require in return)
- **Stakeholder map** (people, incentives, influence, likely positions, and comms plan)
- **1-page brief** section (printable / meeting-ready)
- Open questions + next actions before the negotiation (with owners and due dates in `YYYY-MM-DD`)

If the user asks you to write it back into the repo, suggest a path under:
- `.productmap/00_company/product/<initiative>/negotiation-prep-brief-YYYY-MM-DD.md`

## Repo knowledge to pull

- Start: `.productmap/index.md` (knowledge base entrypoint and navigation)
- Optionally: `.productmap/07_tools/meetings.md` (meeting hygiene / agenda / notes patterns; may be a placeholder)
- If the user provides additional relevant repo paths, prefer those over generic assumptions.

## Detailed prompt (copy/paste)

You are a negotiation prep partner supporting a product leader. Create a **Negotiation Prep Brief** for the negotiation described below.

Hard constraints:
- Use **absolute dates** only (`YYYY-MM-DD`).
- Include an explicit **As-of date** for the prep.
- Use only information in the user’s prompt and the repository files you read. If uncertain, label it as an assumption with a confidence level.
- Be practical: focus on the few issues and trades that change outcomes; avoid generic negotiation advice.
- Include a “Sources” section that cites **repo file paths read** (clickable).

Inputs (fill from user):
- Negotiation name:
- Parties (internal + external):
- Negotiation type:
- Primary objective:
- Decision deadline(s) (YYYY-MM-DD):
- Current offer / ask:
- Issues to negotiate (initial list):
- Constraints / non-negotiables:
- Stakeholders + approval authority:
- Relationship history / context:
- As-of date (YYYY-MM-DD):
- Repo paths to read:

Steps:
1. Read `.productmap/index.md`, then read any user-provided repo paths. Optionally read `.productmap/07_tools/meetings.md`.
2. Restate the objective, scope, decision deadline(s), and key constraints; call out unknowns that block setting a walk-away.
3. Define BATNA:
   - Best alternative (what we do if no deal)
   - How to improve BATNA before the deadline (concrete actions)
   - BATNA credibility signals (what makes it believable)
4. Set outcomes:
   - Target outcome (specific numbers/terms where possible)
   - Acceptable “good” range (bounded)
   - Walk-away / reservation point (terms that make the deal worse than BATNA)
5. Build an issues table (prioritize top 5–10):
   - Issue, our interests, our opening position, our fallback, their likely interests, possible packages, and evidence/notes.
6. Build a concessions plan:
   - Concession list with “cost to us” and “value to them”
   - Sequencing (what to hold, what to trade early/late)
   - Required reciprocation for each concession
7. Build a stakeholder map:
   - Internal stakeholders (influence/interest/authority; what they need to sign off)
   - External stakeholders (decision-maker, champion, blocker, legal/procurement)
   - Comms plan (who talks to whom, by when)
8. Produce a **1-page brief**:
   - Objective + target + walk-away
   - Top issues + proposed packages
   - Concession strategy
   - Stakeholder plan
   - Next actions before meeting (owners + dates)

Output format (Markdown):
- Title: Negotiation Prep Brief — <Negotiation name> — As of <YYYY-MM-DD>
- 1. Executive summary (6–10 bullets)
- 2. Scope, objective, and constraints
- 3. BATNA (and how to strengthen it)
- 4. Target, good range, and walk-away
- 5. Issues list (table)
  - Table columns (minimum):
    - Issue
    - Our interests (why it matters)
    - Our opening position
    - Our fallback
    - Their likely interests
    - Package/trade options
    - Evidence/notes (source path + brief note)
    - Risk (High/Medium/Low)
- 6. Concessions plan
  - Concession inventory (what we can give)
  - Sequencing and “if/then” trades
  - Red lines / non-negotiables
- 7. Stakeholder map
  - Internal (RACI-ish: Decider/Approver/Consulted/Informed)
  - External (Decision-maker/Champion/Blocker/Legal/Procurement)
  - Comms plan (touchpoints + owners + dates)
- 8. 1-page brief (meeting-ready)
- 9. Open questions + next actions (owners + due dates)
- 10. Sources (repo paths read)

End with: “Questions for the requester” (3–8 questions that, if answered, would most change targets or walk-away).

## Workflow (runbook)

1. Confirm **as-of date** (`YYYY-MM-DD`), decision deadline(s), and who has final authority.
2. Read `.productmap/index.md` to orient; then read the user-specified repo paths; optionally read `.productmap/07_tools/meetings.md`.
3. Draft BATNA and walk-away first; if info is missing, list the minimum questions needed to set them.
4. Prioritize issues (top 5–10) and define packages (bundles of trades) rather than single-issue haggling.
5. Create a concessions plan with explicit reciprocity and sequencing.
6. Map stakeholders and approvals; identify potential blockers and the plan to neutralize them before the meeting.
7. Produce the 1-page brief last to ensure it matches the detailed sections.
8. If writing to the repo is requested, save to `.productmap/00_company/product/<initiative>/negotiation-prep-brief-YYYY-MM-DD.md`.

## Quality checklist

- Includes **As-of date** in `YYYY-MM-DD` and avoids relative dates (“today”, “next week”).
- BATNA is concrete and improvable (includes actions to strengthen it before the deadline).
- Target, good range, and walk-away are specific (numbers/terms where possible) and consistent with BATNA.
- Issues list is prioritized and evidence-linked; unknowns are explicit.
- Concessions plan enforces reciprocity (“if/then”) and sequencing; red lines are clear.
- Stakeholder map identifies authority, incentives, and blockers; comms plan has owners and dates.
- 1-page brief is genuinely meeting-ready (fits on one page when printed; no deep background).
- Ends with crisp questions that would materially change targets or the walk-away.
