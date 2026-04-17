# Product Management Context

This repository is a **personal product management knowledge base** synced from the [ProductMap.io](https://app.productmap.io) platform. It contains structured PM knowledge covering the full product lifecycle — strategy, generation, analysis, delivery, and supporting practices.

## Knowledge base entrypoint

- **Start here:** [.productmap/index.md](.productmap/index.md) (alias of `.productmap/INDEX.md`) — topic index, navigation, and links into frameworks and templates across the tree.
- Use it as the **canonical map** before drafting artifacts or answering PM questions; drill into section `_overview.md` files and `09_templates/` as needed.

## Repository structure

All content lives under [.productmap/](.productmap/) and mirrors the ProductMap.io taxonomy. See [.productmap/index.md](.productmap/index.md) for the full index. Top-level sections:

- `00_company/` — company and product one-pagers, roadmap, backlog
- `01_strategy/` — business model, PMF, MVP, segmentation, OKRs
- `02_generation/` — user research, design/UX, marketing, growth, AI/ML
- `03_analysis/` — KPIs, analytics, unit economics, finance
- `04_delivery/` — requirements, agile, lean, development, risk
- `05_people/` — talent, communication, negotiation
- `06_operations/` — product ops
- `07_tools/` — PM tool landscape (writing, research, analytics, etc.)
- `08_frameworks/` — RICE, JTBD, OKRs, other frameworks
- `09_templates/` — PRD, user story, ADR, persona, board deck, retro, etc.
- `10_data/` — raw data, interviews, feedback, research notes

## How to work in this repo

- **Read before writing.** When answering a PM question, first consult the relevant `_overview.md` under `.productmap/` and the matching template in `09_templates/`. Cite file paths so the user can navigate.
- **Templates are the source of truth.** For artifacts like PRDs, user stories, or OKRs, use the templates under [.productmap/09_templates/](.productmap/09_templates/) rather than inventing structure.
- **Frameworks are reusable tools.** Pull from [.productmap/08_frameworks/](.productmap/08_frameworks/) (RICE, JTBD, etc.) when the task calls for prioritization, discovery, or goal-setting.
- **Data stays in `10_data/`.** Interviews, analytics dumps, and raw feedback belong there — not scattered through the other sections.

## Skills

- **Claude Code:** domain-specific PM skills live under [.claude/skills/](.claude/skills/). Each skill encodes a PM practice and is invoked via `/skill-name` or auto-matched by description.
- **Gemini CLI:** workflows created for Gemini (long-context synthesis, structured docs, AI specs) live under [.gemini/skills/](.gemini/skills/); see [GEMINI.md](GEMINI.md).

Prefer skills over ad-hoc prompts for recurring PM tasks.

## Conventions

- Dates are absolute (`2026-04-17`), never relative.
- Artifacts for a specific initiative go under `00_company/product/` — reference frameworks/templates instead of duplicating them.
- Keep `.productmap/` in sync with the platform; treat manual edits as drift and flag them.
