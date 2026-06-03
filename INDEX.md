# ChainSea AI Hub Index

這份索引用來讓工程師快速判斷「現在的任務該看哪裡」。正式條目使用 [templates/resource-card.md](templates/resource-card.md) 的判斷導向 schema（Why listed / ChainSea Value / Risks / Verification / Next Step）。

## 兩種層別

- **Adoption 層**：Repos / Skills / Cases / Experiences —— 完整判斷 schema，做技術選型用
- **Discovery 層**：Watchlist —— 一行 entry，低門檻 stash

## Resource Repos

- [AI Agents](resources/repos/ai-agents.md)：agent framework、multi-agent workflow、coding agent 工具。

其他分類（Testing & QA / MCP & Tool Integration / Documentation / PM）在累積 ≥3 entries 時才開設專頁；現在新資源預設進 [Watchlist](resources/watchlist.md)。完整 taxonomy 見 [hub-curator SKILL.md](.claude/skills/hub-curator/SKILL.md)。

## Skills

- [Skill Registry](resources/skills/skill-registry.md)：內部 skill、prompt workflow、agent 操作手冊。
- [Hub Curator](.claude/skills/hub-curator/SKILL.md)：維護本 hub 的內建 skill（clone 後 Claude Code 會自動註冊為 `/hub-curator`）。
- [AGENTS.md](AGENTS.md)：給不支援 `.claude/skills/` 的工具使用的 fallback 入口。

## Case Library

- [Case Library](resources/cases/README.md)：已被實際專案驗證或可對內分享的成果案例（目前無條目）。

## Experience Library

- [Development Experience Notes](resources/experiences/README.md)：保留時間痕跡的開發經驗紀錄（目前無條目）。

## Governance

- [Watchlist](resources/watchlist.md)：awesome 風格 discovery 層 —— 一行 entry、月度 review。
- [Templates](templates)：resource、case、experience note 的模板。
