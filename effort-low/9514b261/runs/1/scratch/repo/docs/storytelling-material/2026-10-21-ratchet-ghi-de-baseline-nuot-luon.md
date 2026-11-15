---
id: 2026-10-21-ratchet-ghi-de-baseline-nuot-luon
date: 2026-10-21
repo: repo
status: raw
signals: [số trước/sau, ràng buộc định hình thiết kế]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L95", "claude:9514b261#L282"]
hook: "Lệnh ghi baseline biến mọi lỗi mới thành 'đã biết'"
tension: giup_ma_hai
sides: ["Baseline 374 mục có để chặn vi phạm mới", "Chạy lại --write-baseline thì vi phạm mới được nuốt luôn, không báo"]
strength: 3
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Ratchet ghi đè baseline nuốt luôn vi phạm mới

**Bối cảnh:** Một hệ kiểm kiến trúc dùng file baseline để chỉ chặn vi phạm mới, nợ cũ được chấp nhận. Lệnh ghi lại baseline lại ghi đè vô điều kiện.
**Chuyện gì xảy ra:** Hai script kiểm quyết định đều có lệnh --write-baseline ghi đè baseline mà không so với bản cũ. Ai chạy lại lệnh đó thì mọi vi phạm mới thành 'đã biết' mà không báo. Baseline hiện có 374 mục.
**Bài học:** Lệnh ghi baseline phải so với bản cũ và từ chối khi số mục tăng; muốn tăng phải có cờ tường minh.
**Artefact:** Bảng so sánh baseline trước/sau khi chạy lệnh ghi, chỉ hiện số mục, không có nội dung file.
