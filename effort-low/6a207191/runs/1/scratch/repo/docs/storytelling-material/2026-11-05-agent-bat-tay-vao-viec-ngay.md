---
id: 2026-11-05-agent-bat-tay-vao-viec-ngay
date: 2026-11-05
repo: repo
status: raw
signals: []
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:6a207191#L1280", "claude:6a207191#L1324", "claude:6a207191#L2038", "claude:6a207191#L2103"]
hook: "Agent làm ngay khi có bản nháp, nhưng dừng trước việc gửi ra ngoài"
tension: khac
sides: ["Agent tự chạy không chờ duyệt từng bước", "Vẫn dừng hỏi trước khi gửi lên hub hoặc merge main"]
strength: 1
stakes: 0
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Agent bắt tay vào việc ngay khi có bản nháp, không chờ người dùng duyệt từng bước, nhưng vẫn dừng trước các hành động ảnh hưởng ra ngoài (gửi lên hub, merge lên main)

**Chuyện gì xảy ra:** Agent bắt tay vào việc ngay khi có bản nháp, không chờ người dùng duyệt từng bước, nhưng vẫn dừng trước các hành động ảnh hưởng ra ngoài (gửi lên hub, merge lên main)
**Góc người ngoài:** cách làm phổ biến là Nhiều người dùng AI hoặc đợi xác nhận từng bước, hoặc để agent chạy hết không giám sát rồi phải dọn lộn xộn; ở đây khác ở Phân loại rõ việc nào đảo ngược được (sửa file trong repo) và việc nào không (gửi hub, push). Người đọc sẽ hỏi: làm sao agent biết khi nào phải hỏi lại?.
