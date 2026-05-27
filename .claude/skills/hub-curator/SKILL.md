---
name: hub-curator
description: Maintain chainsea-ai-hub, an internal AI engineering resource hub. Use when adding, reviewing, classifying, or updating repositories, tools, MCP servers, agent skills, AI workflows, templates, technical articles, development experience notes, or case studies in the hub.
---

# Hub Curator

## Overview

Use this skill to keep `chainsea-ai-hub` useful, current, and easy to maintain. The goal is to turn a resource link or rough note into a classified, practical, time-aware hub entry.

## Core Workflow

1. Inspect the provided resource or note.
2. Identify what problem it solves, who should use it, and what inputs/outputs it expects.
3. Classify it using `references/taxonomy.md`.
4. Evaluate maturity, integration difficulty, priority, and risks using `references/quality-rubric.md`.
5. Decide whether to add it to the main hub, place it in watchlist, or reject it for now.
6. Write or update the relevant Markdown entry.
7. Update `INDEX.md` only when the item becomes a major entry or creates a new category.
8. Preserve dates and context for experience notes; append updates instead of overwriting old observations.

## Placement Rules

- Do not copy, vendor, or store the full target repository inside `chainsea-ai-hub`. Clone external repos only to a temporary analysis location, then keep only curated notes, links, metadata, templates, case studies, or experience records in the hub.
- Repos, frameworks, tools, MCP servers, and external platforms: `resources/repos/`.
- Agent skills, prompt workflows, reusable agent procedures: `resources/skills/`.
- Project outcomes and reusable internal success stories: `resources/cases/`.
- Time-aware engineering observations, experiments, and lessons learned: `resources/experiences/`.
- Interesting but unverified resources: `resources/watchlist.md`.
- Reusable entry formats: `templates/`.

## Storage Rules

- Keep `README.md`, `INDEX.md`, and category pages short and scannable.
- Use category pages as quick indexes, not long-form analysis pages.
- If an entry needs more than roughly 10-12 lines, create a detail page under a same-named subdirectory, such as `resources/repos/ai-agents/han-agents.md`.
- The category entry should link to the detail page through a `Details:` field.
- Put verification logs, long caveats, integration notes, and next-step plans in the detail page.
- Do not mirror or rewrite the original project's README. Store only the minimum context needed to support internal adoption judgment, classification, risk review, and maintenance.
- It is okay for the hub to grow, as long as growth happens in leaf pages instead of top-level indexes.

## Decision Rules

Add a resource to the main hub only when at least one is true:

- It solves a recurring engineering problem.
- It improves AI-assisted development workflow.
- It can be reused across projects.
- It is useful for testing, documentation, automation, or integration.
- It is an important reference for future internal experiments.

If the resource is promising but immature, add it to `resources/watchlist.md` with a recheck date. If it is not clearly useful, explain why and do not add it.

## Writing Rules

- Write primarily in Traditional Chinese.
- Keep necessary English technical terms when they are clearer than translation.
- Prefer practical notes over broad claims.
- Focus on internal judgment: why listed, not for, ChainSea value, risks, verification, and next step.
- Include `Last checked` for resources and dates for experience notes.
- Link to original docs for feature details instead of copying them.
- Avoid marketing language and vague adjectives.

For detailed style guidance, read `references/writing-style.md` when drafting longer entries.

## Templates

Use these templates when creating new entries:

- Resource cards: `assets/templates/resource-card.md`
- Case studies: `assets/templates/case-card.md`
- Experience notes: `assets/templates/experience-note.md`

The repo root also contains user-facing templates under `templates/`.

## Output Format

When asked to add or review a resource, return:

1. short summary
2. classification
3. recommended placement
4. maturity and risk assessment
5. Markdown entry or files changed
6. follow-up checks

When editing files directly, also report verification performed and remaining uncertainty.
