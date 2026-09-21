# OpsAI Kandev 本機設定紀錄

日期：2026-09-21（Asia/Taipei）

## 安裝

- Repository：`https://github.com/kdlbs/kandev.git`
- Local checkout：`/Users/opsai/Documents/sp1050107-zbot/kandev`
- Revision：`db8131436fe06482c883a9027d95e5888ae4658d`
- npm runtime：`kandev@0.95.0`
- License：AGPL-3.0-only

## 啟動

```bash
KANDEV_SERVER_HOST=127.0.0.1 \
  npx --yes kandev@0.95.0 run --port 8091 --headless
```

服務網址：`http://127.0.0.1:8091`

MCP endpoint：`http://127.0.0.1:8091/mcp`

資料庫：`/Users/opsai/.kandev/data/kandev.db`

## 驗證

- backend ready：PASS
- SQLite initialization：PASS
- agentctl bootstrap：PASS
- standalone、Docker、remote Docker、Sprites、SSH、K8s runtime registration：PASS（實際可用性仍須逐項測試）
- Claude／Codex ACP profiles：已建立預設設定
- taskctl integration：未啟用，刻意保持獨立

## 安全注意

Kandev 預設 authentication 關閉；本次以 `KANDEV_SERVER_HOST=127.0.0.1` 限制為本機，沒有對外開放。若要讓其他裝置或其他使用者連線，必須先啟用 Kandev authentication、TLS／反向代理與明確的使用者權限。
