---
id: 2026-11-02-hai-agent-thiet-ke-mcp-doc-3c6e
code: M-SCGG
aliases: [M-SCGG]
date: 2026-11-02
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:2dfb5915#L3051", "claude:2dfb5915#L3070", "claude:2dfb5915#L3088", "claude:2dfb5915#L3098", "claude:2dfb5915#L3110"]
hook: "Hai agent đồng ý hết, nhưng một con số token sai gần gấp đôi"
tension: tuong_ma_hoa_ra
sides: ["Hai agent độc lập cùng kết luận", "Số token danh sách tool bị tính thấp: 1,9 nghìn so với 3,3–3,8 nghìn"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án là một công cụ dòng lệnh để Claude Desktop hỏi về graph của vault Obsidian, và người làm đang chốt bộ tool MCP cho bản Rust. Hai agent thiết kế độc lập gần như trùng nhau: giữ tool rời, không làm code mode, để pkm tự đọc file. Khi phản biện chéo, một bên chỉ ra bên kia ước lượng danh sách tool khoảng 1,9 nghìn token, trong khi file thật 13.381 ký tự tương đương khoảng 3,3 đến 3,8 nghìn. Ước lượng theo số ký tự có thể lệch gần gấp đôi, nên đo file thật trước khi đặt ngưỡng."
audience: dev viết MCP server và đặt ngưỡng token
spine_context: Công cụ dòng lệnh để Claude Desktop hỏi về graph vault Obsidian; đang port lõi sang Rust và chốt bộ tool MCP.
spine_context_lines: [profile, "claude:2dfb5915#L11", "claude:2dfb5915#L3027"]
spine_want: "Chốt interface MCP một cửa gồm search, read và related cho phase 17."
spine_want_lines: ["claude:2dfb5915#L3027", "claude:2dfb5915#L3060"]
spine_obstacle: "Số token mới chỉ ước lượng theo số ký tự, chưa đo bằng tokenizer."
spine_obstacle_lines: ["claude:2dfb5915#L3051"]
spine_turn: "Tưởng danh sách tool khoảng 7 KB, tức khoảng 1,9 nghìn token; hoá ra file thật 13.381 ký tự, khoảng 3,3 đến 3,8 nghìn token."
spine_turn_lines: ["claude:2dfb5915#L3098"]
spine_action: "Hai agent thiết kế độc lập, rồi mỗi bên phản biện bản của bên kia."
spine_action_lines: ["claude:2dfb5915#L3073", "claude:2dfb5915#L3077"]
spine_outcome: "Thống nhất bộ 13 tool; ngưỡng test kích thước đổi từ khoảng 11 KB lên khoảng 17 KB; token nạp mỗi phiên ước 3,8 đến 4,4 nghìn, thay vì khoảng 6,0 nghìn."
spine_outcome_lines: ["claude:2dfb5915#L3098", "claude:2dfb5915#L3110"]
spine_takeaway: Ước lượng token theo số ký tự có thể lệch gần gấp đôi; đo file thật trước khi đặt ngưỡng.
spine_takeaway_lines: ["claude:2dfb5915#L3051", "claude:2dfb5915#L3098"]
completeness: 7
---

# Hai agent thiết kế MCP độc lập, phản biện chéo và sửa con số token

**Góc kể:** Dự án là một công cụ dòng lệnh để Claude Desktop hỏi về graph của vault Obsidian, và người làm đang chốt bộ tool MCP cho bản Rust. Hai agent thiết kế độc lập gần như trùng nhau: giữ tool rời, không làm code mode, để pkm tự đọc file. Khi phản biện chéo, một bên chỉ ra bên kia ước lượng danh sách tool khoảng 1,9 nghìn token, trong khi file thật 13.381 ký tự tương đương khoảng 3,3 đến 3,8 nghìn. Ước lượng theo số ký tự có thể lệch gần gấp đôi, nên đo file thật trước khi đặt ngưỡng.
**Bối cảnh:** Cần chốt bộ tool MCP một cửa, gồm search, read và related.
**Chuyện gì xảy ra:** Hai agent làm độc lập và đi tới kết luận gần như trùng: giữ tool rời, không làm code mode, read do pkm tự đọc. Số token định nghĩa giảm từ khoảng 6,0 nghìn xuống 4,4 nghìn. Khi phản biện chéo, một agent chỉ ra bản kia tính thấp số token danh sách tool: 7 KB là khoảng 1,9 nghìn token, nhưng file thật 13.381 ký tự cho ra khoảng 3,3 đến 3,8 nghìn.
**Bài học:** Ước lượng token theo số ký tự dễ lệch. Hai thiết kế độc lập rồi phản biện chéo bắt được lỗi mà một agent đơn lẻ bỏ sót.
**Artefact:** Bảng so sánh các phương án (chụp báo cáo, không lộ đường dẫn).
**Góc người ngoài:** cách làm phổ biến là Một người viết spec rồi tự quyết, hoặc hỏi nhiều câu nhỏ rời rạc; ở đây khác ở Hai thiết kế gần như trùng nhau; phản biện chéo sửa được số token ước lượng và bắt lỗi compact() mà cả hai không nêu lúc đầu. Người đọc muốn biết cách tổ chức để ra quyết định nhanh mà không phải đoán.
