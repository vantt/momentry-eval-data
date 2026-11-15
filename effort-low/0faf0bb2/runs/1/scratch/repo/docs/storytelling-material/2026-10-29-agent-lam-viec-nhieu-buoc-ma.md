---
id: 2026-10-29-agent-lam-viec-nhieu-buoc-ma
date: 2026-10-29
repo: repo
status: raw
signals: []
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:0faf0bb2#L1204", "claude:0faf0bb2#L1212", "claude:0faf0bb2#L1228", "claude:0faf0bb2#L1315", "claude:0faf0bb2#L1324", "claude:0faf0bb2#L3539", "claude:0faf0bb2#L3695"]
hook: "Agent gặp lỗi tự dừng, báo cáo, chờ, rồi làm tiếp đúng chỗ cũ"
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

# Agent làm việc nhiều bước mà user không phải nhắc lại: khi phát hiện lỗi hoặc thiếu thông tin, agent tự dừng, báo cáo rồi chờ, sau đó tiếp tục đúng chỗ đã dừng.

**Chuyện gì xảy ra:** Agent làm việc nhiều bước mà user không phải nhắc lại: khi phát hiện lỗi hoặc thiếu thông tin, agent tự dừng, báo cáo rồi chờ, sau đó tiếp tục đúng chỗ đã dừng.
**Góc người ngoài:** cách làm phổ biến là Phần lớn người dùng AI coding agent phải theo dõi sát, nhắc lại yêu cầu, hoặc tự chạy lại lệnh khi agent đi lạc; ở đây khác ở Người đọc sẽ muốn biết cách agent được cấu hình để tự theo dõi tiến trình (Monitor, task notification) mà không cần poll thủ công, và cách nó quyết định khi nào dừng hỏi lại.
