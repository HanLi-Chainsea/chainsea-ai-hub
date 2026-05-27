# Skill Registry

這裡記錄 ChainSea 內部可複用的 agent skills、prompt workflows、操作手冊與可被其他工程師拿去改寫的任務流程。

## Built-in Skills

### Hub Curator

- Status: Experimental
- Category: Documentation / Knowledge Operations
- Best for: 分析 repo、工具、workflow 或案例，並更新 `chainsea-ai-hub`
- Why listed: 目前唯一維護 hub 自身索引與資源卡的內部 skill，統一分類判斷邏輯。
- Not for: 非 hub 相關的研究任務；不應被複製成第二份 skill。
- Link: [.claude/skills/hub-curator/SKILL.md](../../.claude/skills/hub-curator/SKILL.md)
- Invocation: clone repo 後直接使用 `/hub-curator`（Claude Code 會從 `.claude/skills/` 自動註冊）
- Compatibility note: `.claude/skills/hub-curator/` 是唯一維護來源；其他工具應用 symlink、pointer file 或 [AGENTS.md](../../AGENTS.md) 轉接，不要複製第二份 skill。

## Planned Skills

- Unit test agent
- Jira / GitLab automation assistant
- E2E test case generator
- PRD review workflow
- Research / crawling curator

## External / Candidate Skills

### HAN-Agents

- Status: Useful
- Category: AI Agents / Agent Skills
- Best for: 長任務拆解、agent review loop、local memory / task state、skill-code drift 檢查。
- Why listed: 外部多 agent skill 樣板，候選用於 unit test generation / review loop / long-running task workflow。
- Not for: 高敏感 repo、嚴格受控 CI、不能接受本機 SQLite / hook 副作用的環境。
- Main entry: [HAN-Agents](../repos/ai-agents.md#han-agents)
- Link: https://github.com/HanLi-Chainsea/han-agents
