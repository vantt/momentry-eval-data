---
id: 2026-11-02-doi-co-che-tim-kiem-mcp
date: 2026-11-02
repo: repo
status: raw
signals: [đảo quyết định có lý do, người duyệt thứ máy soạn]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:2dfb5915#L2983", "claude:2dfb5915#L2991", "claude:2dfb5915#L3029", "claude:2dfb5915#L3060", "claude:2dfb5915#L3088", "claude:2dfb5915#L3170"]
hook: "Hai agent độc lập, cùng một thiết kế 13 tool, cùng từ chối code mode"
tension: tuong_ma_hoa_ra
sides: ["Hai agent làm riêng, tưởng sẽ ra hai hướng khác nhau", "Cả hai đi đến đúng một thiết kế, chỉ khác cách đọc file"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đổi cơ chế tìm kiếm MCP: hai agent độc lập đi đến cùng một thiết kế và từ chối code mode

**Bối cảnh:** Người dùng muốn gộp hai MCP kg và ohs thành một. Hai agent thiết kế riêng, không xem bài của nhau.
**Chuyện gì xảy ra:** Cả hai đề xuất bộ 13 tool và đều từ chối code mode vì Claude Desktop không có shell và không có sandbox. Ước tính token định nghĩa giảm từ khoảng 6 nghìn xuống 4,4 nghìn. Hai bên khác nhau ở chỗ read: một bên chuyển sang OHS, một bên tự đọc file; người dùng chọn tự đọc.
**Bài học:** Mời hai agent thiết kế độc lập rồi phản biện chéo cho kết quả tốt hơn một agent, và việc từ chối một cơ chế cũng cần lý do cụ thể.
**Artefact:** Bảng so sánh các phương án với số token và số lượt gọi.
**Góc người ngoài:** cách làm phổ biến là Dev thường hỏi một AI một lần rồi chấp nhận kết quả, hoặc tự so hai câu trả lời trong đầu. Ít người cố ý buộc hai bản cạnh tranh nhau trước khi quyết; ở đây khác ở Hai agent đi đến cùng một kết luận (bỏ code mode, giữ tool rời), nên mức tin cậy cao hơn một bản đơn lẻ. Người đọc sẽ muốn biết khi nào đáng bỏ công làm vậy và làm sao để các bên không bị ảnh hưởng bởi nhau.
