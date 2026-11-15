---
id: 2026-10-09-rebase-11-commit-len-main-moi-4257
code: M-F042
aliases: [M-F042]
date: 2026-10-09
repo: repo
status: raw
signals: [khác]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [harvest]
lines: ["omp:cd4449ab#L2358", "omp:cd4449ab#L2360", "omp:cd4449ab#L2361", "omp:cd4449ab#L2363", "omp:cd4449ab#L2364"]
hook: "Rebase 11 commit lên main mới mà không một xung đột"
tension: cam_ma_van_lot
sides: ["11 commit rebase lên main đã đổi", "không xung đột nào, vì mỗi worktree sở hữu file riêng"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Rebase 11 commit lên main mới: không xung đột

**Bối cảnh:** Main đã được worktree khác merge thêm commit. Lead yêu cầu rebase trước khi báo cáo.
**Chuyện gì xảy ra:** git rebase main áp dụng sạch 11 commit, không xung đột. make check chạy lại xanh trên nhánh đã rebase, go test mất khoảng 14 giây. Lý do không xung đột là mỗi worktree sở hữu nhóm file riêng.
**Bài học:** Chia phạm vi file theo chủ sở hữu giúp rebase song song ít xung đột. Kiểm tra bằng merge-tree trước khi rebase thật.
**Artefact:** Sơ đồ git log trước và sau rebase, che hash nếu cần.
