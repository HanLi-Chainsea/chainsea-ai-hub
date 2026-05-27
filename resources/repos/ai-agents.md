# AI Agents

Agent framework、coding agent、multi-agent workflow 與 AI-assisted engineering 工具。

## 收錄格式

```md
### Resource Name

- Status: Experimental / Useful / Production-used / Deprecated
- Category:
- Best for:
- Why listed:
- Not for:
- Last checked:
- Details:
- Link:
```

## Entries

### HAN-Agents

- Status: Useful
- Category: AI Agents
- Best for: 長任務拆解、agent review loop、local memory / task state、skill-code drift 檢查。
- Why listed: 把多 agent 工作流、memory、code graph、critic loop 包成可複用 skill，是 ChainSea 內部 agent workflow 設計的外部參考樣板。
- Not for: 高敏感 repo、嚴格受控 CI、不能接受本機 SQLite / hook 副作用的環境。
- Last checked: 2026-05-20
- Details: [ai-agents/han-agents.md](ai-agents/han-agents.md)
- Link: https://github.com/HanLi-Chainsea/han-agents
