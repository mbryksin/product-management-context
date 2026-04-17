# Codex Agent Instructions (product-management-context)

This repository is a **product management knowledge base**. Prefer using it as source material when answering questions or generating artifacts.

## Knowledge base entrypoint

- Start at `.productmap/index.md` (alias of `.productmap/INDEX.md`) to navigate topics and templates.
- When you reference knowledge, include clickable file paths (e.g. `.productmap/09_templates/prd-template.md`).

## Working principles

- Read first, then write: consult the most relevant `.productmap/**/_overview.md` and templates under `.productmap/09_templates/` before drafting anything new.
- Prefer adapting existing templates over inventing new structures.
- Keep edits minimal and focused; treat `.productmap/` as a synced source and avoid large rewrites unless explicitly requested.

## Artifacts and storage

- Put initiative-specific artifacts under `.productmap/00_company/product/` (unless the user requests a different location).
- Store raw inputs (interviews, feedback, analytics exports) under `.productmap/10_data/`.

## Conventions

- Use absolute dates (`YYYY-MM-DD`).
- If you make assumptions, state them briefly.

## Gemini CLI

Project context for [Gemini CLI](https://github.com/google-gemini/gemini-cli) is in `GEMINI.md` (with `.productmap/index.md` imported). Optional CLI settings: `.gemini/settings.json`. Gemini-oriented skills: `.gemini/skills/` (see `.gemini/README.md`).

## Codex skills (repo-local)

- Repo-local Codex skills live under `.codex/skills/` (each skill is a folder with a `SKILL.md`).
- When a task matches a skill, follow it and reference `.productmap/index.md` + relevant templates/frameworks.
