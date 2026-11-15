---
id: 2026-11-02-phien-ban-rust-port-vuot-python
date: 2026-11-02
repo: repo
status: raw
signals: ["số trước, số sau"]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L1859", "claude:2dfb5915#L2254"]
hook: "Bản Rust tự viết nhỏ hơn 4 lần và build nhanh hơn 6 lần"
tension: it_ma_nhieu
sides: ["Tự viết tay, chỉ 12 crate, 0,68 MB", "Thư viện có sẵn nặng 2,79 MB, 56 crate, build 16,5 giây"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Phiên bản Rust port: vượt Python ở tốc độ build, nhưng cái được chọn là sự nhỏ gọn

**Bối cảnh:** So sánh hai hướng thư viện cho MCP server: một bản viết tay JSON-RPC và một bản dùng thư viện rmcp.
**Chuyện gì xảy ra:** Bản viết tay ra binary 0,68 MB, 12 crate, build sạch 2,5 s; rmcp ra 2,79 MB, 56 crate, build 16,5 s và kéo theo tokio. rmcp còn lệch Python ở năm chỗ của tầng giao thức nên bị loại.
**Bài học:** Đo kích thước binary, số crate và thời gian build trước khi chọn thư viện; lệch giao thức quan trọng hơn tiện lợi API.
**Artefact:** Bảng so sánh hai phương án (kích thước, crate, thời gian build).
