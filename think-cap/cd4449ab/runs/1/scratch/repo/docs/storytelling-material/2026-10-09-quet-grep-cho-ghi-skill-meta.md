---
id: 2026-10-09-quet-grep-cho-ghi-skill-meta
date: 2026-10-09
repo: repo
status: raw
signals: []
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [harvest]
lines: ["omp:cd4449ab#L2124", "omp:cd4449ab#L2126", "omp:cd4449ab#L2319", "omp:cd4449ab#L2321", "omp:cd4449ab#L2352"]
hook: "Quét grep từ hai chỗ ghi xuống còn một fallback"
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

# Quét grep: chỗ ghi skill.meta.yaml từ hai xuống một fallback

**Bối cảnh:** Lead yêu cầu quét mọi chỗ ghi skill.meta.yaml còn lại trong internal/.
**Chuyện gì xảy ra:** Lần quét đầu ra hai dòng: một comment ở distribution và một chỗ ghi ở source_backfill. Sau khi sửa, lần quét sau còn đúng một dòng ở source_backfill, là fallback cho schema nhỏ hơn 3. Bản sửa đi cùng commit ghi .meta/skill.yaml trong source_import, source_backfill và upstream_update.
**Bài học:** Sau khi đổi định dạng, quét grep để đếm chỗ ghi còn lại và ghi rõ chỗ nào là fallback có chủ đích.
**Artefact:** Đầu ra grep trước và sau, che đường dẫn.
