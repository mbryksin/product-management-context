# Gemini agent assets

- **`settings.json`** — Gemini CLI context (`GEMINI.md`, `AGENTS.md`).
- **`skills/`** (under `.gemini/`) — PM workflows tuned for Gemini (each folder: `SKILL.md` + optional `subagent-prompt.md`). Knowledge and templates still live under [`.productmap/`](../.productmap/).
- The repository root [`skills/`](../skills/) directory mirrors these same workflows with file symlinks so the open `npx skills` CLI discovers them under the standard `skills/` path (see root `README.md`).

See the root [`GEMINI.md`](../GEMINI.md) for full agent instructions.
