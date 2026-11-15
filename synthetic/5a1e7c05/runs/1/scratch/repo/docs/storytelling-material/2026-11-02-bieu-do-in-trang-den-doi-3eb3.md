---
id: 2026-11-02-bieu-do-in-trang-den-doi-3eb3
code: M-N38C
aliases: [M-N38C]
date: 2026-11-02
repo: repo
status: raw
signals: [người duyệt thứ máy soạn, có thứ nhìn thấy được]
source: "chat Claude, claude:5a1e7c05"
sessions: ["claude:5a1e7c05"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:5a1e7c05#L47", "claude:5a1e7c05#L48", "claude:5a1e7c05#L49", "claude:5a1e7c05#L50", "claude:5a1e7c05#L51", "claude:5a1e7c05#L52", "claude:5a1e7c05#L53"]
hook: "Cam nhạt trên màn hình thành vệt mờ khi in trắng đen"
tension: tuong_ma_hoa_ra
sides: ["Biểu đồ màu cam trông rõ trên màn hình", "In trắng đen thì cột gần như biến mất"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một chủ tiệm bánh ở Đà Lạt nhờ agent vẽ biểu đồ doanh thu theo tháng để in dán ở bếp, yêu cầu chữ to và màu dễ nhìn. Agent chọn màu cam, tưởng là dễ nhìn, nhưng chủ tiệm báo cam hơi nhạt khi in trắng đen. Agent vẽ lại bằng nâu đậm và thêm số trên mỗi cột. Với thứ sẽ in ra giấy, kiểm tra độ tương phản đen trắng trước khi chốt màu là việc đáng làm."
audience: dev dùng AI để làm biểu đồ hoặc tài liệu sẽ in ra giấy
spine_context: "Chủ tiệm bánh ở Đà Lạt muốn xem lại doanh thu cả năm để tính năm sau, và cần biểu đồ doanh thu theo tháng để in dán ở bếp."
spine_context_lines: ["claude:5a1e7c05#L1", "claude:5a1e7c05#L47"]
spine_want: "Biểu đồ chữ to, màu dễ nhìn, in ra dán được."
spine_want_lines: ["claude:5a1e7c05#L47"]
spine_obstacle: Màu cam vẽ ra hơi nhạt khi in trắng đen.
spine_obstacle_lines: ["claude:5a1e7c05#L50"]
spine_turn: Tưởng màu cam là dễ nhìn; hoá ra cam nhạt khi in đen trắng.
spine_turn_lines: ["claude:5a1e7c05#L47", "claude:5a1e7c05#L48", "claude:5a1e7c05#L50"]
spine_action: "Vẽ lại bằng màu nâu đậm #5a3420 và ghi số triệu đồng trên đầu mỗi cột."
spine_action_lines: ["claude:5a1e7c05#L51"]
spine_outcome: "Ảnh 1600x900. Agent báo cột nâu đậm vẫn rõ khi in trắng đen, nhưng chưa có bản in được kiểm tra."
spine_outcome_lines: ["claude:5a1e7c05#L52", "claude:5a1e7c05#L53"]
spine_takeaway: "Với thứ sẽ in ra giấy, kiểm tra độ tương phản khi in đen trắng trước khi chốt màu."
spine_takeaway_lines: ["claude:5a1e7c05#L50"]
completeness: 7
---

# Biểu đồ in trắng đen: đổi từ cam nhạt sang nâu đậm và ghi số trên cột

**Góc kể:** Một chủ tiệm bánh ở Đà Lạt nhờ agent vẽ biểu đồ doanh thu theo tháng để in dán ở bếp, yêu cầu chữ to và màu dễ nhìn. Agent chọn màu cam, tưởng là dễ nhìn, nhưng chủ tiệm báo cam hơi nhạt khi in trắng đen. Agent vẽ lại bằng nâu đậm và thêm số trên mỗi cột. Với thứ sẽ in ra giấy, kiểm tra độ tương phản đen trắng trước khi chốt màu là việc đáng làm.
**Bối cảnh:** Chủ tiệm muốn biểu đồ doanh thu theo tháng để in dán ở bếp, yêu cầu chữ to và màu dễ nhìn.
**Chuyện gì xảy ra:** Agent vẽ lần đầu bằng màu cam, chữ cỡ 18, chưa có nhãn số. Chủ tiệm báo màu cam nhạt khi in trắng đen và yêu cầu ghi số triệu trên đầu mỗi cột. Agent vẽ lại bằng màu nâu đậm #5a3420 có nhãn số, ảnh 1600x900. Vòng sửa chỉ gồm hai lần chạy script.
**Bài học:** Với thứ sẽ được in ra giấy, hãy kiểm tra độ tương phản khi in đen trắng trước khi chốt màu, vì màu đẹp trên màn hình có thể nhạt đi khi in.
**Artefact:** Ảnh biểu đồ cột doanh thu theo tháng (bản nâu đậm có nhãn số), không hiện tên tiệm.
**Góc người ngoài:** cách làm phổ biến là Người làm biểu đồ thường giữ nguyên màu đã chọn, hoặc chỉ đổi màu mà không kiểm tra điều kiện in ấn; ở đây khác ở Agent hiểu mục đích sử dụng thực tế (in, dán ở bếp) và điều chỉnh cho đúng môi trường đó. Người đọc sẽ hỏi làm sao agent nghĩ tới điều này.
