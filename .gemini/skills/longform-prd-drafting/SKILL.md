---
name: longform-prd-drafting
description: Drafts and refines long-form PRDs using repo templates, traceable requirements, and metrics. Use when writing or restructuring a PRD, merging AI-specific sections, or turning messy notes into a coherent spec aligned with .productmap templates.
---

# Long-form PRD drafting

## When to use

- New initiative needs a full PRD or major revision.
- Inputs are scattered (tickets, notes, Slack); output must match `.productmap/09_templates/prd-template.md` (and `ai-prd-template.md` when AI/ML is in scope).

## Steps

1. Read [`.productmap/index.md`](../../../.productmap/index.md), then open `09_templates/prd-template.md` and relevant `_overview.md` under `04_delivery/backlog-requirements/` and strategy folders as needed.
2. Map user input to template sections; mark TBD and open questions where data is missing.
3. Link requirements to goals, acceptance criteria, and metrics; align prioritization language with `08_frameworks/rice.md` when scoring appears.
4. End with **Assumptions** (dated `YYYY-MM-DD`).

## Delegation

For a dedicated worker with full behavioral instructions, pass [subagent-prompt.md](subagent-prompt.md) as the sub-agent system prompt.
