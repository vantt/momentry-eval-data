---
id: 2026-10-09-mot-builder-cho-ba-writer-meta-4257
code: M-E6HY
aliases: [M-E6HY]
date: 2026-10-09
repo: repo
status: raw
signals: [khac]
signal_note: "Gom ba writer vào một builder, và test source_import từng ghi kiểu v1 mà không ai bắt được."
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L2123", "omp:cd4449ab#L2133", "omp:cd4449ab#L2204", "omp:cd4449ab#L2234", "omp:cd4449ab#L2255", "omp:cd4449ab#L2294", "omp:cd4449ab#L2352"]
hook: "Test đỏ 5 lần chỉ vì thiếu file:// và một trường"
tension: nho_ma_to
sides: ["Một builder dùng chung cho ba writer", "Test đỏ 4-5 lần vì thiếu file:// và một trường"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Một builder cho ba writer .meta/skill.yaml

**Bối cảnh:** skill_add, source_import và source_backfill mỗi nơi ghi một kiểu metadata khác nhau.
**Chuyện gì xảy ra:** Agent tạo buildInitialSkillMetaYAML dùng chung (L2133). Test source_import v3 đỏ liên tục (bốn đến năm lần) vì nguồn git cần file:// và record thiếu trường. Sau khi sửa, test xanh và commit gom một lần.
**Bài học:** Gom các writer về một builder trước khi sửa từng nơi; test cần repo git thật để bắt lỗi đường ghi.
**Artefact:** Diff của buildInitialSkillMetaYAML; che tên người.
