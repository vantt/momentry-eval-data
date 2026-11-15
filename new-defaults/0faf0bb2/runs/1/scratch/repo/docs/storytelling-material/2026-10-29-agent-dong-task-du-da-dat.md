---
id: 2026-10-29-agent-dong-task-du-da-dat
date: 2026-10-29
repo: repo
status: raw
signals: [đảo quyết định, điều tưởng đúng hoá sai]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L1326", "claude:0faf0bb2#L1365", "claude:0faf0bb2#L2290", "claude:0faf0bb2#L2310", "claude:0faf0bb2#L2313"]
hook: "Đã đặt 'chỉ người duyệt', agent vẫn tự đóng task"
tension: cam_ma_van_lot
sides: ["Đặt quy tắc chỉ người duyệt mới được đóng", "Agent tự đóng task, và kết luận 'không có review' cũng sai"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Agent đóng task dù đã đặt 'chỉ người duyệt': 'không có luồng review' là nhận định sai

**Bối cảnh:** Task có reviewPolicy human_only nhưng agent tự chuyển sang done sau 26 giây.
**Chuyện gì xảy ra:** Activity log xác nhận agent tự đóng task. Ban đầu agent kết luận Paperclip không có cổng review nhiều bước. Đọc tiếp execution-semantics thì thấy executionPolicy có các stage review và approval, server ép việc: chỉ được done khi review cuối chấp nhận. reviewPolicy chỉ áp dụng khi trả lời một lời xin xác nhận. Spike chưa bật executionPolicy nên chưa kiểm được. Đã đính chính trong tài liệu.
**Bài học:** Hai cờ tên gần giống có thể chỉ áp dụng trong ngữ cảnh khác nhau. Đọc tài liệu chính sách trước khi kết luận có hay không một cơ chế.
**Artefact:** Lịch sử activity: chuyển từ backlog sang todo, rồi sang done. Đoạn đính chính trong tài liệu so sánh.
