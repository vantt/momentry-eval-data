---
id: 2026-11-02-prd-muc-3-5-agent-sai-40f9
code: M-YX5C
aliases: [M-YX5C]
date: 2026-11-02
repo: repo
status: raw
signals: [đảo quyết định có lý do, nguyên nhân bất ngờ]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L1177", "claude:c4caee3c#L1192", "claude:c4caee3c#L1264"]
hook: "Agent sửa ghi chú theo hướng sai, người dùng chỉ ra PRD vốn đúng"
tension: nguoi_dung_may_sai
sides: ["agent khẳng định PRD sai về FTS5", "người dùng đọc lại: PRD đúng"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# PRD mục 3.5: agent sai về FTS5, người dùng chỉ ra PRD đúng

**Bối cảnh:** Agent tin PRD sai về việc bỏ dấu tiếng Việt trong FTS5 và định sửa PRD.
**Chuyện gì xảy ra:** Người dùng đọc lại và chỉ ra PRD đúng: unicode61 chỉ bỏ được chữ có một dấu. Agent đổi ghi chú trong plan cho khớp, không sửa PRD.
**Bài học:** Đọc lại tài liệu gốc trước khi sửa tài liệu chuẩn; nhận định của máy có thể sai.
