# skills

Personal agent skills, packaged as a Claude Code plugin marketplace.

## Install

```
/plugin marketplace add panupat-top/skills
/plugin install panupat-skills@panupat-top-skills
```

## Add a skill

Create `skills/<skill-name>/SKILL.md`:

```markdown
---
name: skill-name
description: What it does and when to use it.
---

Instructions...
```

Bump `version` in `.claude-plugin/plugin.json` so installed users get the update.
