# HAN-Agents

## Basic Info

- Type: Python-based multi-agent task orchestration skill / local agent support library
- Category: AI Agents
- Secondary categories: MCP / Tool Integration, Testing & QA, LLM Evaluation, Development Experience
- Tags: `agent`, `workflow`, `testing`, `evaluation`, `python`, `sqlite`
- Link: https://github.com/HanLi-Chainsea/han-agents
- License: README badge / section says MIT; no standalone `LICENSE` file observed in the inspected clone.
- Last checked: 2026-05-20

## Summary

HAN-Agents 把一套可重複的 coding-agent 工作流包成 skill：以 `SKILL.md` 作為 intent layer，搭配 `servers/` API、SQLite memory / tasks、AST code graph、drift detector、guardrails、review queue、trace / eval harness。

核心 API 包含 `ensure_project()`、`recipe_unit_tests()`、`get_next_dispatch()`、`check_drift()`、`search_memory_semantic()` 與 local trace evaluation。

## Best Use Cases

- 任務需要跨多回合維持狀態。
- 同一類工程流程想標準化，例如 unit test generation + critic review loop。
- 需要保存 implementation lesson，之後用 semantic memory 搜尋。
- 想檢查 skill definition 與實際 code implementation 的 drift。

## Inputs

- 專案路徑。
- 專案名稱。
- 要執行的 task 或 recipe。
- 若使用 enhanced code graph，可能需要 tree-sitter grammar。
- 若在 Claude Code 使用 hook / Task tool，需允許對本機 skill、agent、hook 目錄寫入。

## Outputs

- SQLite `brain.db` 中的 task / memory / graph / trace 資料。
- Agent dispatch instructions。
- Code graph / drift report。
- Unit-test recipe task tree。
- Guardrail / review queue / eval 結果。

## ChainSea Fit

適合熟悉 agent workflow、願意把任務狀態交給本地 SQLite 與 hooks 管理的 AI-assisted engineering 使用者。優先給 Claude Code / Codex CLI 類型工具評估。

它不是一般聊天 prompt；需要把 repo clone 到 AI tool 的 skills 目錄，並讓 Python 模組讀寫本地資料庫。

## Risks / Caveats

- README badge / 文字標示 MIT，但 clone 後未看到獨立 `LICENSE` 檔；正式採用前要確認授權來源。
- README 安裝範例仍指向 `Stanley-1013/han-agents`，本次資源連結是 `HanLi-Chainsea/han-agents`；導入文件時需統一 remote URL。
- `requirements.txt` 註明 core stdlib only；enhanced code extraction 的 tree-sitter 套件列在 `requirements-ast.txt`。實際部署前要確認是否允許首次使用時按需安裝 optional grammars。
- Auto hook / auto install 對本機環境有副作用，應先在 sandbox repo 跑 `python scripts/doctor.py` 與 `python cli/main.py eval`。
- 多平台相容性文件很完整，但 Claude Code 以外的平台主要是 sequential / shared-context 模式，multi-agent 隔離程度需實測。
- 不建議直接套用在高敏感 repo 或嚴格受控 CI 環境，除非先設定 `HAN_NO_INSTALL=1` 或審查 auto-setup 行為。

## Maturity

- Status: Useful
- Integration difficulty: Medium
- Recommended priority: Medium

## Verification

- Clone checked from `https://github.com/HanLi-Chainsea/han-agents` on 2026-05-20.
- Latest commit inspected: `b837bd0b9cfe5c9ff0abe9353f2fa5ad9cf8b9b3` (2026-05-06, `Update Traditional Chinese README`).
- Ran `python scripts/doctor.py` in the cloned repo: 6 OK, 1 warning, 0 errors. The warning was an empty Code Graph with suggested sync command.
- Confirmed `pytest` is available locally (`pytest 9.0.3`), but did not run the full test suite for this hub entry.

## Recommended Next Step

在一個非敏感 demo repo 中安裝，跑 `doctor`、`eval`、`recipe_unit_tests()`，記錄是否真的能降低 unit test 補齊與 review loop 的人工操作量；若通過，再整理成 `resources/experiences/` 的內部試用紀錄。
