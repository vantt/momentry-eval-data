---
id: 2026-11-02-viet-tay-json-rpc-cho-mcp
date: 2026-11-02
repo: repo
status: raw
signals: [số trước sau, ràng buộc định hình thiết kế]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L279"]
hook: "Viết tay JSON-RPC: 0.68 MB so với 2.79 MB của thư viện"
tension: it_ma_nhieu
sides: ["tự viết tay, 12 crate, build 2.5 giây", "thư viện có sẵn nặng gấp 4 lần, 56 crate"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Viết tay JSON-RPC cho MCP thay vì dùng rmcp

**Bối cảnh:** Chọn giữa thư viện rmcp và tự viết JSON-RPC cho MCP server.
**Chuyện gì xảy ra:** Binary đã strip: bản viết tay 0.68 MB, rmcp 2.79 MB. Số crate kéo theo là 12 so với 56. Build release sạch mất 2.5 s so với 16.5 s. rmcp lệch Python ở 5 điểm của tầng giao thức, ví dụ thông báo lỗi unknown method và dòng không phải JSON không có phản hồi. Chọn viết tay.
**Bài học:** Đo kích thước và số crate trước khi chọn thư viện. Chỗ lệch ở tầng giao thức khó sửa hơn chỗ khác.
**Artefact:** Bảng hai cột so sánh kích thước, số crate và thời gian build.
