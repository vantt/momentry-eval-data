---
id: 2026-11-02-reviewer-agent-tim-lenh-duong-di-3c6e
code: M-S1VW
aliases: [M-S1VW]
date: 2026-11-02
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:2dfb5915#L1777", "claude:2dfb5915#L1950"]
hook: "Một lệnh tìm đường đi có thể treo cả server, kể cả ping"
tension: nho_ma_to
sides: ["Một tham số max_len 8–10 trông vô hại", "Đường đi tăng theo cấp số nhân, CPU 100%, mọi request treo"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một công cụ dòng lệnh hỏi Claude Desktop về graph của vault Obsidian đang được viết lại bằng Rust để thay bản Python. Người làm tưởng tham số max_len của lệnh tìm đường đi là vô hại, nhưng trên vault dày liên kết, max_len 8 đến 10 đẩy CPU lên 100% và làm treo cả server, kể cả ping. Đáng nghe vì lỗi này lọt qua agent viết code và chỉ lộ ra khi một agent review độc lập đọc lại code."
audience: dev dùng agent AI để viết code
spine_context: "Một công cụ dòng lệnh để hỏi Claude Desktop về graph của vault Obsidian, đang được viết lại bằng Rust để thay bản Python."
spine_context_lines: [profile, "claude:2dfb5915#L11"]
spine_want: Hoàn tất lõi Rust để thay bản Python.
spine_want_lines: ["claude:2dfb5915#L11"]
spine_obstacle: "Lệnh tìm đường đi nhận max_len từ model mà không có trần, nên một lệnh có thể làm treo cả server MCP."
spine_obstacle_lines: ["claude:2dfb5915#L1777"]
spine_turn: "Tưởng tham số max_len không có trần là vô hại; hoá ra trên vault dày liên kết, max_len 8 đến 10 làm CPU 100%, RAM tăng tới khi bị OS giết, và mọi request sau đó kể cả ping đều treo."
spine_turn_lines: ["claude:2dfb5915#L1777"]
spine_action: "Agent review độc lập đọc code và báo lỗi; người làm giao phần sửa cho agent khác, yêu cầu giới hạn max_len và thời gian chạy."
spine_action_lines: ["claude:2dfb5915#L1780"]
spine_outcome: "Trần max_len là 12, timeout 10 giây; fmt, clippy và test đều qua; đã merge vào nhánh, chưa push."
spine_outcome_lines: ["claude:2dfb5915#L1950", "claude:2dfb5915#L1958"]
spine_takeaway: Mọi truy vấn đệ quy có đầu vào từ model cần trần độ sâu và trần thời gian chạy.
spine_takeaway_lines: ["claude:2dfb5915#L1777"]
completeness: 7
---

# Reviewer agent tìm lệnh đường đi có thể làm treo server MCP

**Góc kể:** Một công cụ dòng lệnh hỏi Claude Desktop về graph của vault Obsidian đang được viết lại bằng Rust để thay bản Python. Người làm tưởng tham số max_len của lệnh tìm đường đi là vô hại, nhưng trên vault dày liên kết, max_len 8 đến 10 đẩy CPU lên 100% và làm treo cả server, kể cả ping. Đáng nghe vì lỗi này lọt qua agent viết code và chỉ lộ ra khi một agent review độc lập đọc lại code.
**Bối cảnh:** Các tool paths, loops và all_loops nhận max_len từ model mà không có trần.
**Chuyện gì xảy ra:** Với max_len 8 đến 10 trên vault dày liên kết, số đường đi tăng theo cấp số nhân, CPU 100% và RAM tăng cho tới khi bị OS giết. Server đơn luồng giữ khoá state nên mọi request sau đó, kể cả ping, đều treo. Fix: max_len tối đa 12, và tự dừng sau 10 giây.
**Bài học:** Mọi truy vấn đệ quy mà đầu vào đến từ model đều cần trần độ sâu và thời gian chạy.
**Góc người ngoài:** cách làm phổ biến là Nhận kết quả 'đã xong' từ agent và tin, hoặc đọc lướt tóm tắt; ở đây khác ở Phiên yêu cầu agent ghi số cụ thể, rồi một agent review khác đọc code và tìm lỗi (ví dụ treo khi stderr lỗi UTF-8, alias bomb 1,45 GB). Người đọc muốn biết vì sao review độc lập bắt được lỗi mà agent viết không thấy.
