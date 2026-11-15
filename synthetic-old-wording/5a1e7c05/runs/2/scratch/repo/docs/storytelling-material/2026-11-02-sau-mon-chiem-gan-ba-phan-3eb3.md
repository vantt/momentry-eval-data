---
id: 2026-11-02-sau-mon-chiem-gan-ba-phan-3eb3
code: M-3SME
aliases: [M-3SME]
date: 2026-11-02
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:5a1e7c05"
sessions: ["claude:5a1e7c05"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:5a1e7c05#L24", "claude:5a1e7c05#L25", "claude:5a1e7c05#L26", "claude:5a1e7c05#L27", "claude:5a1e7c05#L28", "claude:5a1e7c05#L29", "claude:5a1e7c05#L30", "claude:5a1e7c05#L31", "claude:5a1e7c05#L32", "claude:5a1e7c05#L33"]
hook: "6 món làm ra 71% lãi, 15 món cuối chỉ lãi 6,2 triệu"
tension: it_ma_nhieu
sides: ["6 món đầu chiếm 71% tổng lãi gộp cả năm", "15 món bán chậm cộng lại chỉ lãi 6,2 triệu"]
strength: 1
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Chủ tiệm bánh ở Đà Lạt muốn xem lại cả năm bán hàng từ hai file xuất của KiotViet để tính năm sau. Kết luận ban đầu cho rằng tháng 2 thấp, nhưng chủ tiệm bác ngay: tháng Tết mới là tháng bán nhiều nhất, khách đặt bánh biếu và hộp quà, và file ghi ngày theo ngày/tháng. Chuyện nhỏ này đáng nghe với dev dùng AI, vì đọc sai định dạng ngày trong file xuất thì mọi kết luận theo tháng đều lệch."
audience: dev dùng AI xử lý file số liệu xuất từ phần mềm bán hàng
spine_context: Chủ tiệm bánh ở Đà Lạt muốn xem lại cả năm bán hàng từ hai file xuất của KiotViet để tính năm sau.
spine_context_lines: ["claude:5a1e7c05#L1"]
spine_want: "Xem lại cả năm bán hàng để tính năm sau, và biết món nào lời nhất."
spine_want_lines: ["claude:5a1e7c05#L1", "claude:5a1e7c05#L24"]
spine_obstacle: "File xuất từ KiotViet ghi ngày theo kiểu ngày/tháng, còn chị không rành Excel."
spine_obstacle_lines: ["claude:5a1e7c05#L1", "claude:5a1e7c05#L21"]
spine_turn: "Tưởng tháng 2 thấp; hoá ra tháng Tết là tháng bán nhiều nhất năm, vì file ghi ngày theo ngày/tháng."
spine_turn_lines: ["claude:5a1e7c05#L13", "claude:5a1e7c05#L21"]
spine_action: Ghi rõ trong ghi-chu.txt rằng ngày trong file KiotViet là ngày/tháng.
spine_action_lines: ["claude:5a1e7c05#L21", "claude:5a1e7c05#L22"]
spine_outcome: Ghi chú đã được cập nhật thành công.
spine_outcome_lines: ["claude:5a1e7c05#L23"]
spine_takeaway: "Trước khi kết luận theo tháng, kiểm tra thứ tự ngày/tháng của file xuất từ phần mềm."
spine_takeaway_lines: ["claude:5a1e7c05#L21"]
completeness: 7
---

# Sáu món chiếm gần ba phần tư lãi gộp, cắt 15 món bán chậm

**Góc kể:** Chủ tiệm bánh ở Đà Lạt muốn xem lại cả năm bán hàng từ hai file xuất của KiotViet để tính năm sau. Kết luận ban đầu cho rằng tháng 2 thấp, nhưng chủ tiệm bác ngay: tháng Tết mới là tháng bán nhiều nhất, khách đặt bánh biếu và hộp quà, và file ghi ngày theo ngày/tháng. Chuyện nhỏ này đáng nghe với dev dùng AI, vì đọc sai định dạng ngày trong file xuất thì mọi kết luận theo tháng đều lệch.
**Bối cảnh:** Chủ tiệm có 48 món và muốn biết món nào lời để bớt việc bếp. Agent ghép lịch sử hoá đơn chi tiết với file giá vốn từng món.
**Chuyện gì xảy ra:** Sáu món đầu làm ra khoảng 71% tổng lãi gộp cả năm. Mười lăm món bán chậm nhất cộng lại chỉ lãi 6,2 triệu cả năm. Chủ tiệm quyết định cắt 15 món và agent xuất danh sách ra file cho bếp. Agent đề nghị giữ bánh flan kiểu đặt trước vì có khách quen hỏi.
**Bài học:** Xếp món theo lãi gộp rồi cộng dồn thường cho thấy đuôi bảng ít lãi, nhưng nên kiểm tra thêm công làm sáng và món khách đặc biệt quan tâm trước khi cắt.
**Artefact:** Bảng top món theo lãi gộp và tỷ lệ cộng dồn, che giá vốn chi tiết nếu cần.
**Góc người ngoài:** cách làm phổ biến là Thường người ta chỉ đưa bảng xếp hạng hoặc con số, không nói đánh đổi cụ thể; ở đây khác ở Câu trả lời được viết để người ra quyết định dùng ngay, nêu rõ cái được và cái mất. Người đọc sẽ muốn bắt chước cách trình bày này.
