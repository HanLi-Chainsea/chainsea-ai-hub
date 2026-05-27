# HAN-Agents

## Index Judgment

- Status: Useful
- Category: AI Agents
- Secondary categories: Agent Skills, Testing & QA, LLM Evaluation
- Best for: 長任務拆解、agent review loop、local memory / task state、skill-code drift 檢查。
- Why listed: 它把 AI coding workflow 產品化成可安裝 skill + local state system，值得作為 ChainSea 內部 agent workflow 與 hub 自我維護設計的參考樣板。
- Not for: 高敏感 repo、嚴格受控 CI、不能接受本機 SQLite / hook / optional install 副作用的環境。
- Link: https://github.com/HanLi-Chainsea/han-agents

## ChainSea Value

它的價值不在單一 API 或 feature list，而在「把多 agent 工作流、memory、code graph、critic loop 包成可複用 skill」。這對 `chainsea-ai-hub` 有兩層參考價值：

- 作為內部 agent workflow registry 的外部案例。
- 作為未來整理 unit test generation / review loop / long-running task workflow 的候選工具。

## Risks

- README 安裝範例仍指向 `Stanley-1013/han-agents`，本次收錄來源是 `HanLi-Chainsea/han-agents`；導入文件時需統一 remote URL。
- README 標示 MIT，但 inspected clone 未看到獨立 `LICENSE` 檔；正式採用前要確認授權來源。
- Auto setup / hooks / optional tree-sitter install 會改動本機環境，團隊導入前需先 sandbox。
- Claude Code 以外平台主要是 sequential / shared-context 模式，multi-agent 隔離程度需實測。

## Verification

- Last checked: 2026-05-20
- Commit inspected: `b837bd0b9cfe5c9ff0abe9353f2fa5ad9cf8b9b3` (2026-05-06)
- `python scripts/doctor.py`: 6 OK, 1 warning, 0 errors
- Warning: Code Graph empty; repo suggested running sync
- Full test suite: Not run

## Next Step

在非敏感 demo repo 中安裝並測 `recipe_unit_tests()`。若確實能降低 unit test 補齊與 review loop 的人工操作量，再升級成 `resources/experiences/` 試用紀錄或 `resources/cases/` 案例。
