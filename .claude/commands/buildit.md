# Monitor and Fix CI Build

Monitor the CI build for the current PR. If it fails, diagnose and fix the issue.

## Steps

1. Get the current PR with `gh pr view --json number --jq .number`.
2. Check CI status with `gh pr checks`.
3. If all checks pass, report success and stop.
4. If a check fails, get the logs with `gh run view <run-id> --log-failed`.
5. Diagnose the failure (lint, typecheck, test, build).
6. Fix the code and push the fix.
7. Re-check CI after the push.

## Rules

- Only fix what's needed to pass CI — no unrelated changes.
- Run `pnpm lint && pnpm typecheck` locally before pushing.
