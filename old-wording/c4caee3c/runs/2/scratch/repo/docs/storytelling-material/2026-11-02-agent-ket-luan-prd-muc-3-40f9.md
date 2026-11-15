---
id: 2026-11-02-agent-ket-luan-prd-muc-3-40f9
code: M-Y35G
aliases: [M-Y35G]
date: 2026-11-02
repo: repo
status: raw
signals: [khac, nguoi_duyet_may_soan]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L1177", "claude:c4caee3c#L1179", "claude:c4caee3c#L1187", "claude:c4caee3c#L1264"]
hook: "Agent kết luận PRD sai, hoá ra chính agent đọc nhầm"
tension: tuong_ma_hoa_ra
sides: ["Agent chắc PRD mục 3.5 sai", "PRD đúng, chính agent đọc nhầm"]
strength: 3
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Agent kết luận PRD mục 3.5 sai, hoá ra chính agent đọc nhầm

**Bối cảnh:** Một agent đề nghị sửa PRD 3.5 vì corpus cũ không tái hiện được lỗi tiếng Việt với FTS5.
**Chuyện gì xảy ra:** Khi lead đọc lại PRD, nội dung đã đúng: FTS5 chỉ bỏ dấu được chữ có một dấu, còn chữ hai dấu và chữ đ thì không. Lead chỉ sửa ghi chú trong plan cho khớp và không sửa PRD.
**Bài học:** Trước khi sửa tài liệu theo nhận định của agent, đọc lại nguồn. Lỗi có thể nằm ở bộ đo chứ không ở tài liệu.
