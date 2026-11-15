---
id: 2026-11-02-compact-xoa-khoa-null-lam-ohs
date: 2026-11-02
repo: repo
status: raw
signals: [nguyên nhân bất ngờ]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L3088", "claude:2dfb5915#L3110"]
hook: "Test 5 khoá đều xanh, nhưng agent thật chỉ nhận được 3 khoá"
tension: cam_ma_van_lot
sides: ["Test 5 khoá đã chạy và qua", "Agent thật chỉ thấy 3 khoá"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# compact() xoá khoá null làm ohs_not_ready còn 3 trên 5 khoá

**Bối cảnh:** Kết quả MCP đi qua compact để bỏ khoá rỗng cho gọn.
**Chuyện gì xảy ra:** Ở trạng thái starting, progress và eta_s là null nên bị xoá; agent chỉ thấy 3 khoá trong khi hợp đồng là 5. Test 5 khoá chạy trước compact nên không bắt được lỗi. Hai agent độc lập cùng xác nhận. Sửa: miễn compact cho lỗi ohs_not_ready và thêm test ở tầng MCP.
**Bài học:** Test hợp đồng phải kiểm thứ agent nhận được, sau mọi lớp biến đổi.
**Artefact:** Không có.
