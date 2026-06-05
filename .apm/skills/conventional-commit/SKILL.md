---
name: conventional-commit
description: >-
  Activate when the user asks to commit changes. Produces commit messages that
  follow the Conventional Commits specification and split work into logical
  units.
---

# Commit

Commit changes to the repository.

## Rules

- Use English for commit messages, except for specific terms that are better left untranslated.
- Follow the Conventional Commits specification.
  - Use the format `type(scope): description` for commit messages.
  - Use `fix`, `feat`, `chore`, `docs`, `style`, `refactor`, `test`, `perf`, and `build` as types.
  - Use `scope` to indicate the area of the codebase affected by the change.
- Ensure that the commit message is clear and concise.
- Include relevant issue references in the commit message if applicable (e.g., `Fixes #123`).
- Avoid committing large changes in a single commit; break them down into logical units.
