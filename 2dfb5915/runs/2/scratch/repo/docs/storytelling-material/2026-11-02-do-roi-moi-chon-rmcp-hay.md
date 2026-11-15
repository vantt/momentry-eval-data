---
id: 2026-11-02-do-roi-moi-chon-rmcp-hay
date: 2026-11-02
repo: repo
status: raw
signals: [số trước sau, đảo quyết định]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L279", "claude:2dfb5915#L292"]
hook: "Thư viện chính thức nặng 2,79 MB, bản viết tay chỉ 0,68 MB"
tension: tuong_ma_hoa_ra
sides: ["dùng thư viện chính thức cho yên tâm", "nặng gấp 4, kéo 56 crate, build chậm gấp 6"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đo rồi mới chọn: rmcp hay JSON-RPC viết tay cho server MCP

**Bối cảnh:** Phase 03 thử hai cách làm server MCP bằng Rust: thư viện rmcp hoặc JSON-RPC viết tay.
**Chuyện gì xảy ra:** Bản viết tay ra binary 0.68 MB, 12 crate, build sạch trong 2.5 giây. Bản rmcp ra 2.79 MB, 56 crate, build 16.5 giây và kéo theo tokio. Protocol của rmcp khác Python ở 5 chỗ, ví dụ thông báo method không tồn tại và cách trả lời dòng không phải JSON. Quyết định chọn viết tay.
**Bài học:** Khi chọn thư viện, đo kích thước binary, số dependency và khác biệt hành vi với bản gốc trước khi chốt.
**Artefact:** Bảng so sánh hai phương án (kích thước binary, số crate, thời gian build). Không chụp nội dung tool.
