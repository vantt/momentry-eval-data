---
id: 2026-11-02-phien-ban-rust-port-vuot-python-3c6e
code: M-FCX0
aliases: [M-FCX0]
date: 2026-11-02
repo: repo
status: raw
signals: ["số trước, số sau"]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L1859", "claude:2dfb5915#L2254"]
hook: "Rust nhanh hơn Python, nhưng thứ được chọn là 0,68 MB gọn nhẹ"
tension: chon_mot_mat_mot
sides: ["thư viện rmcp có sẵn, đỡ viết tay", "bản viết tay 0,68 MB, build 2,5 giây thay vì 2,79 MB và 16,5 giây"]
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
