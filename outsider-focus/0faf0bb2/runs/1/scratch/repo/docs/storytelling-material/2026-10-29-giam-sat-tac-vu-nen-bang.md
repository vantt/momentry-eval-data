---
id: 2026-10-29-giam-sat-tac-vu-nen-bang
date: 2026-10-29
repo: repo
status: raw
signals: []
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:0faf0bb2#L1187", "claude:0faf0bb2#L1204", "claude:0faf0bb2#L1305", "claude:0faf0bb2#L3032", "claude:0faf0bb2#L3501", "claude:0faf0bb2#L3591", "claude:0faf0bb2#L3679"]
hook: "Thay vòng sleep và curl bằng Monitor, agent viết runbook trong lúc chờ"
tension: none
sides: []
strength: 1
stakes: 0
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Giám sát tác vụ nền bằng Monitor: viết vòng lặp theo dõi trạng thái issue và số comment, mỗi lần đổi thì phát sự kiện đánh thức agent, trong lúc đó agent làm việc khác (viết runbook, chuẩn bị test kế tiếp). Không sleep hay polling thủ công.

**Chuyện gì xảy ra:** Giám sát tác vụ nền bằng Monitor: viết vòng lặp theo dõi trạng thái issue và số comment, mỗi lần đổi thì phát sự kiện đánh thức agent, trong lúc đó agent làm việc khác (viết runbook, chuẩn bị test kế tiếp). Không sleep hay polling thủ công.
**Góc người ngoài:** cách làm phổ biến là Dev thường sleep rồi curl lại nhiều lần, hoặc ngồi xem log, hoặc chạy lệnh chờ trong một terminal khác; ở đây khác ở Một vòng lặp chạy nền có timeout và báo sự kiện cho phép AI vừa chờ agent khác làm việc hàng chục phút vừa tiếp tục việc có ích. Người đọc đang dùng AI hằng ngày sẽ muốn mẫu này cho các tác vụ chạy lâu.
