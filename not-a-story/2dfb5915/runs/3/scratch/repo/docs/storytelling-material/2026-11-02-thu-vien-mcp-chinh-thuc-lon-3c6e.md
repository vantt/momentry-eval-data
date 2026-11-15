---
id: 2026-11-02-thu-vien-mcp-chinh-thuc-lon-3c6e
code: M-999M
aliases: [M-999M]
date: 2026-11-02
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L279", "claude:2dfb5915#L285"]
hook: "Thư viện MCP chính thức lớn gấp 4 lần bản tự viết"
tension: giup_ma_hai
sides: ["Dùng thư viện chính thức cho yên tâm", "rmcp nặng 2,79 MB với 56 crate, bản tự viết chỉ 0,68 MB với 12 crate"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Thư viện MCP chính thức lớn gấp 4 lần, nên tự viết JSON-RPC

**Bối cảnh:** Chọn giữa thư viện rmcp và tự viết server JSON-RPC cho MCP.
**Chuyện gì xảy ra:** Bản tự viết có binary 0,68 MB và 12 crate, rmcp là 2,79 MB và 56 crate, thời gian build sạch 2,5 giây so với 16,5 giây. rmcp cần tokio và khác Python ở 5 điểm của tầng giao thức. Claude Code thử server/discover trước, rồi fallback về initialize, và bản Python dựa vào đường fallback đó.
**Bài học:** Thư viện đầy đủ có thể kéo theo lệch hành vi ở tầng giao thức, đo cả kích thước lẫn hành vi trước khi chọn.
**Artefact:** Bảng so sánh kích thước và số crate (không có đường dẫn).
