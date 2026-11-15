---
id: 2026-10-09-moi-agent-lam-viec-trong-mot-4257
code: M-T1TR
aliases: [M-T1TR]
date: 2026-10-09
repo: repo
status: raw
signals: []
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [outsider]
lines: ["omp:cd4449ab#L6", "omp:cd4449ab#L2345", "omp:cd4449ab#L2358", "omp:cd4449ab#L3656"]
hook: "Mỗi agent một worktree, cấm ghi vào checkout chính"
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

# Mỗi agent làm việc trong một git worktree riêng với branch riêng, còn lead làm trong checkout chính. Có quy tắc cấm ghi vào checkout chính và cấm push hay merge.

**Chuyện gì xảy ra:** Mỗi agent làm việc trong một git worktree riêng với branch riêng, còn lead làm trong checkout chính. Có quy tắc cấm ghi vào checkout chính và cấm push hay merge.
**Góc người ngoài:** cách làm phổ biến là Phần lớn người dùng AI làm trên một thư mục và một branch, hoặc để agent chỉnh thẳng vào repo đang dùng; ở đây khác ở Đây là cách cô lập nhiều agent cùng lúc trên một repo. Người đọc muốn biết tại sao cần ranh giới đường dẫn tuyệt đối và cách rebase về main trước khi báo cáo.
