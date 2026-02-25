Read the skill at .claude/skills/codex-delegate/SKILL.md if it exists, then evaluate the user's task:

1. Decide: should this be done by you (Claude Code) or delegated to Codex via `ao spawn`?
2. Print your reasoning in 1-2 lines.
3. If delegating: use `ao spawn <project> --agent codex` with a clear task description.
4. If handling yourself: proceed directly with implementation.
