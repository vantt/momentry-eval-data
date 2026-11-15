---
id: 2026-11-02-compact-xoa-khoa-null-loi-ohs
date: 2026-11-02
repo: repo
status: raw
signals: [nguyên nhân bất ngờ]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L3100", "claude:2dfb5915#L3110"]
hook: "Test kiểm 5 khoá đều xanh, nhưng agent chỉ nhận được 3"
tension: cam_ma_van_lot
sides: ["test kiểm đủ 5 khoá và đều qua", "hàm compact xoá 2 khoá null sau test, agent chỉ thấy 3"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Compact() xoá khoá null, lỗi ohs_not_ready chỉ còn 3 khoá

**Bối cảnh:** Theo hợp đồng, lỗi ohs_not_ready phải có đủ 5 khoá.
**Chuyện gì xảy ra:** Hàm compact của server lọc mọi khoá có giá trị null. Khi OHS ở trạng thái starting, progress và eta_s là null nên bị bỏ, agent chỉ thấy 3 khoá. Test kiểm 5 khoá chạy trước compact nên không bắt được lỗi. Hai agent thiết kế cùng xác nhận.
**Bài học:** Test hợp đồng phải kiểm đầu ra cuối, sau mọi lớp lọc, không chỉ kiểm tầng bên trong.
**Artefact:** Không có.
