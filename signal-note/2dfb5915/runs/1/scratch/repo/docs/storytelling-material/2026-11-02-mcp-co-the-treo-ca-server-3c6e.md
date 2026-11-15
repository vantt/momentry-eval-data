---
id: 2026-11-02-mcp-co-the-treo-ca-server-3c6e
code: M-GFW0
aliases: [M-GFW0]
date: 2026-11-02
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo, khac]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L1780", "claude:2dfb5915#L1950"]
hook: "Một lần gọi paths max_len 8 đến 10 làm CPU 100%, ping cũng kẹt"
tension: nho_ma_to
sides: ["Một tham số max_len nhích lên 8-10", "Tổ hợp bùng nổ, cả server treo, kể cả ping"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một công cụ giúp hỏi Claude Desktop về graph của vault Obsidian đang viết lại lõi bằng Rust để thay bản Python cũ và cho kết quả giống hệt. Khi review bản Rust, người làm thấy một chỗ tưởng vô hại: tham số độ dài đường đi do model gửi vào không có trần, nên một lượt gọi có thể làm CPU 100% và kẹt cả server, kể cả ping. Lỗi này đã có từ bản Python, và ai đưa tham số do AI sinh ra vào truy vấn đồ thị đều có thể gặp. Fix đặt trần 12 và thời hạn 10 giây ngay trong truy vấn, và bộ kiểm parity vẫn khớp."
audience: dev làm công cụ hoặc MCP server nhận tham số từ AI
spine_context: "Một công cụ giúp hỏi Claude Desktop về graph của vault Obsidian, đang viết lại lõi bằng Rust để thay bản Python cũ và cho kết quả giống hệt."
spine_context_lines: [profile, "claude:2dfb5915#L11"]
spine_want: Bản Rust phải cho kết quả giống bản Python trên cùng dữ liệu.
spine_want_lines: ["claude:2dfb5915#L11"]
spine_obstacle: "Server đơn luồng giữ khoá state, nên một lượt truy vấn treo làm kẹt cả các yêu cầu sau, kể cả ping."
spine_obstacle_lines: ["claude:2dfb5915#L1777"]
spine_turn: "Tưởng tham số độ dài đường đi do model gửi vào là an toàn; hoá ra không có trần, một lượt gọi có thể làm CPU 100% và treo cả server."
spine_turn_lines: ["claude:2dfb5915#L1777"]
spine_action: Giao phần sửa cho agent riêng và đặt trần max_len 12 cùng thời hạn 10 giây ngay trong tầng truy vấn.
spine_action_lines: ["claude:2dfb5915#L1780", "claude:2dfb5915#L1950"]
spine_outcome: "Vượt 12 thì báo lỗi, quá 10 giây thì báo timeout; parity 64 mục không lệch chưa có tên, 0 mục chưa có; answer key đạt 70/70 và 11/11."
spine_outcome_lines: ["claude:2dfb5915#L1950"]
spine_takeaway: "Đừng tin tham số độ dài do model đưa vào; đặt trần và thời hạn ngay ở tầng truy vấn, không chỉ ở tầng giao thức."
spine_takeaway_lines: ["claude:2dfb5915#L1950"]
completeness: 7
---

# MCP có thể treo cả server: một lượt paths với max_len 8 đến 10 có thể làm bùng nổ tổ hợp

**Góc kể:** Một công cụ giúp hỏi Claude Desktop về graph của vault Obsidian đang viết lại lõi bằng Rust để thay bản Python cũ và cho kết quả giống hệt. Khi review bản Rust, người làm thấy một chỗ tưởng vô hại: tham số độ dài đường đi do model gửi vào không có trần, nên một lượt gọi có thể làm CPU 100% và kẹt cả server, kể cả ping. Lỗi này đã có từ bản Python, và ai đưa tham số do AI sinh ra vào truy vấn đồ thị đều có thể gặp. Fix đặt trần 12 và thời hạn 10 giây ngay trong truy vấn, và bộ kiểm parity vẫn khớp.
**Bối cảnh:** Các tool paths, loops và all_loops nhận max_len từ model mà không có trần. Server đơn luồng giữ khoá state.
**Chuyện gì xảy ra:** Review chỉ ra một lần gọi có thể làm CPU 100% và RAM tăng cho tới khi bị kill, và cả ping cũng bị kẹt. Fix đặt trần max_len là 12 và thời gian tối đa 10 giây, dùng progress handler của SQLite để ngắt. Các ca parity dùng tối đa 4 và answer key tối đa 10, nên không ảnh hưởng.
**Bài học:** Đừng tin tham số độ dài do model đưa vào; đặt trần và thời hạn ngay ở tầng query, không chỉ ở tầng giao thức.
**Artefact:** Con số trần 12 và timeout 10 giây. Không đưa truy vấn.
