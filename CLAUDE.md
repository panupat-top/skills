# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repo is

A Claude Code plugin marketplace that distributes personal agent skills. There is no build, lint, or test tooling — the content is Markdown and JSON manifests.

## Structure

The repo root is both the marketplace and its single plugin:

- `.claude-plugin/marketplace.json` — marketplace `panupat-top-skills`, listing one plugin with `"source": "./"` (the repo root).
- `.claude-plugin/plugin.json` — plugin `panupat-skills`. Skills are auto-discovered from `skills/`.
- `skills/<skill-name>/SKILL.md` — one directory per skill, with YAML frontmatter (`name`, `description`) and instructions. The `name` should match the directory name. Supporting files (scripts, references) go in the same directory.

Users install with:

```
/plugin marketplace add panupat-top/skills
/plugin install panupat-skills@panupat-top-skills
```

## Commands

- `claude plugin validate .` — validate the marketplace and plugin manifests. Run after changing anything in `.claude-plugin/` or adding a skill.

## Releasing changes

Bump `version` in `.claude-plugin/plugin.json` when skills change; installed users only receive updates when the version changes.
