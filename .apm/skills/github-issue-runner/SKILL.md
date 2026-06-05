---
name: github-issue-runner
description: >-
  Activate when the user asks to work on, implement, or execute a GitHub Issue
  (e.g. "run issue #123", "start on this issue"). Drives the full
  branch -> implement -> pull request workflow for that issue.
---

# Execute a GitHub Issue

Review the GitHub Issue content and carry out the task end to end.

## Steps

1. **Update main**: `git checkout main`, then `git pull origin main` to get the latest state.
2. **Read the issue**: `gh issue view #<number>` to inspect the details.
3. **Create a branch**: branch off main with a name derived from the issue.
4. **Break down tasks**: decompose the issue into concrete, ordered work items.
5. **Implement**: make the code changes for each item.
6. **Commit & push**: commit at sensible granularity and push as you progress.
7. **Open a PR**: run `gh pr create` once the work is complete.

## Notes

- Take the issue number from the user's request or the surrounding context.
- Follow the repository's existing branch-naming and commit conventions.
