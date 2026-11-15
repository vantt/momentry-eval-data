---
id: 2026-11-02-mot-dong-dinh-dang-ngay-lam-3eb3
code: M-PS16
aliases: [M-PS16]
date: 2026-11-02
repo: repo
status: raw
signals: [so_truoc_so_sau, nguyen_nhan_bat_ngo, dao_quyet_dinh, nguoi_duyet_may_soan]
source: "chat Claude, claude:5a1e7c05"
sessions: ["claude:5a1e7c05"]
captured_by: harvest
hit_by: [hotspot, harvest, outsider]
lines: ["claude:5a1e7c05#L10", "claude:5a1e7c05#L11", "claude:5a1e7c05#L12", "claude:5a1e7c05#L13", "claude:5a1e7c05#L14", "claude:5a1e7c05#L15", "claude:5a1e7c05#L16", "claude:5a1e7c05#L17", "claude:5a1e7c05#L18", "claude:5a1e7c05#L19", "claude:5a1e7c05#L20"]
hook: "Một dòng định dạng ngày suýt khiến chủ tiệm nghỉ đúng mùa Tết"
tension: nguoi_dung_may_sai
sides: ["Agent đọc nhầm ngày, khuyên nghỉ Tết vì tháng 2 chỉ 18,9 triệu", "Chủ tiệm phản đối, đọc đúng thì tháng 2 đạt 168,3 triệu, cao nhất năm"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một chủ tiệm bánh ở Đà Lạt xuất dữ liệu bán hàng cả năm để lên kế hoạch cho năm sau, và người trợ lý AI gộp hai file rồi tính doanh thu theo tháng. AI thấy tháng 2 thấp nhất năm, chỉ 18,9 triệu, nên khuyên nghỉ hai tuần quanh Tết. Hoá ra nó đọc ngày kiểu tháng/ngày trong khi file ghi ngày/tháng, nên hơn nửa hoá đơn bị bỏ và tháng 2 thật ra đạt 168,3 triệu, cao nhất năm. Ai dùng AI để tổng hợp số liệu nên đếm số dòng bị bỏ trước khi tin một con số."
audience: người dùng AI để xử lý bảng số liệu
spine_context: Chủ tiệm bánh ở Đà Lạt muốn xem lại doanh thu cả năm từ phần mềm bán hàng để tính kế hoạch năm sau.
spine_context_lines: ["claude:5a1e7c05#L1", "claude:5a1e7c05#L8"]
spine_want: Muốn xem doanh thu từng tháng để tính chuyện năm sau.
spine_want_lines: ["claude:5a1e7c05#L1", "claude:5a1e7c05#L9"]
spine_obstacle: "Cột ngày ghi theo ngày/tháng nhưng cách đọc mặc định là tháng/ngày, nên 15.240 hoá đơn không đọc được ngày."
spine_obstacle_lines: ["claude:5a1e7c05#L11", "claude:5a1e7c05#L17"]
spine_turn: "Tưởng tháng 2 thấp vì nghỉ Tết nên khuyên nghỉ hẳn hai tuần; hoá ra lỗi đọc ngày làm sai số, tháng 2 thật ra cao nhất năm."
spine_turn_lines: ["claude:5a1e7c05#L12", "claude:5a1e7c05#L20"]
spine_action: "Đọc lại cột ngày theo ngày/tháng, tính lại doanh thu và ghi quy tắc vào file ghi chú."
spine_action_lines: ["claude:5a1e7c05#L18", "claude:5a1e7c05#L22"]
spine_outcome: "Tháng 2/2026 đạt 168,3 triệu, cao nhất năm; các tháng thường 70–95 triệu."
spine_outcome_lines: ["claude:5a1e7c05#L20"]
spine_takeaway: "Trước khi tin một bảng tổng hợp, đếm số dòng bị bỏ khi đọc ngày; số lượng lớn không đọc được là dấu hiệu sai định dạng."
spine_takeaway_lines: ["claude:5a1e7c05#L14", "claude:5a1e7c05#L17"]
completeness: 7
---

# Một dòng định dạng ngày làm mất nửa số hoá đơn và suýt khuyên nghỉ đúng mùa Tết

**Góc kể:** Một chủ tiệm bánh ở Đà Lạt xuất dữ liệu bán hàng cả năm để lên kế hoạch cho năm sau, và người trợ lý AI gộp hai file rồi tính doanh thu theo tháng. AI thấy tháng 2 thấp nhất năm, chỉ 18,9 triệu, nên khuyên nghỉ hai tuần quanh Tết. Hoá ra nó đọc ngày kiểu tháng/ngày trong khi file ghi ngày/tháng, nên hơn nửa hoá đơn bị bỏ và tháng 2 thật ra đạt 168,3 triệu, cao nhất năm. Ai dùng AI để tổng hợp số liệu nên đếm số dòng bị bỏ trước khi tin một con số.
**Bối cảnh:** Chủ tiệm bánh xuất dữ liệu bán hàng cả năm từ phần mềm KiotViet để lên kế hoạch năm sau. Agent gộp hai file và tính doanh thu theo tháng.
**Chuyện gì xảy ra:** Agent đọc cột ngày theo kiểu tháng/ngày trong khi KiotViet ghi ngày/tháng, nên 15.240 trên 28.197 hoá đơn (hơn một nửa) không đọc được và bị bỏ, còn ngày 03/11 bị đọc thành tháng 3. Bảng sai cho tháng 2 chỉ 18,9 triệu, thấp nhất năm, và agent khuyên nghỉ hai tuần quanh Tết. Chủ tiệm phản đối vì tháng Tết bán nhiều nhất; khi đọc đúng định dạng, tháng 2 đạt 168,3 triệu, cao nhất năm, còn các tháng thường là 70-95 triệu. Agent ghi quy tắc định dạng ngày vào file ghi chú.
**Bài học:** Trước khi tin một bảng tổng hợp, hãy đếm số dòng bị bỏ khi parse ngày; số lượng lớn không đọc được là dấu hiệu sai định dạng, không phải dữ liệu thiếu.
**Artefact:** Bảng doanh thu theo tháng trước và sau khi sửa định dạng ngày, đã che tên file, đường dẫn và tên tiệm.
**Góc người ngoài:** cách làm phổ biến là Nhiều agent hoặc người làm phân tích sẽ giải thích thêm, hoặc chỉ sửa câu chữ mà không xem lại dữ liệu gốc; ở đây khác ở Agent kiểm tra nguyên nhân bằng dữ liệu cụ thể trước khi đổi kết luận, và nói rõ hậu quả nếu làm theo lời khuyên sai. Người đọc sẽ muốn biết cách làm này.
