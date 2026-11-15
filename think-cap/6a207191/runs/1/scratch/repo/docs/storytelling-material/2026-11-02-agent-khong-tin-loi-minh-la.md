---
id: 2026-11-02-agent-khong-tin-loi-minh-la
date: 2026-11-02
repo: repo
status: raw
signals: []
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:6a207191#L1100", "claude:6a207191#L1103", "claude:6a207191#L1147", "claude:6a207191#L1161", "claude:6a207191#L1441", "claude:6a207191#L1453"]
hook: "Agent không tin lời mình: grep ra 2 file thay vì 3, nó tự sửa"
tension: khac
sides: ["Câu trả lời của AI nghe có lý nên người dùng tin", "Chính agent chạy lại lệnh và phát hiện mình sai"]
strength: 2
stakes: 1
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Agent không tin lời mình là đúng. Nó tự chạy lại các lệnh, đọc file thật, và khi thấy kết quả không khớp (ví dụ grep chỉ ra 2 file thay vì 3, hay skill không có trường như mình nghĩ) thì sửa lại nhận định.

**Chuyện gì xảy ra:** Agent không tin lời mình là đúng. Nó tự chạy lại các lệnh, đọc file thật, và khi thấy kết quả không khớp (ví dụ grep chỉ ra 2 file thay vì 3, hay skill không có trường như mình nghĩ) thì sửa lại nhận định.
**Góc người ngoài:** cách làm phổ biến là Người dùng thường tin câu trả lời của AI nếu nghe có lý, hoặc chỉ hỏi lại khi thấy lỗi rõ ràng; ở đây khác ở Agent sửa khi bằng chứng mâu thuẫn, nên ít đưa ra thông tin sai đi xa. Người đọc sẽ hỏi làm sao để AI tự kiểm chứng trước khi báo cáo.
