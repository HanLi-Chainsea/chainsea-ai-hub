---
name: hub-curator
description: Maintain chainsea-ai-hub, an internal AI engineering resource hub. Use when adding, reviewing, classifying, or updating repositories, tools, MCP servers, agent skills, AI workflows, templates, technical articles, development experience notes, or case studies in the hub.
---

# Hub Curator

## Overview

Use this skill to keep `chainsea-ai-hub` useful, current, and easy to maintain. The goal is to turn a resource link or rough note into a classified, practical, time-aware hub entry.

## Core Workflow

1. Determine whether this belongs in watchlist (default) or main hub (see Watchlist Workflow).
2. Identify what problem it solves and who should use it.
3. Classify it using the Categories below.
4. Evaluate status, risks, and adoption blockers using `references/style.md`.
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

## Categories

- **AI Agents / Agent Skills**：agent framework、coding agent、multi-agent workflow、reusable agent skill
- **Testing & QA**：unit test、E2E、test generation、coverage、mutation testing、QA case
- **MCP / Tool Integration**：MCP server、Jira/GitLab/GitHub integration、browser automation、API wrapper
- **Documentation / PM**：PRD、meeting notes、technical doc、Jira ticket gen、planning workflow

Add new categories only when ≥3 entries justify the split. Do not pre-create empty categories.

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

## Watchlist Workflow

`resources/watchlist.md` 是 awesome-style discovery 層，跟 main hub 是不同產品。

### When to use watchlist instead of main hub

預設丟 watchlist，除非滿足以下任一：
- 使用者明確說要做完整評估
- 已是 ChainSea 內部正在用或評估中的工具
- 已有具體採用情境（不是「看起來有用」）

### Watchlist entry format

一行：`- [name](link) — 一句 tagline。為什麼想看：reason。Added: YYYY-MM-DD`

不要在 watchlist 寫完整判斷、風險、驗證 —— 那是 promotion 後的事。

### Monthly review

當被要求 review watchlist，對每條目判斷：
- **Promote**：條目已成熟 / 有具體 use case → 移到 `resources/repos/<category>/<name>.md` 完整 detail page，從 watchlist 刪除
- **Keep**：仍值得觀察 → 不動，但更新 Added 日期或加 note
- **Drop**：專案停更 / 不再相關 → 刪除

### Promotion 時要做什麼

從 watchlist 移到 main hub 時：
1. 確認 detail page 用 `templates/resource-card.md` 完整 schema
2. 真的做 verification（不是抄 watchlist 的 reason）
3. 在類別頁 entries 區加索引卡
4. 從 watchlist.md 移除原條目

## Review Cadence

- Production-used / 高頻使用：每 1-2 月檢查一次。
- Useful / Experimental：每季檢查一次。
- Watchlist：每月 review 一次（見 Watchlist Workflow）。
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