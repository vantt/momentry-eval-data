---
id: 2026-10-31-cong-cu-tra-phi-lot-vao-f60d
code: M-J6W5
aliases: [M-J6W5]
date: 2026-10-31
repo: repo
status: raw
signals: [dao_quyet_dinh]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:f0bf048d#L1601", "claude:f0bf048d#L1620", "claude:f0bf048d#L1633", "claude:f0bf048d#L1635"]
hook: "Công cụ trả phí lọt vào plan dù khách chưa mua"
tension: cam_ma_van_lot
sides: ["Bộ lọc đã chặn add-on chưa mua", "Nhánh workspace chưa tồn tại bỏ qua bộ lọc"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án đóng gói các vai marketing thành bộ agent cho từng khách, và người làm muốn mỗi khách chỉ nhận đúng công cụ trả phí họ đã mua. Họ tưởng bộ lọc add-on đã chặn công cụ cho mọi khách chưa mua, nhưng nhánh xử lý workspace mới lại bỏ qua bộ lọc đó, khiến khách chưa mua vẫn được tạo DataForSEO. Ai viết cấu hình có nhiều nhánh cũng dễ gặp lỗi kiểu này: một bộ lọc chỉ phủ được một nhánh."
audience: "dev viết cấu hình có nhiều nhánh, hoặc bán công cụ theo gói"
spine_context: "Dự án đóng gói các vai marketing (SEO, nội dung, quảng cáo) thành bộ agent cho từng khách; người làm đang đóng gói từng vai trước."
spine_context_lines: ["claude:f0bf048d#L7", "claude:f0bf048d#L1282"]
spine_want: "Mỗi khách chỉ nhận công cụ trả phí mà họ đã mua, nhưng vẫn hỗ trợ từ miễn phí đến trả tiền."
spine_want_lines: ["claude:f0bf048d#L1439", "claude:f0bf048d#L1603"]
spine_obstacle: "Khi workspace chưa tồn tại, plan chạy một nhánh khác không qua bộ lọc add-on."
spine_obstacle_lines: ["claude:f0bf048d#L1603"]
spine_turn: "Tưởng bộ lọc add-on chặn mọi khách chưa mua; hoá ra nhánh workspace mới bỏ qua nó, và khách chưa mua vẫn được tạo DataForSEO."
spine_turn_lines: ["claude:f0bf048d#L1603", "claude:f0bf048d#L1619"]
spine_action: "Thêm bộ lọc vào nhánh đó, rồi chạy plan ba trường hợp: có add-on, không có, và workspace đã có sẵn."
spine_action_lines: ["claude:f0bf048d#L1620", "claude:f0bf048d#L1625"]
spine_outcome: "Plan đúng: PageSpeed được tạo và gắn cho agent; DataForSEO không được tạo cho khách chưa mua."
spine_outcome_lines: ["claude:f0bf048d#L1623", "claude:f0bf048d#L1635"]
spine_takeaway: "Khi cấu hình có nhiều nhánh, mỗi nhánh phải dùng cùng một bộ lọc, và phải kiểm từng nhánh riêng."
spine_takeaway_lines: ["claude:f0bf048d#L1619"]
completeness: 7
---

# Công cụ trả phí lọt vào plan khi khách chưa mua

**Góc kể:** Dự án đóng gói các vai marketing thành bộ agent cho từng khách, và người làm muốn mỗi khách chỉ nhận đúng công cụ trả phí họ đã mua. Họ tưởng bộ lọc add-on đã chặn công cụ cho mọi khách chưa mua, nhưng nhánh xử lý workspace mới lại bỏ qua bộ lọc đó, khiến khách chưa mua vẫn được tạo DataForSEO. Ai viết cấu hình có nhiều nhánh cũng dễ gặp lỗi kiểu này: một bộ lọc chỉ phủ được một nhánh.
**Bối cảnh:** Sau khi thêm add-on DataForSEO, plan cho một khách chưa mua vẫn tạo server dataforseo.
**Chuyện gì xảy ra:** Plan có một nhánh riêng cho workspace chưa tồn tại và nhánh đó bỏ qua bộ lọc add-on. Agent tìm ra nhánh này, lọc add-on chưa mua ở cả hai nhánh, rồi kiểm plan trên ba trường hợp: có add-on, không có, và workspace đã tồn tại. Kết quả đúng như mong đợi: PageSpeed được gắn, DataForSEO không được tạo.
**Bài học:** Mọi nhánh của plan phải dùng cùng một bộ lọc. Kiểm từng nhánh riêng.
**Artefact:** Kết quả plan hai lần: có và không có add-on.
