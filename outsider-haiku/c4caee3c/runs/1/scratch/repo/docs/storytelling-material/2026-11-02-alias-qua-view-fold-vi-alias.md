---
id: 2026-11-02-alias-qua-view-fold-vi-alias
date: 2026-11-02
repo: repo
status: raw
signals: ["Số trước, số sau"]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L1274", "claude:c4caee3c#L1283", "claude:c4caee3c#L1285"]
hook: "Một thay đổi nhỏ ở query.ts đẩy vi-alias Hit@5 từ 0,73 lên 1,00"
tension: it_ma_nhieu
sides: ["thay đổi nhỏ trong query.ts", "vi-alias Hit@5 từ 0,73 lên 1,00"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Alias qua view fold: vi-alias Hit@5 0,73 lên 1,00

**Bối cảnh:** Alias và từ đồng nghĩa cần khớp theo dạng đã bỏ dấu.
**Chuyện gì xảy ra:** Alias được khoá bằng view fold của truy vấn. Vi-alias Hit@5 từ 0,73 lên 1,00, Hit@1 từ 0,60 lên 0,93. Kiểm đoạn trích cho 15/15 câu là chữ gốc có dấu. Thay đổi trong query.ts nhỏ nên được merge trước các việc khác.
**Bài học:** Khoá alias bằng đúng hàm chuẩn hoá đã dùng khi lưu, đừng viết lại một hàm khác.
**Artefact:** Bảng Hit@1 và Hit@5 trước và sau.
