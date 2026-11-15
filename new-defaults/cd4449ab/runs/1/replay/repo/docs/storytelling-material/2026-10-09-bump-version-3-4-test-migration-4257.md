---
id: 2026-10-09-bump-version-3-4-test-migration-4257
code: M-G4ED
aliases: [M-G4ED]
date: 2026-10-09
repo: repo
status: raw
signals: [khac]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L2770", "omp:cd4449ab#L2771", "omp:cd4449ab#L2773", "omp:cd4449ab#L2795", "omp:cd4449ab#L2797", "omp:cd4449ab#L2800", "omp:cd4449ab#L2804", "omp:cd4449ab#L2806", "omp:cd4449ab#L2807", "omp:cd4449ab#L2809", "omp:cd4449ab#L2812"]
hook: "Nâng version 3→4, test của các bản migrate cũ đồng loạt hỏng"
tension: giup_ma_hai
sides: ["Thêm bước migrate mới", "Test của các bước migrate cũ hỏng theo"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Bump version 3→4: test migration cũ đọc marker không còn đúng

**Bối cảnh:** Binary mới báo 'Canonical schema version is incompatible', nên các test migration cũ đỏ.
**Chuyện gì xảy ra:** Test v1→v2 không tìm thấy hàm đã đổi tên. Test v2→v3 phải đổi file skill.meta.yaml cũ sang đúng dạng. Sau khi sửa, go test ./internal/migration xanh ở L2809. make check vẫn đỏ ở lint và fmt.
**Bài học:** Khi đổi version schema, test migration từng bước phải đổi cùng, vì mỗi bước dựng dữ liệu khác nhau.
**Artefact:** Không cần.
