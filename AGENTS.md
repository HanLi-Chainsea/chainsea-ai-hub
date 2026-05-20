# ChainSea AI Hub Agent Guide

This repo contains a built-in hub maintenance skill at:

```txt
.claude/skills/hub-curator/SKILL.md
```

Claude Code should auto-register it after cloning the repo. Use:

```txt
/hub-curator add this repo:
https://github.com/example/project
```

For tools that do not auto-load `.claude/skills/`, read `.claude/skills/hub-curator/SKILL.md` and follow that workflow manually.

## Important Rules

- Do not copy full target repositories into this hub.
- Clone external repos only to a temporary analysis location.
- Keep category pages short and scannable.
- Move long analysis, verification, risks, and update history into detail pages.
- Use `resources/watchlist.md` for promising but unverified resources.

## Codex CLI Note

In the current verified environment, Codex can load this skill through a user-level symlink:

```bash
ln -s "$(pwd)/.claude/skills/hub-curator" ~/.codex/skills/hub-curator
```

Repo-local Codex skill auto-registration is not assumed by this hub until verified.
