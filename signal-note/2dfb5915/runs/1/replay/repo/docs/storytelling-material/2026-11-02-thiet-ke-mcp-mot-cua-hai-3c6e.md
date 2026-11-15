---
id: 2026-11-02-thiet-ke-mcp-mot-cua-hai-3c6e
code: M-A8FQ
aliases: [M-A8FQ]
date: 2026-11-02
repo: repo
status: raw
signals: [nguoi_duyet_may_soan, khac, dao_quyet_dinh]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:2dfb5915#L3051", "claude:2dfb5915#L3088", "claude:2dfb5915#L3110", "claude:2dfb5915#L3170"]
hook: "Hai agent độc lập chốt gần giống nhau, người dùng vẫn lệch khỏi plan"
tension: nguoi_dung_may_sai
sides: ["Hai agent đề xuất cùng một thiết kế qua OHS", "Người dùng chọn đọc note trực tiếp vì OHS không thấy note chưa index"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một công cụ giúp Claude Desktop hỏi graph của vault Obsidian đang viết lại lõi bằng Rust và chuẩn bị bộ tool MCP mới. Plan tin rằng tool đọc note có thể chuyển sang OHS, bộ index có sẵn. Hoá ra OHS chỉ đọc được note đã index, nên trong lúc nó khởi động hoặc đang index, agent không đọc được note nào. Người làm nên chú ý vì bất kỳ tool nào đẩy việc đọc qua một service đang index đều thừa hưởng khoảng trống này."
audience: dev xây tool cho AI đọc dữ liệu qua một service đang index
spine_context: "Một công cụ giúp Claude Desktop hỏi graph của vault Obsidian, đang viết lại lõi bằng Rust và chuẩn bị bộ tool MCP mới."
spine_context_lines: [profile, "claude:2dfb5915#L11"]
spine_want: Cố định chữ ký bộ tool MCP một cửa trước khi làm.
spine_want_lines: ["claude:2dfb5915#L3027"]
spine_obstacle: "OHS chỉ đọc được note đã index, nên khi nó khởi động hoặc đang index thì không đọc được note nào."
spine_obstacle_lines: ["claude:2dfb5915#L3160"]
spine_turn: Plan tưởng tool đọc note chuyển sang OHS là đủ; hoá ra OHS không đọc được note chưa index.
spine_turn_lines: ["claude:2dfb5915#L3145", "claude:2dfb5915#L3160"]
spine_action: "Hai agent độc lập thiết kế rồi phản biện chéo, đề nghị pkm tự đọc file; người làm đồng ý."
spine_action_lines: ["claude:2dfb5915#L3088", "claude:2dfb5915#L3170"]
spine_outcome: "Bộ 13 tool được giao làm trên nhánh phase 17; ước lượng định nghĩa tool giảm từ khoảng 6,0 nghìn xuống 4,4 nghìn token, chưa đo bằng tokenizer."
spine_outcome_lines: ["claude:2dfb5915#L3051", "claude:2dfb5915#L3180"]
spine_takeaway: "Khi thiết kế, tách phần đọc khỏi phần index; và việc lệch khỏi plan cần người duyệt chốt."
spine_takeaway_lines: ["claude:2dfb5915#L3100", "claude:2dfb5915#L3170"]
completeness: 7
---

# Thiết kế MCP một cửa: hai agent độc lập ra kết luận gần như giống nhau, người dùng chọn đọc note trực tiếp thay vì qua OHS

**Góc kể:** Một công cụ giúp Claude Desktop hỏi graph của vault Obsidian đang viết lại lõi bằng Rust và chuẩn bị bộ tool MCP mới. Plan tin rằng tool đọc note có thể chuyển sang OHS, bộ index có sẵn. Hoá ra OHS chỉ đọc được note đã index, nên trong lúc nó khởi động hoặc đang index, agent không đọc được note nào. Người làm nên chú ý vì bất kỳ tool nào đẩy việc đọc qua một service đang index đều thừa hưởng khoảng trống này.
**Bối cảnh:** Plan ghi tool read sẽ chuyển tiếp sang OHS. Người dùng muốn thiết kế kỹ trước khi cố định chữ ký tool.
**Chuyện gì xảy ra:** Hai agent độc lập đề xuất 13 tool, bỏ chế độ code mode, và đề nghị pkm tự đọc file. Ước lượng token định nghĩa giảm từ khoảng 6.0k xuống 4.4k, theo độ dài chuỗi chứ chưa đo bằng tokenizer. Sau phản biện chéo, người dùng đồng ý read tự đọc file vì OHS không đọc được note chưa index, lệch khỏi plan.
**Bài học:** Để hai bản thiết kế độc lập rồi phản biện chéo rất có ích; và một lựa chọn trái plan cần được người duyệt chốt, không tự quyết.
**Artefact:** Bảng so sánh các phương án (token, số lượt gọi, công sức). Ước lượng cần ghi rõ là chưa đo.
