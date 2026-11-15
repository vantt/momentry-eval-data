---
id: 2026-11-01-bot-khong-push-duoc-la-do
date: 2026-11-01
repo: repo
status: raw
signals: ["5", "3"]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L3327", "claude:f0bf048d#L3333", "claude:f0bf048d#L3340"]
hook: "Bot có quyền ghi thì hook pre-push bị --no-verify bỏ qua"
tension: cam_ma_van_lot
sides: ["Hook pre-push được dựng để chặn push bậy", "Một cờ --no-verify là qua, nên chỉ còn deploy key đọc"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Bot không push được là do quyền GitHub, không phải lời dặn

**Bối cảnh:** System Operator cần đưa thay đổi của nó về repo chung.
**Chuyện gì xảy ra:** Người dùng hỏi vì sao không push. Lý do: repo private của tài khoản free không bảo vệ được main, và bot có quyền ghi thì hook pre-push vẫn bị qua bằng --no-verify. Chọn deploy key chỉ đọc; thay đổi của bot đi qua nhánh ops/ và người duyệt fetch về.
**Bài học:** Giới hạn hành vi agent bằng quyền truy cập, không bằng lời dặn trong prompt.
