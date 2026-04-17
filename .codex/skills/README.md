# Codex skills (repo-local)

This folder contains **repo-local Codex skills** for common product management tasks.

For overall Codex agent behavior in this repository, see `.codex/README.md` (mirrors `AGENTS.md`).

## How to use

- Each `SKILL.md` starts with YAML frontmatter (`name`, `description`) so tools like `npx skills` can index and install the skill.
- Treat each skill as a repeatable workflow: open the folder and follow `SKILL.md`.
- Ground outputs in this repository first: start at `.productmap/index.md`, then pull in relevant templates under `.productmap/09_templates/` and frameworks under `.productmap/08_frameworks/`.

## Skills included

- `.codex/skills/ai-feature-brief/SKILL.md`
- `.codex/skills/business-model-canvas/SKILL.md`
- `.codex/skills/competitor-landscape-brief/SKILL.md`
- `.codex/skills/customer-development-hypotheses/SKILL.md`
- `.codex/skills/design-thinking-workshop-plan/SKILL.md`
- `.codex/skills/market-research-synthesis/SKILL.md`
- `.codex/skills/market-segmentation-icp/SKILL.md`
- `.codex/skills/mvp-scope-decision/SKILL.md`
- `.codex/skills/negotiation-prep-brief/SKILL.md`
- `.codex/skills/product-ops-operating-model/SKILL.md`

## Conventions

- Skills are written as prompt templates with clear inputs/outputs and a step-by-step runbook.
- Use absolute dates (`YYYY-MM-DD`) in any artifacts.
