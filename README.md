# Product management context engineering

This repository is your product management knowledge base and agentic workspace. You use it to connect durable product context to day-to-day PM work (strategy, discovery, delivery, alignment) so assistants behave like teammates who read your docs.

The [`.productmap/`](.productmap/) folder follows the same taxonomy you get from [Product Map](https://www.productmap.io/) when you sync or mirror the platform. On top of that tree, [AGENTS.md](AGENTS.md), [CLAUDE.md](CLAUDE.md), and [GEMINI.md](GEMINI.md) spell out how agents should behave; repeatable workflows live under [`.claude/skills/`](.claude/skills/) (Claude Code) and [`.gemini/skills/`](.gemini/skills/) (Gemini-oriented). You can point Claude, Codex, Gemini, and Cursor at one versioned source of truth instead of restarting context in every tool.

## Get started with this repository

**What you are building.** Product Map AI and the `.productmap/` tree are your context engineering and knowledge layer: curated lifecycle topics, templates, and frameworks in files agents can read. Cursor, Claude Code, Codex, and Gemini CLI sit on top as different runners; you pick the tool for the job and keep one repo as the handoff surface.

**A setup that works well**

- **Cursor** as the hub. Open this repo as the workspace so chat and edits see [AGENTS.md](AGENTS.md), [CLAUDE.md](CLAUDE.md), and [GEMINI.md](GEMINI.md) without path gymnastics. Use the Claude Code plugin for workflows that match [`.claude/skills/`](.claude/skills/). Use the Codex plugin with the same repo so Codex follows [AGENTS.md](AGENTS.md) (mirrored in [`.codex/README.md`](.codex/README.md)) and [`.codex/skills/`](.codex/skills/) (see [`.codex/skills/README.md`](.codex/skills/README.md)).
- **Claude Code** for skill-driven PM runs. The plugin reads [CLAUDE.md](CLAUDE.md) and routes recurring jobs through the right skill under [`.claude/skills/`](.claude/skills/) instead of one-off prompts.
- **Codex (inside Cursor)** when you want Codex-specific behavior and repo-local skills. Keep initiative outputs under `.productmap/00_company/product/` and raw inputs under `.productmap/10_data/` as [AGENTS.md](AGENTS.md) describes.
- **Gemini CLI** for jobs that need long-context synthesis, structured multi-section docs, or batch turns over the same tree. Install the Gemini CLI, open terminal in Cursor, `cd` to this repo, and rely on [GEMINI.md](GEMINI.md) plus [`.gemini/skills/`](.gemini/skills/) (see [`.gemini/README.md`](.gemini/README.md)). Optional: [`.gemini/settings.json`](.gemini/settings.json) for CLI defaults.
- **Product Map AI** ([app](https://app.productmap.io/)) to align assessments, learning paths, and copilots with the same map you mirror into `.productmap/`. Sync or copy from the platform when you want the repo to stay the single file-based source of truth.

**Steps**

1. Clone or copy this repository and open it in Cursor.
2. In [Product Map AI](https://app.productmap.io/) or on the platform, sync or export so `.productmap/` matches the taxonomy and content you care about. Treat manual edits under `.productmap/` as intentional; otherwise you risk drift from the platform.
3. Skim [`.productmap/INDEX.md`](.productmap/INDEX.md) (or `.productmap/index.md`) so you know where templates, frameworks, and overviews live.
4. For day-to-day PM work in Cursor, `@`-mention or paste paths to the relevant `_overview.md` files and `09_templates/` files instead of pasting unstructured blobs into chat.
5. For a recurring task (PRD, roadmap narrative, KPI spec, research synthesis), open the matching folder under [`.claude/skills/`](.claude/skills/) or [`.gemini/skills/`](.gemini/skills/) and follow `SKILL.md` rather than improvising.
6. For Codex in Cursor, match the task to a skill under [`.codex/skills/`](.codex/skills/) when one exists; ground answers in `.productmap/index.md` first.
7. Put initiative-specific artifacts in `.productmap/00_company/product/`. Put interviews, exports, and raw feedback in `.productmap/10_data/`.
8. Use absolute dates (`YYYY-MM-DD`) in anything you write back to the repo.

You stay the orchestrator: same knowledge layer, different agents for different strengths; the repo is where outputs compound.

## What context engineering means for you

**Context engineering** means you choose what an agent sees, in what format, and in what order, so outputs stay consistent, reviewable, and tied to the product. You shape the whole environment around the task, not only the line you type into the chat box.

PM-oriented context engineering covers more than prompt engineering (one question, one reply) and more than context stuffing (pasting every PDF into the window). In practice it does three jobs:

- Separates roles: instructions (how the agent should act), durable knowledge (facts, templates, decisions), retrieval (large or fast-changing sources), and runtime context (the live initiative, ticket, or interview batch).
- Slows drift: when priorities, messaging, and constraints move every week, shared files beat everyone keeping a private story in chat threads.
- Stays repo-first: Git gives history, review, rollback, and portability. Your team owns the text in files you can branch and diff.

Think in four layers: canonical project knowledge, then agent instruction files, then runtime task context, then personal preferences. Keep root instruction files short. Link to [`.productmap/INDEX.md`](.productmap/INDEX.md) and templates; pull deeper files only when the task needs them.

## TASK: topics, agents, skills, knowledge

The [TASK framework](https://www.productmap.io/task-agentic-product-management) (Product Map, 2026-04-02) names how agentic PM work fits together. You stay the orchestrator. Scoped helpers run in clear domains on your product context; you keep judgment and calls.

| Pillar | Role |
|--------|------|
| T: Topics | PM domains and expert-led resources; the space where work happens (strategy, generation, analysis, delivery, people). |
| A: Agents | Scoped executors (research, drafting, prioritization, synthesis) with prompts, memory, and access to the right files. |
| S: Skills | Your competences and quality bars: what to delegate, how to steer agents, where to step in. |
| K: Knowledge | Outputs that compound: specs, roadmaps, research, decision logs; plain text, versioned, written back each cycle. |

### A loop you can run

- Start with one PM domain you are in today (discovery, analytics, delivery, and so on).
- Define or refine an agent: system prompt, tools, and which folders it may read or write.
- Apply your skills: steer output, set the bar, validate.
- Write back to the repo under `.productmap/` and raw inputs under `10_data/` so the next task reuses work.

Each pass gets faster when knowledge compounds and context stays clean. When output is wrong, thin, or stale, you fix the source: the instruction or file that led to it.

## How this repository supports that workflow

- [`.productmap/`](.productmap/). Topics, frameworks, and templates along the product lifecycle.
- [`AGENTS.md`](AGENTS.md) and [`CLAUDE.md`](CLAUDE.md). Entry points that send agents to the index and house rules.
- Skills. Repeatable PM jobs with steps and guardrails: [`.claude/skills/`](.claude/skills/) for Claude Code, [`.gemini/skills/`](.gemini/skills/) for Gemini CLI (see [`.gemini/README.md`](.gemini/README.md)).
- Codex skills. Repo-local PM skills for Codex: [`.codex/skills/`](.codex/skills/) (see [`.codex/skills/README.md`](.codex/skills/README.md)).

If you edit `.productmap/` by hand, treat it as drift from the platform unless you mean to own that change.

## Product Map AI

[Product Map AI](https://app.productmap.io/) is where you turn structured product management context into day-to-day help. You attach your product context so assistants stay aligned with your situation instead of generic advice. The copilot draws on the same topic map and materials that experts curate across the lifecycle, so AI help stays grounded in proven approaches, not stray prompts.

You get PM-oriented assistants for real tasks (strategy, discovery, delivery, collaboration, data-informed decisions, career support), plus skills assessment, gap analysis, growth plans, progress tracking, and a knowledge hub that stays tied to those resources. Use it when you want the app experience: assessments, plans, and assistants that sit on top of industry-led expert content, with your context in the loop.

## About Product Map

[Product Map](https://www.productmap.io/) is the **product management copilot to guide your decisions.** It offers tools and resources for the entire product lifecycle, built so you can learn, build, and grow as a product person.

## Product Map

Product Map is a community-built home for product work. It maps the full PM lifecycle into curated topics, resources, and frameworks (strategy, discovery, analysis, delivery, people). You get structured paths to learn and apply. Together, the map and your repo answer how you learn, build, and ship product work with a repeatable system.
