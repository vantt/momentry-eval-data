---
id: 2026-10-29-theo-doi-tien-trinh-dai-bang-c455
code: M-11G2
aliases: [M-11G2]
date: 2026-10-29
repo: repo
status: raw
signals: []
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:0faf0bb2#L1187", "claude:0faf0bb2#L1204", "claude:0faf0bb2#L1205", "claude:0faf0bb2#L3501", "claude:0faf0bb2#L3502", "claude:0faf0bb2#L3591", "claude:0faf0bb2#L3679", "claude:0faf0bb2#L3680"]
hook: "Việc chạy dài giao cho Monitor, agent khỏi ngồi chờ và poll"
tension: none
sides: []
strength: 0
stakes: 0
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Theo dõi tiến trình dài bằng Monitor thay vì để agent ngồi chờ hoặc poll liên tục

**Chuyện gì xảy ra:** Theo dõi tiến trình dài bằng Monitor thay vì để agent ngồi chờ hoặc poll liên tục
**Góc người ngoài:** cách làm phổ biến là Chạy lệnh chờ hoặc vòng lặp sleep rồi đợi timeout, hoặc hỏi lại trạng thái thủ công nhiều lần; ở đây khác ở Agent đăng ký một watcher báo khi trạng thái issue đổi (status, comment, run) và nhận thông báo từng sự kiện, không phải poll. Người đọc sẽ muốn biết cơ chế này để làm theo.
