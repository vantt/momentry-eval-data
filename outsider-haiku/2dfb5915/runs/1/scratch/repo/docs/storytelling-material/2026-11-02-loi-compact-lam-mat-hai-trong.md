---
id: 2026-11-02-loi-compact-lam-mat-hai-trong
date: 2026-11-02
repo: repo
status: raw
signals: [Nguyên nhân bất ngờ]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L3088", "claude:2dfb5915#L3100", "claude:2dfb5915#L3117"]
hook: "Test 5 khoá đều xanh, nhưng agent chỉ nhận được 3 khoá"
tension: cam_ma_van_lot
sides: ["Test kiểm đủ 5 khoá đều qua", "Sau khi nén, hai khoá null biến mất, chỉ còn 3"]
strength: 3
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Lỗi `compact()` làm mất hai trong năm khoá của trạng thái OHS 'chưa sẵn sàng'

**Bối cảnh:** Hàm `compact()` bỏ mọi khoá null trong kết quả MCP để giảm token.
**Chuyện gì xảy ra:** Khi OHS ở trạng thái starting/model_missing/broken, `progress` và `eta_s` là null nên bị bỏ, agent chỉ thấy 3 khoá thay vì 5 theo hợp đồng. Test 5 khoá kiểm trước khi compact nên không bắt được. Agent sửa bằng cách miễn compact cho lỗi `ohs_not_ready` và thêm test ở tầng MCP.
**Bài học:** Test hợp đồng phải chạy trên đầu ra cuối cùng gửi đi, không phải trên giá trị trung gian.
**Artefact:** Đoạn JSON trước và sau khi compact (đã che).
