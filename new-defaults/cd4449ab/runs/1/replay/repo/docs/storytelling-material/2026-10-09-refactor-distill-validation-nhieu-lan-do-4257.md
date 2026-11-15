---
id: 2026-10-09-refactor-distill-validation-nhieu-lan-do-4257
code: M-MQ5C
aliases: [M-MQ5C]
date: 2026-10-09
repo: repo
status: raw
signals: []
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L1972", "omp:cd4449ab#L3088", "omp:cd4449ab#L3139", "omp:cd4449ab#L3187", "omp:cd4449ab#L3196", "omp:cd4449ab#L3205", "omp:cd4449ab#L3226", "omp:cd4449ab#L3233", "omp:cd4449ab#L3235", "omp:cd4449ab#L3244", "omp:cd4449ab#L3253", "omp:cd4449ab#L3262", "omp:cd4449ab#L3277", "omp:cd4449ab#L3286", "omp:cd4449ab#L3287", "omp:cd4449ab#L3289", "omp:cd4449ab#L3290", "omp:cd4449ab#L3292", "omp:cd4449ab#L3316", "omp:cd4449ab#L3325", "omp:cd4449ab#L3346"]
hook: "Test cần tìm nằm trong commit docs, không nằm trong code"
tension: khac
sides: ["Test về logic distill", "Lại nằm trong commit tài liệu WebUI"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Refactor distill validation: nhiều lần đỏ và test tombstone nằm trong commit docs

**Bối cảnh:** Bỏ runtime packages khỏi validate workspace distill, nhưng các test cũ về tombstone và comparison stale vẫn dựa vào hành vi đó.
**Chuyện gì xảy ra:** Test đỏ khoảng chục lần. go vet báo thiếu import context. TestDistillGeneratesRemovalTombstoneAndMarksComparisonStale fail vì các observation không còn run được package. git log -S cho thấy chuỗi test nằm trong commit docs về WebUI, không nằm trong code. Diff so với origin/main của workspace_validation.go là +18 và -51 dòng.
**Bài học:** Khi đổi hành vi validate, tìm từng test bị ảnh hưởng và quyết định giữ hay đổi. Đừng thêm cờ bỏ qua để che lỗi.
**Artefact:** Diff +18 -51 dòng và danh sách test bị đổi.
