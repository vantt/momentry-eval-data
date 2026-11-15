---
id: 2026-10-09-rebase-11-commit-len-main-moi-4257
code: M-F042
aliases: [M-F042]
date: 2026-10-09
repo: repo
status: raw
signals: [khac]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["omp:cd4449ab#L2354", "omp:cd4449ab#L2358", "omp:cd4449ab#L2360", "omp:cd4449ab#L2363", "omp:cd4449ab#L2373"]
hook: "Rebase 11 commit, hash đổi hết mà không một xung đột"
tension: none
sides: []
strength: 0
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Rebase 11 commit lên main mới: hash đổi nhưng không xung đột

**Bối cảnh:** Main đã đi tiếp sau khi worktree D merge. Branch có 11 commit chưa merge.
**Chuyện gì xảy ra:** Rebase xong không có xung đột. Tip của branch đổi từ 6b95b7a sang b01eaa3 trên đầu main b32d678. make check xanh sau rebase với 24 package ok. Lead đã dùng merge-tree để dự đoán trước là không có xung đột.
**Bài học:** Dự đoán xung đột bằng merge-tree trước khi rebase. Hash sẽ đổi sau rebase, nên báo cáo phải ghi hash sau cùng.
**Artefact:** git log --oneline trước và sau khi rebase.
**Góc người ngoài:** cách làm phổ biến là Phần lớn dev chỉ chạy test trước khi rebase, quên chạy lại sau khi rebase; ở đây khác ở Việc chạy lại sau rebase phát hiện lỗi gộp mà lần chạy trước không thấy. Người đọc muốn biết kết quả là của nhánh đã rebase, không phải nhánh cũ.
