---
name: refactor-suggestions
description: >-
  Activate when the user asks for refactoring suggestions or a code-quality
  review of the project (e.g. "suggest refactors", "how can I clean this up?").
  Produces concrete, prioritized improvement proposals.
---

# Refactoring Suggestions

Review the structure and content of the project and provide specific refactoring suggestions. Pay attention to the following points when making proposals:

1. **Code Readability**: Check whether the code is readable and easy to understand. Verify that variable, function, and class names are appropriate, and that comments are adequate.
2. **Code Reusability**: Consider whether there is duplicated code and whether common processing can be consolidated into functions or classes.
3. **Performance**: Check for areas where execution speed or memory usage can be improved.
4. **Test Coverage**: Verify whether unit and integration tests are sufficiently covered, and whether any necessary tests are missing.

## Notes

- Prioritize proposals by impact and effort.
- Reference concrete files and line numbers where possible.
