---
name: hub-curator
description: Maintain chainsea-ai-hub, an internal AI engineering resource hub. Use when adding, reviewing, classifying, or updating repositories, tools, MCP servers, agent skills, AI workflows, templates, technical articles, development experience notes, or case studies in the hub.
---

# Hub Curator

## Overview

Use this skill to keep `chainsea-ai-hub` useful, current, and easy to maintain. The goal is to turn a resource link or rough note into a classified, practical, time-aware hub entry.

## Core Workflow

The skill has three distinct paths. Pick one based on the situation — do not mix.

### Path A — Quick Add (watchlist, default)

For resources without a concrete ChainSea adoption scenario. This is the default path.

1. Read the resource (gh api or quick scan).
2. Mentally classify via Categories.
3. Append a single-line entry to `resources/watchlist.md`:
   - Format: `- [name](link) — 一句 tagline。為什麼想看：reason。Added: YYYY-MM-DD`
   - Optional `⭐` prefix for high-signal resources (10k+ stars / major org / cross-tool standard)
   - Optional minimal `Note:` only to flag blockers (e.g., `Note: license unclear`) — flag only, do not evaluate
4. Done. Do not update INDEX.

### Path B — Promote (watchlist → adoption)

Triggered when a watchlist entry has matured into a concrete adoption scenario.

1. Confirm gateway: there is a real ChainSea use case, not "looks promising".
2. Run Path C steps 2-5.
3. Move any watchlist `Note:` content into the new detail page's Risks or Verification section.
4. Remove the original entry from `resources/watchlist.md`.

### Path C — Evaluate (direct adoption entry)

When user explicitly requests full evaluation, or the resource is already in ChainSea use.

1. Read the resource thoroughly. Clone to a tmp location if verification needs running code.
2. Classify via Categories.
3. Evaluate status, risks, and adoption blockers using `references/style.md`.
4. Write detail page using `templates/resource-card.md` schema.
5. Add index card to the category page (or create the page if ≥3 entries justify).
6. Update `INDEX.md` only when the item becomes a major entry or creates a new category.

### Time-Aware Notes (any path)

For experience notes, preserve dates and context; append updates instead of overwriting old observations.

## Placement Rules

- Do not copy, vendor, or store the full target repository inside `chainsea-ai-hub`. Clone external repos only to a temporary analysis location, then keep only curated notes, links, metadata, templates, case studies, or experience records in the hub.
- Repos, frameworks, tools, MCP servers, and external platforms: `resources/repos/`.
- Agent skills, prompt workflows, reusable agent procedures: `resources/skills/`.
- Project outcomes and reusable internal success stories: `resources/cases/`.
- Time-aware engineering observations, experiments, and lessons learned: `resources/experiences/`.
- Interesting but unverified resources: `resources/watchlist.md`.
- Reusable entry formats: `templates/`.

## Categories

- **AI Agents / Agent Skills**：agent framework、coding agent、multi-agent workflow、reusable agent skill
- **Testing & QA**：unit test、E2E、test generation、coverage、mutation testing、QA case
- **MCP / Tool Integration**：MCP server、Jira/GitLab/GitHub integration、browser automation、API wrapper
- **Documentation / PM**：PRD、meeting notes、technical doc、Jira ticket gen、planning workflow

Add new categories only when ≥3 entries justify the split. Do not pre-create empty categories.

這條規則只適用於 `resources/repos/` 下的 **taxonomy categories**。`resources/cases/`、`resources/experiences/`、`resources/skills/`、`resources/watchlist.md` 是 **top-level libraries**，是 hub 的核心資源類型，不受 ≥3 entries 規則限制，即使空也應保留 landing 頁。

## Storage Rules

- Keep `README.md`, `INDEX.md`, and category pages short and scannable.
- Use category pages as quick indexes, not long-form analysis pages.
- If an entry needs more than roughly 10-12 lines, create a detail page under a same-named subdirectory, such as `resources/repos/ai-agents/han-agents.md`.
- The category entry should link to the detail page through a `Details:` field.
- Put verification logs, long caveats, integration notes, and next-step plans in the detail page.
- Do not mirror or rewrite the original project's README. Store only the minimum context needed to support internal adoption judgment, classification, risk review, and maintenance.
- It is okay for the hub to grow, as long as growth happens in leaf pages instead of top-level indexes.

## Decision Rules

Use Path C (full adoption) only when the resource has a concrete ChainSea use case — currently in use, actively being evaluated, or scheduled for a specific upcoming project.

If the resource is interesting but has no concrete use case yet, default to Path A (watchlist quick add). Watchlist entries are reviewed monthly (see Review Cadence).

Reject the resource only when the use case is unclear, the project is abandoned, or risk clearly outweighs expected benefit.

## Review Cadence

- Production-used / 高頻使用：每 1-2 月檢查一次。
- Useful / Experimental：每季檢查一次。
- Watchlist：每月 review 一次。

Watchlist 月度 review 時，對每條目判斷：
- **Promote**：條目已成熟 / 有具體 use case → 走 Path B
- **Keep**：仍值得觀察 → 不動，可更新 Added 日期或 Note
- **Drop**：專案停更 / 不再相關 → 刪除

- Deprecated：只在有人詢問時才重新評估。

Experience notes preserve chronology; append to Later Updates, never overwrite.

## Writing Rules

- Write primarily in Traditional Chinese.
- Keep necessary English technical terms when they are clearer than translation.
- Prefer practical notes over broad claims.
- Focus on internal judgment: why listed, not for, ChainSea value, risks, verification, and next step.
- Include `Last checked` for resources and dates for experience notes.
- Link to original docs for feature details instead of copying them.
- Avoid marketing language and vague adjectives.

For detailed style guidance, read `references/style.md` when drafting longer entries.

## Templates

Use these templates when creating new entries:

- Resource cards: `../../../templates/resource-card.md`
- Case studies: `../../../templates/case-study-template.md`
- Experience notes: `../../../templates/experience-note-template.md`

## Output Format

When asked to add or review a resource, return:

1. short summary
2. classification
3. recommended placement
4. status and risks
5. Markdown entry or files changed
6. follow-up checks

When editing files directly, also report verification performed and remaining uncertainty.
