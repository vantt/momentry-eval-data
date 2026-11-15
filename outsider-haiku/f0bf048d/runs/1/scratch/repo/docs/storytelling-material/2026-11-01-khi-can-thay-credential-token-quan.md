---
id: 2026-11-01-khi-can-thay-credential-token-quan
date: 2026-11-01
repo: repo
status: raw
signals: []
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:f0bf048d#L2536", "claude:f0bf048d#L2543", "claude:f0bf048d#L2548", "claude:f0bf048d#L2549", "claude:f0bf048d#L2550"]
hook: "Thay token quản trị: tạo mới, kiểm tra, rồi mới thu hồi bản cũ"
tension: none
sides: []
strength: 0
stakes: 2
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Khi cần thay credential (token quản trị), agent tạo token mới, kiểm token mới hoạt động, rồi mới thu hồi token cũ. Trước đó nó tìm toàn bộ bản sao của token cũ trong home người dùng bằng cách grep nội dung, nên không sót chỗ nào.

**Chuyện gì xảy ra:** Khi cần thay credential (token quản trị), agent tạo token mới, kiểm token mới hoạt động, rồi mới thu hồi token cũ. Trước đó nó tìm toàn bộ bản sao của token cũ trong home người dùng bằng cách grep nội dung, nên không sót chỗ nào.
**Góc người ngoài:** cách làm phổ biến là Thu hồi token cũ trước rồi mới nhớ ra có vài nơi còn đang dùng nó, hoặc không tìm hết các bản sao; ở đây khác ở Trình tự 'tạo mới, kiểm, thu hồi, và tìm hết bản sao' là cách xoay vòng credential có kiểm chứng. Người đọc muốn biết cách làm đó để không làm gián đoạn dịch vụ đang chạy.
