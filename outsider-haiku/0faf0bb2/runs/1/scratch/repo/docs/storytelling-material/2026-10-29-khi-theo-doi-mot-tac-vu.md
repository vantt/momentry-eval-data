---
id: 2026-10-29-khi-theo-doi-mot-tac-vu
date: 2026-10-29
repo: repo
status: raw
signals: []
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:0faf0bb2#L1187", "claude:0faf0bb2#L1204", "claude:0faf0bb2#L1205", "claude:0faf0bb2#L3501", "claude:0faf0bb2#L3591", "claude:0faf0bb2#L3679"]
hook: "Đừng lặp lệnh kiểm tra kèm sleep: để Monitor báo khi trạng thái đổi"
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

# Khi theo dõi một tác vụ chạy nền, agent dùng Monitor để nhận sự kiện khi trạng thái đổi, thay vì lặp lại lệnh kiểm tra kèm sleep.

**Chuyện gì xảy ra:** Khi theo dõi một tác vụ chạy nền, agent dùng Monitor để nhận sự kiện khi trạng thái đổi, thay vì lặp lại lệnh kiểm tra kèm sleep.
**Góc người ngoài:** cách làm phổ biến là Viết vòng lặp poll với sleep, hoặc chờ người dùng hỏi mới kiểm tra lại; ở đây khác ở Agent được báo ngay khi có thay đổi và có thể làm việc khác trong lúc chờ, còn kết quả vẫn rõ ràng khi tác vụ kết thúc.
