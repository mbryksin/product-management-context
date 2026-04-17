# Skill template (copy/paste)

## Name

`skill-id` — short human name

## When to use

- Bullet list of triggers / user intents

## Inputs (ask user for these)

- Product / area:
- Target users / segment:
- Context files to read (repo paths):
- Time horizon / timeframe (absolute dates):
- Constraints (tech, policy, budget, regions):

## Outputs

- What gets written (and suggested repo path if writing back)

## Repo knowledge to pull

- Start: `.productmap/index.md`
- Templates: `.productmap/09_templates/...`
- Frameworks/tools: `.productmap/08_frameworks/...`, `.productmap/07_tools/...`

## Detailed prompt (copy into Codex/ChatGPT)

Role, goal, constraints, steps, and output format. Include explicit “cite repo paths used”.

## Workflow (runbook)

1. Read the specified repo context.
2. Ask clarifying questions only if blocking.
3. Produce the requested artifact.
4. Write back to the agreed repo location (if requested).
5. Provide a short review checklist.
