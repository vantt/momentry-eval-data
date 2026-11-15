---
id: 2026-10-09-commit-ghi-ten-model-thay-vi
date: 2026-10-09
repo: repo
status: raw
signals: [khác]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["omp:cd4449ab#L2354", "omp:cd4449ab#L2965", "omp:cd4449ab#L3368", "omp:cd4449ab#L3959"]
hook: "Commit mang tên một model AI, không phải tên người dùng đã cấu hình"
tension: tuong_ma_hoa_ra
sides: ["git đã cấu hình danh tính người dùng", "commit lại ghi tên model làm tác giả"]
strength: 1
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
**Góc người ngoài:** cách làm phổ biến là Để nguyên author mặc định do công cụ tạo, không kiểm tra; ở đây khác ở Commit ghi tên model thay vì người dùng; đây là chi tiết dễ bỏ qua nhưng ảnh hưởng lịch sử git. Người đọc muốn biết cách kiểm tra author trước khi push.
