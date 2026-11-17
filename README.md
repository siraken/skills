# siraken-skills

An [APM](https://github.com/microsoft/apm) (Agent Package Manager) package: a
collection of agent skills for Claude Code and other AI coding agents.

## Skills

- **communication-review** — Checklist for drafting, reviewing, and posting questions, requests, and reports to other people (issue/PR comments, chat).
- **gemini-search** — Web search via the Google Gemini CLI.
- **github-issue-runner** — Execute a GitHub Issue end to end (branch → implement → PR).
- **refactor-suggestions** — Review the project and suggest concrete refactorings.

## Install

### Prerequisite: the APM CLI

Install the APM CLI once (it lives globally on your machine):

```bash
# macOS / Linux
curl -sSL https://aka.ms/apm-unix | sh

# Windows (PowerShell)
irm https://aka.ms/apm-windows | iex
```

Verify with `apm --version`. Homebrew, Scoop, and pip are also supported — see the
[APM installation docs](https://microsoft.github.io/apm/getting-started/installation/).

### Per project

Run inside the project you want the skills in:

```bash
apm install siraken/skills --target claude
```

This deploys the skills into the project's `.claude/skills/` and records them in
`apm.lock.yaml`. You can drop `--target claude` when the project already has a
`.claude/` directory — APM auto-detects the harness.

### Global (all projects)

Install to user scope with `-g` to make the skills available in every project:

```bash
apm install -g siraken/skills --target claude
```

This installs into your user scope (`~/.apm/`) so Claude Code picks the skills up
everywhere, without re-installing per project. (Claude is fully supported for
user-scope primitives.)

See the [APM docs](https://microsoft.github.io/apm/) for details.
