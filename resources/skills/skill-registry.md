# Skill Registry

這裡記錄 ChainSea 內部可複用的 agent skills、prompt workflows、操作手冊與可被其他工程師拿去改寫的任務流程。

## Built-in Skills

### Hub Curator

- Type: Internal Skill
- Category: Documentation / Knowledge Operations
- Best for: 分析 repo、工具、workflow 或案例，並更新 `chainsea-ai-hub`
- Inputs needed: resource link、簡短背景、使用目的或內部案例
- Outputs: classification、resource card、建議放置位置、索引更新
- Maturity: Experimental
- Integration difficulty: Low
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

- Type: External Skill / Multi-agent Workflow System
- Category: AI Agents / Agent Skills
- Best for: 將長任務拆成 PFC、Executor、Critic、Memory 流程，並結合 code graph、semantic memory、drift detection 與 local eval harness。
- Maturity: Useful
- Integration difficulty: Medium
- Main entry: [HAN-Agents](../repos/ai-agents.md#han-agents)
- Link: https://github.com/HanLi-Chainsea/han-agents
