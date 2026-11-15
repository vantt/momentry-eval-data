---
id: 2026-10-09-xoa-subsystem-insight-run-revision-vet
date: 2026-10-09
repo: repo
status: raw
signals: [khác]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L3056", "omp:cd4449ab#L3058", "omp:cd4449ab#L3083", "omp:cd4449ab#L3085", "omp:cd4449ab#L3116", "omp:cd4449ab#L3122", "omp:cd4449ab#L3137", "omp:cd4449ab#L3139", "omp:cd4449ab#L3148", "omp:cd4449ab#L3151", "omp:cd4449ab#L3173"]
hook: "Xoá một subsystem: 12 lần test đỏ vì tombstone còn đọc"
tension: cam_ma_van_lot
sides: ["Đã xoá code của subsystem", "Tombstone và validator vẫn đọc revision package"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Xoá subsystem insight/run/revision: vet, test và schema đi theo

**Bối cảnh:** Xoá insight/run lifecycle, revision packages, file LINK và layout intake.
**Chuyện gì xảy ra:** Agent xoá 6 schema JSON, revision_package.go và test của nó. go vet báo 'undefined: context' vì một import còn dùng bị xoá nhầm. Test distill và app chạy khoảng 12 lần đỏ vì tombstone và validator còn đọc revision package. Cuối cùng go test ./internal/app xanh sau 8.8 giây.
**Bài học:** Xoá một subsystem kéo theo validator và test ẩn. Chạy go vet và test sau mỗi bước xoá, đừng gom thành một lượt.
**Artefact:** Số file xoá và sửa theo commit 4022062, cùng docs/design/07 được cập nhật trong cùng commit.
