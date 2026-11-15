---
id: 2026-11-02-viet-tay-json-rpc-thay-vi
date: 2026-11-02
repo: repo
status: raw
signals: [số trước sau, đảo quyết định]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L279", "claude:2dfb5915#L292"]
hook: "Tự viết tay JSON-RPC, binary nhỏ hơn thư viện chuẩn 4 lần"
tension: it_ma_nhieu
sides: ["Viết tay: 0,68 MB, 12 crate", "Thư viện chuẩn: 2,79 MB, 56 crate"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Viết tay JSON-RPC thay vì rmcp: nhị phân nhỏ hơn 4 lần

**Bối cảnh:** Cần MCP server trả tool list và lỗi giống bản Python từng byte.
**Chuyện gì xảy ra:** rmcp 3.8.0 cho binary 2,79 MB, 56 crate, build sạch 16,5 s và kéo tokio. Viết tay: 0,68 MB, 12 crate, 2,5 s, không runtime. rmcp còn lệch Python ở 5 điểm tầng giao thức, ví dụ thông báo method không tồn tại và dòng không phải JSON không có phản hồi.
**Bài học:** Thư viện chuẩn có thể lệch hành vi bạn cần giữ và kéo theo cả runtime; đo cả hai trước khi chọn.
**Artefact:** Bảng so sánh 4 dòng: kích thước, số crate, thời gian build, runtime.
