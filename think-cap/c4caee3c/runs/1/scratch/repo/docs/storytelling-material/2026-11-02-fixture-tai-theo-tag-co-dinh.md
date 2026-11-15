---
id: 2026-11-02-fixture-tai-theo-tag-co-dinh
date: 2026-11-02
repo: repo
status: raw
signals: [Nguyên nhân bất ngờ]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L3909", "claude:c4caee3c#L3912"]
hook: "Golden set v0.11.0 nhưng fixture vẫn tải v0.10.0 hardcode"
tension: nho_ma_to
sides: ["Một chuỗi tag hardcode quên cập nhật", "Cả bộ eval báo lệch golden set"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Fixture tải theo tag cố định v0.10.0 trong khi bộ eval đã sang v0.11.0

**Bối cảnh:** Hai workflow bundles và pin-effect clone fixture ở tag hardcode, còn run-eval.mjs đã chuyển v0.11.0.
**Chuyện gì xảy ra:** Golden set không khớp fixture, báo 'differs from the golden set generated with this fixture version'. Lỗi gốc là một chuỗi hardcode không đồng bộ. Sửa cho workflow đọc FIXTURE_TAG từ run-eval.mjs.
**Bài học:** Đừng hardcode phiên bản dữ liệu trong workflow; đọc từ một nguồn duy nhất.
**Artefact:** Không cần.
