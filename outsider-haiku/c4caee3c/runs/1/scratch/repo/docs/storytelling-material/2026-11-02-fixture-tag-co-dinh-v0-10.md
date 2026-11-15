---
id: 2026-11-02-fixture-tag-co-dinh-v0-10
date: 2026-11-02
repo: repo
status: raw
signals: [Nguyên nhân bất ngờ]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L3868", "claude:c4caee3c#L3875", "claude:c4caee3c#L3912"]
hook: "Tag fixture ghi cứng v0.10.0 làm gói Mac Intel không ra"
tension: nho_ma_to
sides: ["một chuỗi tag ghi cứng trong workflow", "gói Mac Intel không dựng được"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Fixture tag cố định v0.10.0 trong workflow lệch với bộ eval v0.11.0

**Bối cảnh:** Workflow CI tải fixture theo một tag viết cứng, còn golden set đã chuyển sang tag mới hơn.
**Chuyện gì xảy ra:** Hai workflow dựng gói và pin-effect báo lỗi golden set khác với bản được sinh cho phiên bản fixture này, nên gói Mac Intel không ra. Sửa: đọc FIXTURE_TAG từ run-eval.mjs thay cho chuỗi cứng, và thất bại rõ ràng nếu thiếu tag.
**Bài học:** Giữ một nguồn sự thật cho phiên bản fixture; đừng gõ lại tag trong workflow.
**Artefact:** Thông báo lỗi CI đã rút gọn.
