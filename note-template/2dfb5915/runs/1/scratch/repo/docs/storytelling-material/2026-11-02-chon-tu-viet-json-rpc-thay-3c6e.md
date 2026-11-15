---
id: 2026-11-02-chon-tu-viet-json-rpc-thay-3c6e
code: M-1JM3
aliases: [M-1JM3]
date: 2026-11-02
repo: repo
status: raw
signals: [so_truoc_so_sau, nguyen_nhan_bat_ngo]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L279", "claude:2dfb5915#L292"]
hook: "Tự viết JSON-RPC: binary nhỏ hơn 4 lần, build nhanh hơn 6 lần"
tension: it_ma_nhieu
sides: ["Tự viết giao thức thay vì dùng thư viện", "Binary 0,68 MB thay vì 2,79 MB, build 2,5 giây"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một công cụ dòng lệnh cho vault Obsidian đang viết lại lõi bằng Rust để cho kết quả khớp bản Python, và cần một thư viện MCP cho server. Người làm định dùng rmcp, nhưng khi đo thì rmcp lệch Python ở 5 điểm trong tầng giao thức, còn binary to gấp 4 lần và build chậm gấp 6 lần, nên họ tự viết JSON-RPC. Ai chọn thư viện cho một giao thức đã có bản gốc nên đo hành vi trước, vì thư viện có sẵn có thể lệch ngay ở thông điệp lỗi."
audience: dev viết server MCP hoặc chọn thư viện giao thức
spine_context: "Một công cụ dòng lệnh cho vault Obsidian, có cửa MCP để hỏi Claude Desktop về graph; đang viết lại lõi bằng Rust để kết quả khớp bản Python."
spine_context_lines: [profile]
spine_want: "Muốn hoàn tất plan viết lại lõi bằng Rust, làm song song các phase."
spine_want_lines: ["claude:2dfb5915#L11"]
spine_obstacle: Cần chọn thư viện MCP cho server Rust mà vẫn khớp hành vi bản Python.
spine_obstacle_lines: ["claude:2dfb5915#L279"]
spine_turn: Tưởng dùng được thư viện MCP rmcp; đo ra rmcp lệch Python ở 5 điểm trong tầng giao thức.
spine_turn_lines: ["claude:2dfb5915#L279"]
spine_action: Tự viết JSON-RPC và đo so với bản dùng rmcp.
spine_action_lines: ["claude:2dfb5915#L279"]
spine_outcome: "Binary 0,68 MB thay vì 2,79 MB; build sạch 2,5 giây thay vì 16,5 giây; phase 03 đã merge và push."
spine_outcome_lines: ["claude:2dfb5915#L279", "claude:2dfb5915#L292"]
spine_takeaway: Thư viện có sẵn có thể lệch hành vi của bản gốc; đo trước khi chọn.
spine_takeaway_lines: ["claude:2dfb5915#L279"]
completeness: 7
---

# Chọn tự viết JSON-RPC thay vì rmcp: binary 0,68 MB so với 2,79 MB

**Góc kể:** Một công cụ dòng lệnh cho vault Obsidian đang viết lại lõi bằng Rust để cho kết quả khớp bản Python, và cần một thư viện MCP cho server. Người làm định dùng rmcp, nhưng khi đo thì rmcp lệch Python ở 5 điểm trong tầng giao thức, còn binary to gấp 4 lần và build chậm gấp 6 lần, nên họ tự viết JSON-RPC. Ai chọn thư viện cho một giao thức đã có bản gốc nên đo hành vi trước, vì thư viện có sẵn có thể lệch ngay ở thông điệp lỗi.
**Bối cảnh:** Chọn thư viện MCP cho server Rust, phải khớp hành vi của bản Python.
**Chuyện gì xảy ra:** rmcp kéo 56 crate và tokio, build sạch 16,5 giây so với 2,5 giây, binary 2,79 MB so với 0,68 MB. rmcp lệch Python ở 5 điểm trong tầng giao thức. Claude Code thử server/discover trước rồi mới fallback sang initialize, đúng nhánh Python đang dùng, nên ghi lại như điều kiện xem lại.
**Bài học:** Thư viện chuẩn có thể lệch thông điệp lỗi của bản gốc, cần đo trước khi chọn.
