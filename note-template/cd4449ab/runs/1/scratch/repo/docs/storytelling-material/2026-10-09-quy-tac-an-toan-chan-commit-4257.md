---
id: 2026-10-09-quy-tac-an-toan-chan-commit-4257
code: M-17F6
aliases: [M-17F6]
date: 2026-10-09
repo: repo
status: raw
signals: [khac]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [harvest]
lines: ["omp:cd4449ab#L1342", "omp:cd4449ab#L1344", "omp:cd4449ab#L1363", "omp:cd4449ab#L1364", "omp:cd4449ab#L2344", "omp:cd4449ab#L2345"]
hook: "Luật an toàn chặn commit vì file của người khác, chủ phải sửa luật"
tension: giup_ma_hai
sides: ["Luật an toàn để tránh commit nhầm file", "Chặn cả file vô hại, chủ phải viết lại luật nhiều lần"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Quy tắc an toàn chặn commit vì file của worktree khác

**Bối cảnh:** Luật yêu cầu main checkout phải sạch trước mỗi commit, nhưng nhiều worktree làm việc song song trên cùng repo.
**Chuyện gì xảy ra:** Lần đầu agent dừng và báo vì main có file của worktree khác (L1363). Chủ mở luật: chỉ cần không có file do mình sửa (L1364). Lần sau lại dừng vì một file prompt untracked, chủ xác nhận là bình thường (L2345). Luật được viết lại nhiều lần trong một phiên.
**Bài học:** Luật an toàn nên viết theo thứ cần bảo vệ (file của mình), đừng viết theo trạng thái sạch chung.
**Artefact:** Đoạn luật trước và sau khi chủ sửa; che đường dẫn.
