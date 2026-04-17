---
name: competitor-landscape-brief
description: Produce a decision-ready competitive landscape with competitor table, differentiation, messaging hooks, risks, and follow-up intelligence questions.
---

# Competitor Landscape Brief (Competitor table + differentiation)

## Name

`competitor-landscape-brief` — Competitor landscape + differentiation brief

## When to use

- You need a fast, decision-ready view of the competitive landscape for a product/initiative.
- You’re preparing a PRD, strategy memo, board/exec update, or sales enablement and need crisp differentiation.
- You have scattered notes (calls, win/loss, decks, docs) and need a structured competitor table + positioning guidance.
- You need messaging “hooks” (taglines, proof points, objection handling) anchored to a target segment.
- You want risks/unknowns and a follow-up question list to drive ongoing competitive intelligence.

## Inputs

Ask the user for:

- Product / initiative name:
- One-sentence “what we do”:
- Target segment(s) (ICP) + buyer/user roles:
- Geography / regulatory constraints (if any):
- Competitive set:
  - Known direct competitors (names):
  - Indirect / substitutes (categories):
  - “Do nothing” / status quo alternative:
- Use cases / jobs-to-be-done (top 3):
- Differentiation hypotheses (what you believe you’re better at):
- Known constraints (pricing model, platform, channels, roadmap “won’t do”):
- Sources provided (any of these, with repo paths when applicable):
  - Notes, call transcripts, win/loss, RFPs, competitor decks, pricing pages (snippets), analyst reports
- As-of date for this snapshot (YYYY-MM-DD). If not provided, use the run date and write it explicitly (example: `2026-04-17`).

## Outputs

Produce a Markdown “Competitor Landscape Brief” that includes:

- Scope & assumptions (segment, geography, as-of date, sources used with repo paths)
- Competitor table (decision-ready, with confidence levels and evidence notes)
- Positioning map guidance (recommended axes + how to plot + interpretation notes)
- Differentiation summary (1–2 sentence positioning statement + 3–5 proof-backed pillars)
- Messaging hooks (by persona + common objections + “what to say instead”)
- Risks / watchouts (including legal/compliance considerations and unknowns)
- Follow-up questions (for interviews, sales, research, and CI cadence)

If the user asks you to write it back into the repo, suggest a path under:
- `.productmap/00_company/product/<initiative>/competitor-landscape-brief-YYYY-MM-DD.md`

## Repo knowledge to pull

Start by orienting in:
- `.productmap/index.md` (knowledge base entrypoint and navigation)

Optionally consult:
- `.productmap/07_tools/strategy-ci.md` (strategy / competitive intelligence tooling notes; may be a placeholder)

If the user provides additional relevant repo paths, prefer those over generic assumptions.

## Detailed prompt (copy/paste)

You are a product strategy analyst. Create a **Competitor Landscape Brief** for the product/initiative described below.

Hard constraints:
- Use **absolute dates** only (`YYYY-MM-DD`).
- Explicitly include an **As-of date** for the snapshot.
- Use only information in the user’s prompt and the repository files you read. If you are unsure, mark it as an assumption and label confidence.
- Avoid defamatory language and unsupported claims; keep comparisons factual and evidence-linked (or “unknown”).
- Cite the **repo file paths used** (clickable paths) in a “Sources” section.

Inputs (fill from user):
- Product / initiative:
- One-liner:
- Target segment(s) + buyer/user roles:
- Geography / constraints:
- Competitive set (direct, indirect, substitutes, status quo):
- Top use cases / JTBD (3):
- Differentiation hypotheses:
- As-of date (YYYY-MM-DD):
- Source files to read (repo paths):

Steps:
1. Read `.productmap/index.md`, then read the user-provided repo paths. Optionally read `.productmap/07_tools/strategy-ci.md`.
2. Normalize competitor names and categories. Separate **direct**, **indirect**, **substitutes**, and **status quo**.
3. Build a competitor table with **evidence notes** and **confidence** per row.
4. Recommend a positioning map (2x2) appropriate for the segment and use case; explain axes selection and plotting guidance.
5. Produce a differentiation summary: a positioning statement + 3–5 pillars with proof points and “how to defend” guidance.
6. Draft messaging hooks by persona:
   - Primary promise (1 sentence)
   - Proof points (3 bullets)
   - Objections & rebuttals (2–4)
   - Competitive “land/expand” wedge (if applicable)
7. Enumerate risks and unknowns; propose follow-up questions and a 2–4 week CI plan outline (lightweight).

Output format (Markdown):
- Title: Competitor Landscape Brief — <Product> — As of <YYYY-MM-DD>
- 1. Executive summary (5–8 bullets)
- 2. Scope & assumptions
- 3. Competitor table
  - Table columns (minimum):
    - Competitor
    - Type (Direct / Indirect / Substitute / Status quo)
    - Target segment(s)
    - Core promise (1 line)
    - Differentiators / strengths (bullets)
    - Weaknesses / gaps (bullets)
    - Pricing / packaging (known / unknown)
    - Distribution / GTM motion (PLG/Sales/Channel/etc., known/unknown)
    - Evidence notes (source path + brief note)
    - Confidence (High / Medium / Low)
    - “How we win” angle (1–2 lines)
- 4. Positioning map guidance
  - Recommended axes (with definitions)
  - Where each competitor plots (bullets, not invented numbers)
  - Interpretation: what the map suggests we should emphasize
  - “Don’t use this map if…” caveats
- 5. Differentiation & positioning statement
  - Positioning statement (template: For <ICP> who <need>, <Product> is a <category> that <benefit>. Unlike <competitor/alt>, it <key difference> because <reason-to-believe>.)
  - Differentiation pillars (3–5)
  - Proof points to collect (per pillar)
- 6. Messaging hooks
  - By persona (Buyer / User / Security / Finance as relevant)
  - Competitive talk tracks (what to say vs. what not to claim)
- 7. Risks, watchouts, and unknowns
- 8. Follow-up questions
  - For customers/prospects
  - For sales / CS / solutions engineering
  - For product/engineering
  - For market research
- 9. Sources (repo paths read)

End with: “Open questions for the requester” (3–8 questions).

## Workflow (runbook)

1. Confirm scope: segment, geography, and **as-of date (YYYY-MM-DD)**.
2. Read `.productmap/index.md` to orient, then read any user-specified repo paths; optionally read `.productmap/07_tools/strategy-ci.md`.
3. Draft the competitor table first; label each row with confidence and evidence notes.
4. Propose 1–2 candidate positioning maps; pick the one that best separates meaningful choices for the buyer.
5. Convert insights into differentiation pillars and persona-based messaging hooks.
6. Add risks/unknowns + a short list of follow-up questions that would most change the conclusions.
7. If writing to the repo is requested, save to `.productmap/00_company/product/<initiative>/competitor-landscape-brief-YYYY-MM-DD.md`.

## Quality checklist

- Includes **As-of date** in `YYYY-MM-DD` and avoids relative dates (“today”, “recently”).
- Clear separation of **direct vs indirect vs substitutes vs status quo**.
- Competitor table has evidence notes and confidence labels; unknowns are explicit.
- Positioning map axes are **interpretable** and relevant to the buyer’s decision (not vanity axes).
- Differentiation pillars are defensible (reasons-to-believe, proof points to collect).
- Messaging hooks avoid unsubstantiated claims and include objection handling.
- Risks include: stale info risk, segment mismatch risk, legal/compliance messaging risk, and “we might be the same” risk.
- Ends with crisp follow-up questions that could change strategy or positioning.
