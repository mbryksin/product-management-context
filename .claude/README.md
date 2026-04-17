# Claude Code configuration

This directory configures Claude Code for the product-management-context repository.

- `settings.json` — project-scoped permissions (read-only access to knowledge base by default).
- `skills/` — reusable PM skills for Claude Code. See [skills/README.md](skills/README.md) for the index. Each subdirectory contains a `SKILL.md` with YAML frontmatter (`name`, `description`) and the skill instructions. Claude auto-matches skills by their description; you can also invoke them explicitly as `/skill-name`. Ground work in the knowledge base at [`.productmap/index.md`](../.productmap/index.md).

See the root [CLAUDE.md](../CLAUDE.md) for repository conventions. **Gemini-oriented** skills (including `subagent-prompt.md` pairs added for Gemini workflows) live under [`.gemini/skills/`](../.gemini/skills/). For **Gemini CLI**, see the root [`GEMINI.md`](../GEMINI.md) and [`.gemini/settings.json`](../.gemini/settings.json).
