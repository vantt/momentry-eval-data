---
id: 2026-11-02-chay-claude-code-headless-voi-config-3c6e
code: M-QDT4
aliases: [M-QDT4]
date: 2026-11-02
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L1545"]
hook: "Chạy thử 10 tool MCP bằng config tạm, không đụng config thật"
tension: none
sides: []
strength: 0
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Chạy Claude Code headless với config MCP tạm, không đụng config thật

**Bối cảnh:** Cần kiểm tool MCP được gọi thật từ Claude Code mà không làm hỏng cấu hình người dùng.
**Chuyện gì xảy ra:** Agent chạy headless với --mcp-config tạm và --strict-mcp-config. Mười tool, trừ related, chạy đúng trên bản copy của kg-solo, kể cả khi wrong id trả về did_you_mean và more chạy qua một lần tự rebuild. Log và câu trả lời được lưu vào báo cáo.
**Bài học:** Kiểm tích hợp thật bằng cấu hình tạm, để không phải đoán và không rủi ro với môi trường thật.
**Artefact:** Trích log server và câu trả lời của Claude (che đường dẫn vault).
