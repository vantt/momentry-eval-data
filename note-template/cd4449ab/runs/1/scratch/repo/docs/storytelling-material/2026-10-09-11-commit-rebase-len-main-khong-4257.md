---
id: 2026-10-09-11-commit-rebase-len-main-khong-4257
code: M-YMS3
aliases: [M-YMS3]
date: 2026-10-09
repo: repo
status: raw
signals: [khac]
signal_note: "Rebase 11 commit lên main mới không xung đột, dù main vừa có commit từ worktree khác."
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [harvest]
lines: ["omp:cd4449ab#L2358", "omp:cd4449ab#L2360", "omp:cd4449ab#L2363", "omp:cd4449ab#L2364", "omp:cd4449ab#L2366"]
hook: "11 commit rebase xong, không xung đột, vì đã đoán trước"
tension: none
sides: []
strength: 0
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# 11 commit rebase lên main không xung đột

**Bối cảnh:** Main đã tiến thêm commit từ worktree khác trong lúc nhánh chưa merge.
**Chuyện gì xảy ra:** Rebase thành công 11 commit (L2360) và make check xanh sau rebase (L2364-2366). Lead đã dự đoán trước bằng merge-tree rằng không có xung đột.
**Bài học:** Dùng merge-tree để dự đoán xung đột trước khi rebase; rebase không xung đột là kết quả đã kiểm chứng.
**Artefact:** Lịch sử commit trước và sau rebase; che tên người.
