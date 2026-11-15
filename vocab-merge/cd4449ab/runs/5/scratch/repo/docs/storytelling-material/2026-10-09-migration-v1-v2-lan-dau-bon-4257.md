---
id: 2026-10-09-migration-v1-v2-lan-dau-bon-4257
code: M-MZYY
aliases: [M-MZYY]
date: 2026-10-09
repo: repo
status: raw
signals: [khác]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L288", "omp:cd4449ab#L459", "omp:cd4449ab#L468", "omp:cd4449ab#L507", "omp:cd4449ab#L531"]
hook: "Migration v1→v2 chạy lần đầu: đỏ bốn lượt"
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

# Migration v1→v2 lần đầu: bốn lần đỏ trước khi chạy được

**Bối cảnh:** Đây là lần đầu chạy test migration cho các bước v1→v2 và v2→v3.
**Chuyện gì xảy ra:** Lần chạy đầu go test migration exit 1. Lỗi gồm marker schema không đọc được, workspace v1 không dựng đủ thư mục .skillhub, và receipt thiếu operation id. Sau bốn lượt sửa, go test ./internal/migration xanh ở L531.
**Bài học:** Khi bắt đầu viết migration, chạy liên tục một gói test nhỏ và đừng gom nhiều thay đổi cùng lúc.
**Artefact:** Không cần.
