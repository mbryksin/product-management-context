# Product management knowledge base (Gemini CLI)

You are assisting in a **personal product management knowledge repository** synced from [ProductMap.io](https://www.productmap.io). Treat **`.productmap/`** as the authoritative knowledge tree. Start navigation from **[`.productmap/index.md`](.productmap/index.md)** (same content intent as `INDEX.md`).

## Knowledge layout

| Area | Path | Use for |
|------|------|---------|
| Company / product artifacts | `.productmap/00_company/` | Roadmap, backlog, one-pagers |
| Strategy | `.productmap/01_strategy/` | Business model, PMF, MVP, segmentation, OKRs |
| Generation (discovery) | `.productmap/02_generation/` | User research, design/UX, marketing, growth, AI/ML |
| Analysis | `.productmap/03_analysis/` | KPIs, analytics, unit economics, finance |
| Delivery | `.productmap/04_delivery/` | Requirements, agile, lean, development, risk |
| People | `.productmap/05_people/` | Talent, communication, negotiation |
| Operations | `.productmap/06_operations/` | Product ops |
| Tools | `.productmap/07_tools/` | Writing, research, analytics, PM tools |
| Frameworks | `.productmap/08_frameworks/` | RICE, JTBD, OKRs, etc. |
| Templates | `.productmap/09_templates/` | PRD, user story, ADR, persona, board deck, retro |
| Data | `.productmap/10_data/` | Raw interviews, feedback, exports |

## Operating rules

1. **Read before writing.** Open the relevant `**/_overview.md` under `.productmap/` and the matching file in `09_templates/` before drafting artifacts.
2. **Templates are source of truth** for structure (PRDs, stories, OKRs, ADRs). Extend templates; do not invent incompatible sections without user approval.
3. **Initiative-specific outputs** belong under `.productmap/00_company/product/` unless the user specifies otherwise.
4. **Raw inputs** (interviews, dumps) go under `.productmap/10_data/`.
5. **Dates:** use absolute `YYYY-MM-DD` (e.g. `2026-04-17`).
6. **Sync note:** manual edits to `.productmap/` may drift from ProductMap.io; flag intentional vs accidental drift when relevant.

## Model strengths to leverage (Gemini)

Prefer tasks that benefit from **long-context synthesis**, **structured multi-section documents**, **clear hierarchies**, **blending narrative with checklists**, and **turning messy notes into spec-quality prose**. When the user attaches **screenshots, decks, or diagrams**, incorporate visual context explicitly.

## Project skills (Gemini)

Reusable workflows live under **`.gemini/skills/<skill-name>/`**. Each folder contains `SKILL.md` (how to run the workflow) and `subagent-prompt.md` (detailed delegation prompt for a sub-agent). Prefer these skills over ad-hoc instructions for the matching task. Claude Code skills that are not Gemini-oriented remain under [`.claude/skills/`](.claude/skills/).

## External reference

Curated topic list from the public Product Map page: [`.claude/resources/productmap-product-management-map-topics.md`](.claude/resources/productmap-product-management-map-topics.md).

Nested memory import (Gemini CLI): the following file is appended for folder-level navigation.

@./.productmap/index.md
