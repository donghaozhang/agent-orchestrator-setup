# Process PR Review Tasks

Process all PR review task files one by one: evaluate, fix, resolve, and commit.

## Steps

1. Find the tasks directory (e.g., `docs/pr-comments/pr-<number>-tasks/`).
2. Group task files by source file.
3. For each source file, sort comments by line number descending (bottom-up).
4. For each comment:
   a. Read the task file to understand the review feedback.
   b. Read the source file and check the referenced line.
   c. Evaluate if the feedback is valid.
   d. If valid: fix the code. If invalid: note why.
5. After fixing all comments for a file, commit the changes.
6. Resolve each fixed thread on GitHub with `ao pr-comments resolve`.
7. Push all changes when done.

## Critical Rules

- **Fix bottom-up** (highest line number first) to avoid line shifts.
- **Group by file** — process all comments for one file before moving to the next.
- Only fix what the review mentions — don't make unrelated changes.
