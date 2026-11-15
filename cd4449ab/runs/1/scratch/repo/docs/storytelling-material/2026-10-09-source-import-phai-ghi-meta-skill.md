---
id: 2026-10-09-source-import-phai-ghi-meta-skill
date: 2026-10-09
repo: repo
status: raw
signals: [khác]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L2204", "omp:cd4449ab#L2234", "omp:cd4449ab#L2249", "omp:cd4449ab#L2255", "omp:cd4449ab#L2264", "omp:cd4449ab#L2267", "omp:cd4449ab#L2294", "omp:cd4449ab#L2306", "omp:cd4449ab#L2316", "omp:cd4449ab#L2344"]
hook: "Test fail 5 lần vì fixture không phải git repo thật"
tension: none
sides: []
strength: 0
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# source_import phải ghi .meta/skill.yaml giống skill_add

**Bối cảnh:** source_import phải ghi .meta/skill.yaml giống skill_add và trust verdict phải khớp.
**Chuyện gì xảy ra:** Test TestSourceImportInV3 fail 5 lần vì fixture: source phải là git repo thật qua file://, revision phải đúng kiểu, và test còn dùng trường cũ. Sau khi sửa, TestSourceImport pass. Commit 6b95b7a gom source_import, source_backfill và upstream_update.
**Bài học:** Test tích hợp với git thật qua file:// tốn nhiều lượt hơn mock, nhưng bắt được cấu trúc revision thật.
**Artefact:** Đầu ra test PASS và FAIL theo từng lượt. Không cần chụp.
