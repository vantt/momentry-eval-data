---
id: 2026-11-02-doi-schema-index-ma-khong-goi
date: 2026-11-02
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L1020", "claude:c4caee3c#L1023"]
hook: "Đổi schema index mà không phải embed lại một vector nào"
tension: it_ma_nhieu
sides: ["đổi schema index", "không gọi embedder lần nào, điền cột từ text đã lưu"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đổi schema index mà không gọi lại embedder

**Bối cảnh:** Block-anchor cần thêm cột block_id và has_highlight, nên INDEX_SCHEMA_VERSION tăng từ 2 lên 3.
**Chuyện gì xảy ra:** Migration điền cột mới từ text đã lưu, không gọi embedder. Kích thước chunk được lưu như hậu tố +chunk=N trong setting, nên đổi cấu hình sẽ rebuild qua đường có sẵn. Cách này tránh phải embed lại toàn bộ vector.
**Bài học:** Đưa tham số ảnh hưởng đến index vào cơ chế rebuild đã có, thay vì tạo cơ chế mới.
**Artefact:** Sơ đồ migration, không cần chụp.
