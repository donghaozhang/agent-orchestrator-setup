# Implement from Plan

Implement the plan file step by step.

## Steps

1. Read the plan markdown file provided by the user.
2. Implement each step for long-term maintainability rather than short-term gain.
3. Ensure the implementation follows the conventions in CLAUDE.md (ESM, `.js` imports, `execFile` not `exec`, plugin pattern with `satisfies`).
4. Test the implemented functionality — run `pnpm typecheck` and `pnpm lint` after changes.
5. Do not break existing features.
6. If a file is longer than 800 lines, split it into smaller modules.

## Rules

- Follow CLAUDE.md conventions strictly (TypeScript ESM, node: prefix, no `any`).
- Include relevant file paths in your progress reports.
- Run `pnpm build` to verify everything compiles.
