# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repo is

An [APM](https://github.com/microsoft/apm) (Agent Package Manager) package that ships agent skills. There is no application code, build step, or test suite — the deliverables are `SKILL.md` files. Consumers install it with `apm install siraken/skills --target claude` (or `-g` for user scope), which deploys the skills into their `.claude/skills/`.

## Layout and how packaging works

- `apm.yml` — package manifest. `includes: auto` means APM picks up everything under `.apm/` automatically; there is no per-skill registration list.
- `.apm/skills/<skill-name>/SKILL.md` — one directory per skill. Only skills placed here are packaged. A skill directory anywhere else (e.g. at the repo root) is not shipped.
- `README.md` — the `## Skills` list is maintained by hand.

History: the repo was previously a Claude plugin marketplace (`.claude-plugin/marketplace.json` + slash commands) and was migrated to APM in #1. Former slash commands were converted into auto-activating skills; don't reintroduce the plugin/marketplace structure.

## Adding, changing, or removing a skill

1. Create/edit `.apm/skills/<name>/SKILL.md`. Frontmatter needs `name` (matching the directory name) and `description`. The `description` is what drives auto-activation, so phrase it as "Activate when the user …" / "Use when …" with concrete trigger phrases.
2. Keep these in sync in the same change: the `## Skills` list in `README.md` and the prose `description` in `apm.yml` (it enumerates the skill themes).

## Useful commands

APM CLI commands pre-approved in `.claude/settings.local.json`:

```bash
apm --version
apm compile ...   # compile/validate the package
apm audit ...
apm pack ...      # build the distributable package
```

Run `apm --help` for exact subcommand usage rather than guessing flags.

## Conventions

- Commit messages: short, lowercase, imperative, no conventional-commit prefix (e.g. `remove conventional-commit and task-orchestrator skills`).
