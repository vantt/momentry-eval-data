---
id: 2026-11-02-compact-xoa-khoa-null-loi-ohs
date: 2026-11-02
repo: repo
status: raw
signals: [nguyên nhân bất ngờ]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:2dfb5915#L3060", "claude:2dfb5915#L3110"]
hook: "Hàm dọn gọn xoá khoá null, lỗi chỉ còn 3 trên 5 khoá"
tension: giup_ma_hai
sides: ["compact để dọn gọn đầu ra", "lỗi mất 2 khoá, test vẫn qua"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Compact() xoá khoá null: lỗi ohs_not_ready chỉ còn 3/5 khoá

**Bối cảnh:** Hợp đồng lỗi yêu cầu 5 khoá khi OHS chưa sẵn sàng.
**Chuyện gì xảy ra:** Hàm compact bỏ mọi khoá null. Khi OHS ở trạng thái starting, progress và eta_s là null, nên agent chỉ thấy 3 khoá. Test 5 khoá kiểm trước khi compact nên không bắt được. Sửa: miễn compact cho lỗi ohs_not_ready, và thêm test ở tầng MCP.
**Bài học:** Test ở đúng tầng: lỗi xuất hiện sau lớp biến đổi thì test ở lớp ngoài cùng.
**Artefact:** Không.
**Góc người ngoài:** cách làm phổ biến là Thường hỏi một lần một mô hình rồi dùng luôn thiết kế đầu tiên, hoặc tự cân nhắc trong đầu; ở đây khác ở Giao diện công cụ của MCP quyết định số token mỗi phiên và số lượt gọi, nên đáng bỏ công. Hai thiết kế độc lập hội tụ ở cùng kết luận, và vòng phản biện cũng lòi ra lỗi thật (khoá null bị xoá, số token bị tính thấp). User chỉ phải chốt ba câu hỏi.
