# OpsAI Kandev 評估與啟動需求

日期：2026-09-21（Asia/Taipei）

## 目的

在不接入 `taskctl`、不改寫 `macbook-local-llm` 真相來源的前提下，獨立體驗 Kandev 作為多 agent 開發工作流與超級助理執行面的能力。

## 範圍

- 本機啟動 Kandev 0.95.0 runtime bundle。
- 使用 Kandev 自己的 SQLite：`~/.kandev/data/kandev.db`。
- 只綁定 `127.0.0.1:8091`。
- 先使用獨立工作區與獨立 Kandev 任務，不匯入 taskctl／roadmap 投影卡片。
- 評估 Claude、Codex、多 agent workflow、worktree、review、MCP 與人工介入流程。

## 非範圍

- 不停止、刪除或修改 `macbook-local-llm` 的未提交變更。
- 不把 Kandev 狀態寫回 `docs/state/tasks/events.jsonl`。
- 不自動啟動外部寫入、GitHub PR、訊息發送或敏感 connector。

## 驗收條件

- `http://127.0.0.1:8091` 可開啟且 health probe 正常。
- Kandev 使用獨立 SQLite，不依賴 ai-agent-board PostgreSQL。
- 可建立一個本機測試任務，選擇 Claude 或 Codex，查看工作流與事件。
- 可辨識 task、agent session、worktree、review、merge 的生命週期。
- 完成後留下 Kandev 版本、啟動命令、資料路徑、風險與下一步評估紀錄。
