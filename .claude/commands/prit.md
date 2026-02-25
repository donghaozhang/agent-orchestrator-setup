# Export PR Comments

Export and preprocess review comments from the current PR using the pr-comments scripts.

## Steps

1. Get the current PR number with `gh pr view --json number --jq .number`.
2. Get the repo with `gh repo view --json nameWithOwner --jq .nameWithOwner`.
3. Run `ao pr-comments export <repo> <pr>` to export all review comments.
4. Run `ao pr-comments preprocess docs/pr-comments/pr-<number>` to create task files.
5. Run `ao pr-comments analyze docs/pr-comments/pr-<number>-tasks` to show file groupings.
6. Report how many comments were found and the recommended fix order.
