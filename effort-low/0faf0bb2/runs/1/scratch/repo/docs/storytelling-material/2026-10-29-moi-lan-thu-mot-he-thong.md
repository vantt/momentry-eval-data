---
id: 2026-10-29-moi-lan-thu-mot-he-thong
date: 2026-10-29
repo: repo
status: raw
signals: []
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:0faf0bb2#L2134", "claude:0faf0bb2#L2138", "claude:0faf0bb2#L2452", "claude:0faf0bb2#L2491", "claude:0faf0bb2#L2616", "claude:0faf0bb2#L3188", "claude:0faf0bb2#L3474", "claude:0faf0bb2#L3723"]
hook: "Thử xong một hệ thống, agent để lại runbook và bảng hoàn tác để dọn sạch máy"
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

# Mỗi lần thử một hệ thống (spike), agent ghi lại đầy đủ runbook có script đăng nhập không lưu bí mật, kèm bảng hoàn tác, để có thể dựng lại hoặc dọn sạch.

**Chuyện gì xảy ra:** Mỗi lần thử một hệ thống (spike), agent ghi lại đầy đủ runbook có script đăng nhập không lưu bí mật, kèm bảng hoàn tác, để có thể dựng lại hoặc dọn sạch.
**Góc người ngoài:** cách làm phổ biến là Phần lớn dev chỉ ghi chú vài dòng hoặc không ghi gì, rồi quên các bước đã làm và không dọn sạch được máy; ở đây khác ở Người đọc sẽ muốn biết cách làm runbook tái lập được và cách dọn sạch an toàn, đặc biệt là việc đọc token từ tiến trình thay vì ghi vào file.
