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
hook: "Hai agent thiết kế riêng, phản biện chéo thì lộ số token tính thấp"
tension: tuong_ma_hoa_ra
sides: ["Hai agent độc lập cùng ra một kết luận, tưởng chắc chắn", "Phản biện chéo thấy số token danh sách tool tính thấp gần một nửa: 1,9 nghìn thay vì 3,3 đến 3,8 nghìn"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án là công cụ hỏi Claude Desktop về graph của vault Obsidian, đang thay lõi Python bằng Rust, và cần chốt bộ tool MCP cho nó. Hai agent thiết kế độc lập rồi chéo phản biện; một bên ước lượng danh sách tool chỉ khoảng 1,9 nghìn token, nhưng file thật 13.381 ký tự tương đương 3,3 đến 3,8 nghìn. Ước lượng theo số ký tự lệch gần một nửa, nên người viết tool MCP cho AI nên đo token thật trước khi chốt ngân sách."
audience: dev viết tool MCP cho AI assistant
spine_context: "Dự án là công cụ hỏi Claude Desktop về graph của vault Obsidian, đang thay lõi Python bằng Rust."
spine_context_lines: [profile, "claude:2dfb5915#L11"]
spine_want: "Chốt bộ tool MCP một cửa gồm search, read và related."
spine_want_lines: ["claude:2dfb5915#L3027"]
spine_obstacle: "Hai cửa tool hiện nay tốn khoảng 6,0 nghìn token định nghĩa cho mỗi request."
spine_obstacle_lines: ["claude:2dfb5915#L3051"]
spine_turn: "Tưởng danh sách tool chỉ khoảng 1,9 nghìn token theo 7 KB; hoá ra file thật 13.381 ký tự, tương đương khoảng 3,3 đến 3,8 nghìn token."
spine_turn_lines: ["claude:2dfb5915#L3098"]
spine_action: "Bật hai agent thiết kế interface độc lập, rồi cho mỗi bên phản biện bản của bên kia."
spine_action_lines: ["claude:2dfb5915#L3039", "claude:2dfb5915#L3073", "claude:2dfb5915#L3077"]
spine_outcome: "Cả hai ra gần như cùng một bộ 13 tool; token định nghĩa ước còn khoảng 3,8 đến 4,4 nghìn, vẫn chưa đo thật."
spine_outcome_lines: ["claude:2dfb5915#L3088"]
spine_takeaway: "Trước khi chốt ngân sách token, đo bằng tokenizer thay vì quy đổi từ số ký tự."
spine_takeaway_lines: ["claude:2dfb5915#L3051", "claude:2dfb5915#L3098"]
completeness: 7
---

# Hai agent thiết kế MCP độc lập, phản biện chéo và sửa con số token

**Góc kể:** Dự án là công cụ hỏi Claude Desktop về graph của vault Obsidian, đang thay lõi Python bằng Rust, và cần chốt bộ tool MCP cho nó. Hai agent thiết kế độc lập rồi chéo phản biện; một bên ước lượng danh sách tool chỉ khoảng 1,9 nghìn token, nhưng file thật 13.381 ký tự tương đương 3,3 đến 3,8 nghìn. Ước lượng theo số ký tự lệch gần một nửa, nên người viết tool MCP cho AI nên đo token thật trước khi chốt ngân sách.
**Bối cảnh:** Cần chốt bộ tool MCP một cửa, gồm search, read và related.
**Chuyện gì xảy ra:** Hai agent làm độc lập và đi tới kết luận gần như trùng: giữ tool rời, không làm code mode, read do pkm tự đọc. Số token định nghĩa giảm từ khoảng 6,0 nghìn xuống 4,4 nghìn. Khi phản biện chéo, một agent chỉ ra bản kia tính thấp số token danh sách tool: 7 KB là khoảng 1,9 nghìn token, nhưng file thật 13.381 ký tự cho ra khoảng 3,3 đến 3,8 nghìn.
**Bài học:** Ước lượng token theo số ký tự dễ lệch. Hai thiết kế độc lập rồi phản biện chéo bắt được lỗi mà một agent đơn lẻ bỏ sót.
**Artefact:** Bảng so sánh các phương án (chụp báo cáo, không lộ đường dẫn).
**Góc người ngoài:** cách làm phổ biến là Một người viết spec rồi tự quyết, hoặc hỏi nhiều câu nhỏ rời rạc; ở đây khác ở Hai thiết kế gần như trùng nhau; phản biện chéo sửa được số token ước lượng và bắt lỗi compact() mà cả hai không nêu lúc đầu. Người đọc muốn biết cách tổ chức để ra quyết định nhanh mà không phải đoán.
