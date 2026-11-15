---
id: 2026-10-09-commit-ghi-ten-model-thay-vi
date: 2026-10-09
repo: repo
status: raw
signals: [khác]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [harvest]
lines: ["omp:cd4449ab#L2354", "omp:cd4449ab#L2965", "omp:cd4449ab#L3368", "omp:cd4449ab#L3959"]
hook: "Commit mang tên model, không phải tên git của bạn"
tension: tuong_ma_hoa_ra
sides: ["Tưởng commit mang danh tính git đã cấu hình", "Tác giả ghi là tên model"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Commit ghi tên model thay vì người dùng đã cấu hình

**Bối cảnh:** Lịch sử git của các commit do agent tạo trong worktree.
**Chuyện gì xảy ra:** Các commit Phase 3 và Phase 4 mang tên tác giả là một tên model cụ thể, không phải danh tính git đã cấu hình. Chi tiết này liên quan đến attribution nên cần kiểm trước khi merge.
**Bài học:** Chạy git log với %an trước khi merge. Tác giả commit là một phần bằng chứng về việc ai đã làm gì.
**Artefact:** Ảnh terminal git log có tên tác giả, che email.
