# Evaluate Review Comment

Evaluate a single PR review comment. If the feedback is valid, fix it. Otherwise explain why it doesn't apply.

## Steps

1. Read the review comment or task file provided.
2. Read the source file referenced in the comment.
3. Check the specific line and surrounding context.
4. Determine if the review feedback is valid.
5. If valid: fix the code and report what changed.
6. If invalid: explain in 2-3 sentences why it doesn't apply.

## Output Format

```
## Result: [FIXED | NOT_APPLICABLE | ALREADY_FIXED]

**File:** path/to/file.ts
**Line:** 123

**Action taken:** [Description of fix OR reason why not applicable]
```
