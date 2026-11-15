---
id: 2026-11-02-thiet-ke-mcp-mot-cua-hai
date: 2026-11-02
repo: repo
status: raw
signals: [đảo quyết định có lý do, người duyệt thứ máy soạn]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:2dfb5915#L2983", "claude:2dfb5915#L3027", "claude:2dfb5915#L3060", "claude:2dfb5915#L3098", "claude:2dfb5915#L3144", "claude:2dfb5915#L3170"]
hook: "Hai agent thiết kế riêng, cùng ra đúng 13 tool và cùng bỏ code mode"
tension: khac
sides: ["Hai agent làm độc lập, không biết nhau", "Cùng kết luận 13 tool, cùng bỏ code mode"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Thiết kế MCP một cửa: hai agent độc lập gặp nhau ở 13 tool và bỏ code mode

**Bối cảnh:** Cần gộp hai MCP `kg` và `ohs` thành một. Trước khi chốt chữ ký tool, người dùng yêu cầu brainstorm kỹ.
**Chuyện gì xảy ra:** Hai agent (một chạy model mạnh nhất) thiết kế độc lập rồi phản biện chéo, đều đi tới 13 tool và đều không làm code mode vì giá token định nghĩa và số lượt gọi thêm. Ước lượng định nghĩa tool giảm từ khoảng 6,0 nghìn xuống 3,8–4,4 nghìn token. Hai bên cùng đề xuất `read` do chính server đọc file, vì OHS chỉ đọc được note đã index; người dùng duyệt. Con số token là ước lượng theo số ký tự, chưa đo bằng tokenizer.
**Bài học:** Với bộ tool nhỏ dành cho một client không có shell, meta-tool kiểu tìm-tool-rồi-gọi làm tăng lượt gọi; giữ tool rời là đủ.
**Artefact:** Bảng so sánh phương án A–D với token định nghĩa và số lượt gọi nhóm D.
**Góc người ngoài:** cách làm phổ biến là Hỏi một agent đề xuất rồi duyệt, hoặc tự thiết kế tên tool theo cảm tính. Ít khi đo kích thước danh sách tool; ở đây khác ở Tạo 'hai ý kiến độc lập' bằng cách cô lập ngữ cảnh. Phản biện chéo bắt được lỗi mà không bên nào tự thấy, như số token bị tính thấp hoặc `compact()` mất khoá. Người dùng chỉ phải trả lời vài câu cụ thể thay vì đọc hai báo cáo dài.
