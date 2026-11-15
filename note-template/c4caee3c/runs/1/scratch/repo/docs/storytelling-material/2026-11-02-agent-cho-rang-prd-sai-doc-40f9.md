---
id: 2026-11-02-agent-cho-rang-prd-sai-doc-40f9
code: M-VTNQ
aliases: [M-VTNQ]
date: 2026-11-02
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L1177", "claude:c4caee3c#L1187", "claude:c4caee3c#L1264"]
hook: "Agent tưởng PRD sai, đọc lại thì lỗi nằm ở bộ eval"
tension: tuong_ma_hoa_ra
sides: ["Agent đề xuất sửa PRD", "PRD đúng, bộ eval mới sai"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Agent cho rằng PRD sai, đọc lại thì PRD đúng

**Bối cảnh:** Một agent cho rằng mục 3.5 của PRD về tiếng Việt và FTS5 sai, vì bộ eval không tái hiện được lỗi như PRD mô tả.
**Chuyện gì xảy ra:** Agent đề xuất sửa PRD. Khi đọc lại, PRD đúng: bỏ dấu được với âm tiết có một dấu, không được với âm tiết hai dấu và đ. Vấn đề nằm ở bộ eval chứ không ở PRD. Agent sửa ghi chú trong plan cho khớp và không sửa PRD.
**Bài học:** Đọc lại spec và kiểm nguồn trước khi kết luận spec sai.
