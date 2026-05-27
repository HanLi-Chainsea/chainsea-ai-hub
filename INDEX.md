# ChainSea AI Hub Index

這份索引用來讓工程師快速判斷「現在的任務該看哪裡」。每個正式收錄的資源都應該包含用途、輸入、輸出、成熟度、限制與最後檢查時間。

## 兩種層別

- **Adoption 層**：Repos / Skills / Cases / Experiences —— 完整判斷 schema，做技術選型用
- **Discovery 層**：Watchlist —— 一行 entry，低門檻 stash

## Resource Repos

- [AI Agents](resources/repos/ai-agents.md)：agent framework、multi-agent workflow、coding agent 工具。
- [Testing & QA](resources/repos/testing-qa.md)：unit test、E2E、QA case、coverage、mutation testing。
- [MCP & Tool Integration](resources/repos/mcp-tools.md)：MCP server、Jira/GitLab/GitHub/API 整合。
- [Documentation & PM](resources/repos/documentation.md)：PRD、文件、會議紀錄、需求整理與知識管理。

## Skills

- [Skill Registry](resources/skills/skill-registry.md)：內部 skill、prompt workflow、agent 操作手冊。
- [Hub Curator](.claude/skills/hub-curator/SKILL.md)：維護本 hub 的內建 skill（clone 後 Claude Code 會自動註冊為 `/hub-curator`）。
- [AGENTS.md](AGENTS.md)：給不支援 `.claude/skills/` 的工具使用的 fallback 入口。

## Case Library

- [Case Library](resources/cases/README.md)：已被實際專案驗證或可對內分享的成果案例。

## Experience Library

- [Development Experience Notes](resources/experiences/README.md)：保留時間痕跡的開發經驗紀錄。

## Governance

- [Watchlist](resources/watchlist.md)：awesome 風格 discovery 層 —— 一行 entry、月度 review。
- [Contributing](CONTRIBUTING.md)：新增或更新內容時的格式與品質規則。
- [Templates](templates)：resource、skill、case、experience note 的模板。
