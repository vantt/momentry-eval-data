---
id: 2026-10-09-rebase-11-commit-len-main-khong
date: 2026-10-09
repo: repo
status: raw
signals: [khác]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [harvest]
lines: ["omp:cd4449ab#L2358", "omp:cd4449ab#L2360", "omp:cd4449ab#L2363", "omp:cd4449ab#L2364", "omp:cd4449ab#L2366"]
hook: "Rebase 11 commit, không xung đột, đúng như lead đoán"
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

# Rebase 11 commit lên main không xung đột

**Bối cảnh:** Sau khi lead merge checkpoint Phase 4, main đã đổi và worktree cần rebase.
**Chuyện gì xảy ra:** git rebase main chạy qua 11 commit và không có xung đột. Lead đã dự đoán điều này bằng merge-tree trước đó. Make check chạy lại trên nhánh đã rebase vẫn xanh.
**Bài học:** Phân quyền file theo worktree giảm xung đột; kiểm bằng merge-tree trước khi rebase.
**Artefact:** Đầu ra log sau rebase, commit hash.
