---
id: 2026-11-02-moi-subagent-lam-viec-trong-worktree-3c6e
code: M-T5R8
aliases: [M-T5R8]
date: 2026-11-02
repo: repo
status: raw
signals: []
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:2dfb5915#L63", "claude:2dfb5915#L121", "claude:2dfb5915#L136", "claude:2dfb5915#L1100", "claude:2dfb5915#L1791"]
hook: "Mỗi agent một worktree git riêng, không giẫm chân nhau"
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

# Mỗi subagent làm việc trong worktree git riêng và báo kết quả bằng một bản tóm tắt có cấu trúc

**Chuyện gì xảy ra:** Mỗi subagent làm việc trong worktree git riêng và báo kết quả bằng một bản tóm tắt có cấu trúc
**Góc người ngoài:** cách làm phổ biến là Thường nhiều agent cùng sửa một thư mục làm và xung đột file, hoặc người dùng tự chia nhánh và gộp tay; ở đây khác ở Mỗi agent có nhánh và worktree riêng, agent điều phối gộp từng nhánh khi xong, và giải quyết xung đột bằng cách giữ cả hai phía. Người đọc sẽ hỏi làm sao nhiều agent không giẫm chân nhau.
