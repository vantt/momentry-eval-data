---
id: 2026-11-02-schema-index-tang-tu-2-len
date: 2026-11-02
repo: repo
status: raw
signals: [số trước sau, khác]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L1020"]
hook: "Nâng schema index từ 2 lên 3 mà không gọi lại embedder"
tension: it_ma_nhieu
sides: ["Không tính lại vector nào", "Chunk cũ vẫn có đủ cột mới, migrate rất nhanh"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Schema index tăng từ 2 lên 3 mà không gọi lại embedder

**Bối cảnh:** Thêm cột block id và highlight cho chunk nên phải tăng phiên bản schema.
**Chuyện gì xảy ra:** Migration điền các cột mới cho chunk cũ từ văn bản đã lưu, không gọi embedder. Điều này giữ thời gian migrate ngắn và không tốn lại tính toán vector.
**Bài học:** Khi chỉ thêm cột có thể suy ra từ dữ liệu đã có, migrate từ văn bản lưu thay vì tính lại embedding.
**Artefact:** Sơ đồ phiên bản schema. Không cần che.
