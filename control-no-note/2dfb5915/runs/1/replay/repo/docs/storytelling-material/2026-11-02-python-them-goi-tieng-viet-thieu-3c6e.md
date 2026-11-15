---
id: 2026-11-02-python-them-goi-tieng-viet-thieu-3c6e
code: M-6W47
aliases: [M-6W47]
date: 2026-11-02
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L2178", "claude:2dfb5915#L2196", "claude:2dfb5915#L2247"]
hook: "Commit 54 dòng, nhưng thiếu một biến môi trường thì index dựng lại mãi"
tension: nho_ma_to
sides: ["Commit chỉ 54 dòng", "Hai OHS khác cấu hình gói khiến index dựng lại liên tục"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: none
spine_context: "Dự án công cụ dòng lệnh hỏi Claude Desktop về graph của vault Obsidian, đang thay bản Python bằng lõi Rust."
spine_context_lines: [profile]
spine_want: Hoàn tất plan chuyển lõi Rust theo yêu cầu của chủ phiên.
spine_want_lines: ["claude:2dfb5915#L11"]
spine_obstacle: Các bước còn lại (phase 15 đến 17) đều nằm sau cổng mà chỉ người làm mở được.
spine_obstacle_lines: ["claude:2dfb5915#L2168"]
spine_action: "Chuyển commit Python 223c9c3 sang Rust, nâng ghim spec và dựng lại golden."
spine_action_lines: ["claude:2dfb5915#L2196", "claude:2dfb5915#L2247"]
spine_outcome: "Mọi cổng kiểm đạt, parity sạch: 64 mục, 0 lệch chưa có tên, 0 mục chưa có."
spine_outcome_lines: ["claude:2dfb5915#L2247", "claude:2dfb5915#L2254"]
spine_takeaway: "Hai tiến trình dùng chung một index phải cùng cấu hình gói ngôn ngữ, nếu không sẽ dựng lại view mãi."
spine_takeaway_lines: ["claude:2dfb5915#L2247"]
completeness: 6
---

# Python thêm gói tiếng Việt: thiếu biến môi trường thì index dựng lại mãi

**Bối cảnh:** Commit 223c9c3 của bản Python làm OHS chạy từ bundle có sẵn gói tiếng Việt.
**Chuyện gì xảy ra:** Commit chỉ 54 dòng, nhưng nếu OHS của pkm và OHS của MCP người dùng dùng cấu hình gói khác nhau trên cùng index, OHS sẽ dựng lại view gói liên tục. Agent đặt biến OHS_LANGUAGE_PACK cho mọi lần khởi động OHS, dựng lại golden với ghim mới, và follow báo 0 commit chưa chuyển.
**Bài học:** Hai tiến trình dùng chung một index phải dùng cùng cấu hình, nếu không sẽ tranh nhau dựng lại.
