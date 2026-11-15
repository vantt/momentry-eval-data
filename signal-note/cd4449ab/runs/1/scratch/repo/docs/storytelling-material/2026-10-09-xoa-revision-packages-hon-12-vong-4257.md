---
id: 2026-10-09-xoa-revision-packages-hon-12-vong-4257
code: M-68TN
aliases: [M-68TN]
date: 2026-10-09
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo, khac]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L3056", "omp:cd4449ab#L3058", "omp:cd4449ab#L3083", "omp:cd4449ab#L3085", "omp:cd4449ab#L3088", "omp:cd4449ab#L3095", "omp:cd4449ab#L3139", "omp:cd4449ab#L3146", "omp:cd4449ab#L3148", "omp:cd4449ab#L3149", "omp:cd4449ab#L3187", "omp:cd4449ab#L3194", "omp:cd4449ab#L3196", "omp:cd4449ab#L3203", "omp:cd4449ab#L3205", "omp:cd4449ab#L3224", "omp:cd4449ab#L3226", "omp:cd4449ab#L3244", "omp:cd4449ab#L3253", "omp:cd4449ab#L3262", "omp:cd4449ab#L3277", "omp:cd4449ab#L3286", "omp:cd4449ab#L3316", "omp:cd4449ab#L3325", "omp:cd4449ab#L3343", "omp:cd4449ab#L3346", "omp:cd4449ab#L3355"]
hook: "Xoá hai file, test đỏ hơn 12 vòng mới xanh"
tension: nho_ma_to
sides: ["chỉ gỡ hai file", "hơn 12 vòng test đỏ mới xong"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: none
spine_context: Dự án mcp-skill-hub đang được đơn giản hoá theo từng phase; phiên này gỡ revision packages trong worktree riêng.
spine_context_lines: ["omp:cd4449ab#L2374"]
spine_want: Gỡ revision packages khỏi code theo phần Phase 3 đã được giao.
spine_want_lines: ["omp:cd4449ab#L2374"]
spine_obstacle: "Test distill đỏ ngay sau khi xoá file, và go test ./internal/app đỏ nhiều lần liên tiếp."
spine_obstacle_lines: ["omp:cd4449ab#L3088", "omp:cd4449ab#L3346"]
spine_action: "Xoá hai file revision_package, sửa validation và types cho đến khi test xanh."
spine_action_lines: ["omp:cd4449ab#L3080", "omp:cd4449ab#L3083"]
spine_outcome: go test ./internal/app xanh ở lần chạy cuối; kết quả make check không có trong trích đoạn.
spine_outcome_lines: ["omp:cd4449ab#L3355"]
spine_takeaway: "Khi gỡ một kiểu dữ liệu, tìm mọi nơi đọc nó trước khi xoá, đừng dựa vào test đỏ để dò."
spine_takeaway_lines: ["omp:cd4449ab#L3088"]
completeness: 6
---

# Xoá revision packages: hơn 12 vòng test đỏ trong internal/app

**Bối cảnh:** Gỡ internal/distill/revision_package.go và test, cùng các chỗ validation đọc nó.
**Chuyện gì xảy ra:** Gỡ hai file revision_package. Test distill đỏ ngay vì validation vẫn duyệt runtime packages. Sau đó go test ./internal/app đỏ hơn 12 lần: tombstone, comparison stale, evidence cần revision và package identity. Mỗi lần sửa một chỗ rồi chạy lại. Lần chạy cuối trong internal/app xanh; vet còn báo thiếu import context trong types.go, đã sửa.
**Bài học:** Khi gỡ một kiểu dữ liệu, tìm mọi nơi validation đọc nó trước; số lần đỏ cho thấy chỗ phụ thuộc còn sót.
**Artefact:** Biểu đồ số lần test đỏ theo thứ tự chạy, nếu muốn vẽ.
