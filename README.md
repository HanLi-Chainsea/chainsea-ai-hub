# ChainSea AI Hub

`chainsea-ai-hub` 是 ChainSea 內部的 AI engineering resource hub，用來整理可複用的 AI workflow、agent skill、open-source repo、MCP 工具、測試自動化方法與實際案例。

這個 hub 的重點不是收藏連結，而是建立一套可持續維護的 **AI-assisted internal knowledge operations infrastructure**：工程師只要提供 repo、工具、文章、workflow 或案例，agent 就能協助分析、分類、撰寫文件並更新索引。

## 核心定位

- **資源索引**：快速找到適合目前情境的 repo、工具、MCP server、模板或 workflow。
- **Skill registry**：保存可被 AI agent 直接使用或改寫的內部技能。
- **開發經驗庫**：記錄實際專案中的使用經驗、時間痕跡、決策背景與後續迭代。
- **案例庫**：把零散實驗整理成可向團隊說明的成果案例。
- **Hub curator skill**：內建維護 skill，讓 agent 可以協助新增、分類、評估與更新內容。

## 快速入口

- [INDEX.md](INDEX.md)：總索引與分類入口。
- [resources/repos/](resources/repos)：repo、工具與平台資源。
- [resources/skills/](resources/skills)：agent skill 與可複用工作流。
- [resources/cases/](resources/cases)：實際案例與成果摘要。
- [resources/experiences/](resources/experiences)：開發經驗、時間脈絡與迭代紀錄。
- [resources/watchlist.md](resources/watchlist.md)：看起來有潛力但尚未驗證的資源。
- [.claude/skills/hub-curator/SKILL.md](.claude/skills/hub-curator/SKILL.md)：用來維護本 hub 的 agent skill（clone 後自動註冊為 `/hub-curator`）。

## 建議使用方式

Claude Code 使用者 clone 這個 repo 後，內建 skill 會從 `.claude/skills/hub-curator/` 自動註冊為 `/hub-curator`。新增資源時，優先使用：

```txt
/hub-curator add this repo:
https://github.com/example/project
```

如果使用的工具尚未支援 `.claude/skills/`，請閱讀 [AGENTS.md](AGENTS.md)；它會指向同一份 skill 與手動註冊方式。

期望輸出：

1. 資源摘要
2. 分類與標籤
3. ChainSea 適用情境
4. 成熟度與風險
5. 建議放置位置
6. Markdown 條目
7. 需要更新的檔案

## 第一版範圍

第一版先聚焦五個方向：

1. Testing & QA
2. Jira / GitLab / MCP automation
3. Agent skills
4. E2E / QA test case generation
5. Research / crawling / knowledge gathering

每個分類先維持少量、高品質、可說明用途的條目。看起來有趣但還沒有實際驗證的資源，先放進 watchlist。

## Skill 相容性策略

- Claude Code：使用 `.claude/skills/hub-curator/`，clone 後可自動註冊。
- Codex CLI：本環境已用 `~/.codex/skills/hub-curator` symlink 到 `.claude/skills/hub-curator/` 驗證可用；是否支援 repo-local `.codex/skills/` 仍不在本 hub 假設內。
- Cursor / Cline / Continue / Roo Code：格式與載入路徑不同時，先透過 [AGENTS.md](AGENTS.md) 取得 fallback 指令，再視工具建立 pointer / rules 檔。

目前以 `.claude/skills/hub-curator/` 作為「可自動註冊的內建 skill 來源」。不要額外維護第二份 skill 內容，避免 drift。
