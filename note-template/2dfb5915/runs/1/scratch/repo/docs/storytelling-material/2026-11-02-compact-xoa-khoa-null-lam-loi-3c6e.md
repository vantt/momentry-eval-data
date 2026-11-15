---
id: 2026-11-02-compact-xoa-khoa-null-lam-loi-3c6e
code: M-45AS
aliases: [M-45AS]
date: 2026-11-02
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L3060", "claude:2dfb5915#L3110"]
hook: "Lỗi hứa 5 khoá, agent chỉ nhận được 3"
tension: giup_ma_hai
sides: ["Hàm compact dọn bớt cho gọn", "Nó xoá mất 2 trong 5 khoá mà hợp đồng yêu cầu"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án là một công cụ dòng lệnh cho vault Obsidian, đang viết lại bằng Rust và thêm cửa MCP để Claude Desktop hỏi graph của vault. Lúc OHS đang khởi động, người làm tin hợp đồng 5 khoá vẫn được giữ vì test kiểm đủ 5 khoá. Hoá ra hàm compact() bỏ các khoá null trước khi trả cho agent, nên chỉ còn 3 khoá; test chạy trước bước đó nên không bắt được. Ai viết test cho API trả JSON nên kiểm đúng chỗ dữ liệu ra khỏi hệ thống."
audience: dev viết test cho API hoặc công cụ MCP
spine_context: "Công cụ dòng lệnh cho vault Obsidian, đang viết lại lõi bằng Rust và thêm cửa MCP để Claude Desktop hỏi graph của vault."
spine_context_lines: [profile]
spine_want: "Cửa MCP phải trả đủ 5 khoá theo hợp đồng, kể cả khi OHS đang khởi động."
spine_want_lines: ["claude:2dfb5915#L3060"]
spine_obstacle: "Lúc OHS starting, progress và eta_s là null nên bị bỏ, agent chỉ nhận 3 khoá."
spine_obstacle_lines: ["claude:2dfb5915#L3060"]
spine_turn: Tưởng hợp đồng 5 khoá đã được giữ vì test kiểm 5 khoá; hoá ra test chạy trước compact() nên không thấy khoá null bị bỏ.
spine_turn_lines: ["claude:2dfb5915#L3060", "claude:2dfb5915#L3110"]
spine_action: Miễn compact() cho lỗi ohs_not_ready và thêm test ở tầng MCP.
spine_action_lines: ["claude:2dfb5915#L3110"]
spine_takeaway: "Viết test ở đúng tầng mà dữ liệu đi ra cho người dùng, không ở tầng trung gian."
spine_takeaway_lines: ["claude:2dfb5915#L3110"]
completeness: 6
---

# compact() xoá khoá null làm lỗi ohs_not_ready mất 2 trong 5 khoá

**Góc kể:** Dự án là một công cụ dòng lệnh cho vault Obsidian, đang viết lại bằng Rust và thêm cửa MCP để Claude Desktop hỏi graph của vault. Lúc OHS đang khởi động, người làm tin hợp đồng 5 khoá vẫn được giữ vì test kiểm đủ 5 khoá. Hoá ra hàm compact() bỏ các khoá null trước khi trả cho agent, nên chỉ còn 3 khoá; test chạy trước bước đó nên không bắt được. Ai viết test cho API trả JSON nên kiểm đúng chỗ dữ liệu ra khỏi hệ thống.
**Bối cảnh:** Mọi kết quả tool đi qua compact() để bỏ khoá rỗng, kể cả lỗi trạng thái OHS.
**Chuyện gì xảy ra:** Khi OHS ở trạng thái starting, progress và eta_s là null nên bị bỏ, agent chỉ nhận 3 khoá trong khi hợp đồng yêu cầu 5. Test cũ kiểm 5 khoá trước khi compact nên không bắt được. Sửa bằng miễn trừ cho lỗi ohs_not_ready và thêm test ở tầng MCP.
**Bài học:** Viết test ở đúng tầng mà dữ liệu đi ra cho người dùng, không ở tầng trung gian.
