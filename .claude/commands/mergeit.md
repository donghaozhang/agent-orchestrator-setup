# Merge PR

Merge the current PR and clean up.

## Steps

1. Check the current branch and find the associated PR with `gh pr view`.
2. Verify CI is passing with `gh pr checks`.
3. Verify the PR is approved with `gh pr view --json reviewDecision`.
4. If mergeable, merge with `gh pr merge --squash --delete-branch`.
5. Switch to main/master and pull latest.
6. Report the merge result.

## If merge fails

- If CI is failing: run `/buildit` to fix it first.
- If review is pending: notify the user.
- If there are conflicts: rebase on main and resolve them.
