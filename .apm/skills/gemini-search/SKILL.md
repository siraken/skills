---
name: gemini-search
description: >-
  Activate when the user needs a web search or up-to-date external information
  and the Google Gemini CLI (`gemini`) is available. Use it to fetch current
  information that may be outside the model's knowledge.
---

# Gemini Search

`gemini` is the Google Gemini CLI, which can perform web searches.

Run a web search through the Task tool by invoking `gemini` with a `WebSearch:` prompt:

```bash
gemini -p "WebSearch: <your query>"
```

## When to use

- The user asks for current events, the latest docs, or anything likely newer than the model's knowledge cutoff.
- You need to confirm an external fact before answering.

## Notes

- Keep the query focused; pass only the search intent after `WebSearch:`.
- Prefer running it via the Task tool so the search output is captured cleanly.
