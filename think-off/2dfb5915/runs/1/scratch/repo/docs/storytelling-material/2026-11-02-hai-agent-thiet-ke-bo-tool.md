---
id: 2026-11-02-hai-agent-thiet-ke-bo-tool
date: 2026-11-02
repo: repo
status: raw
signals: [người duyệt thứ máy soạn]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:2dfb5915#L3029", "claude:2dfb5915#L3060", "claude:2dfb5915#L3088", "claude:2dfb5915#L3100", "claude:2dfb5915#L3110", "claude:2dfb5915#L3170"]
hook: "Hai agent chọn 13 tool và bỏ phương án code mode"
tension: none
sides: []
strength: 0
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Hai agent thiết kế bộ tool MCP độc lập, rồi phản biện chéo

**Bối cảnh:** MCP server phải gọn cho Claude Desktop. Hai agent viết thiết kế độc lập, sau đó phản biện chéo, rồi người dùng chốt.
**Chuyện gì xảy ra:** Hai bên đồng ý 13 tool. read do pkm tự đọc file, không đi qua OHS, vì OHS không đọc được note khi đang index. Phương án code mode bị từ chối vì Claude Desktop không có shell, còn 13 tool thì không cần meta tool tìm kiếm. Người dùng đồng ý phương án read tự đọc.
**Bài học:** Cho hai agent thiết kế độc lập rồi buộc phản biện chéo. Chỗ trùng ý ít cần người duyệt. Chỗ lệch mới là nơi người phải chọn.
**Artefact:** Bảng so sánh các phương án A đến D với ước lượng token và số lượt gọi.
**Góc người ngoài:** cách làm phổ biến là Thường người dùng hỏi một AI, nhận một đáp án rồi làm theo, hoặc tự so hai đáp án bằng cảm tính; hiếm ai bắt các bên tự chất vấn nhau bằng bằng chứng; ở đây khác ở Người đọc muốn biết cách có được thiết kế đã được thử từ nhiều góc mà không tốn thêm công người dùng; phiên này còn tách các điểm đồng ý và không đồng ý ra rõ ràng.
