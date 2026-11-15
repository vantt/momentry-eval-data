---
id: 2026-10-21-khi-commit-agent-chi-stage-dung-fd46
code: M-C9V8
aliases: [M-C9V8]
date: 2026-10-21
repo: repo
status: raw
signals: []
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:9514b261#L1687", "claude:9514b261#L1760", "claude:9514b261#L1773", "claude:9514b261#L3383", "claude:9514b261#L3407"]
hook: "Commit chỉ stage đúng file mình sửa, không dùng git add -A"
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

# Khi commit, agent chỉ stage đúng file do chính nó sửa bằng pathspec, không dùng add tất cả, và để nguyên các thay đổi chưa commit của người dùng trong cây làm việc.

**Chuyện gì xảy ra:** Khi commit, agent chỉ stage đúng file do chính nó sửa bằng pathspec, không dùng add tất cả, và để nguyên các thay đổi chưa commit của người dùng trong cây làm việc.
**Góc người ngoài:** cách làm phổ biến là Chạy git add -A rồi commit một lượt, kéo theo file của người khác hoặc file tạm; ở đây khác ở Mỗi commit chỉ chứa đúng việc của nó, và việc của người dùng không bị đụng. Người đọc sẽ hỏi làm sao để nhiều phiên AI cùng làm trong một repo mà không dẫm chân nhau.
