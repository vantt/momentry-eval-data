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
sides: ["15 món bán chậm chỉ góp 6,2 triệu lãi cả năm", "6 món đầu ôm 71% tổng lãi gộp"]
strength: 1
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một tiệm bánh ở Đà Lạt đang xem lại cả năm bán hàng để tính năm sau. Bản phân tích ban đầu cho thấy tháng 2 bán thấp, nhưng chủ tiệm biết tháng Tết mới là lúc đông khách nhất. Hoá ra file ghi ngày trước tháng nên cách đọc ban đầu đã làm lệch cả bức tranh. Ai xử lý số liệu xuất từ phần mềm bán hàng nên kiểm tra thứ tự ngày/tháng trước khi tin xu hướng theo tháng."
audience: dev dùng AI để xử lý số liệu xuất từ phần mềm bán hàng
spine_context: "Một tiệm bánh ở Đà Lạt có 48 món, đang xem lại cả năm bán hàng để tính năm sau."
spine_context_lines: ["claude:5a1e7c05#L1", "claude:5a1e7c05#L24"]
spine_want: Muốn biết món nào lời nhất để bớt việc bếp.
spine_want_lines: ["claude:5a1e7c05#L24"]
spine_obstacle: "File ngày xuất từ KiotViet là ngày/tháng, nhưng cách đọc ban đầu làm tháng 2 có vẻ thấp."
spine_obstacle_lines: ["claude:5a1e7c05#L13", "claude:5a1e7c05#L21"]
spine_turn: Tưởng tháng 2 bán thấp; hoá ra tháng 2 là tháng bán nhiều nhất vì khách đặt bánh biếu trước Tết.
spine_turn_lines: ["claude:5a1e7c05#L13", "claude:5a1e7c05#L21"]
spine_action: Ghi chú định dạng ngày/tháng của file KiotViet vào ghi-chu.txt.
spine_action_lines: ["claude:5a1e7c05#L22", "claude:5a1e7c05#L23"]
spine_outcome: "Phân tích lại theo món: 6 món chiếm khoảng 71% lãi gộp; 15 món bán chậm cộng lại chỉ 6,2 triệu. Chủ tiệm quyết định cắt 15 món và có 15 dòng trong mon-cat.txt."
spine_outcome_lines: ["claude:5a1e7c05#L29", "claude:5a1e7c05#L30", "claude:5a1e7c05#L32"]
spine_takeaway: "Trước khi đọc xu hướng theo tháng, kiểm tra thứ tự ngày/tháng trong file xuất."
spine_takeaway_lines: ["claude:5a1e7c05#L21"]
completeness: 7
---

# Sáu món chiếm gần ba phần tư lãi gộp, cắt 15 món bán chậm

**Góc kể:** Một tiệm bánh ở Đà Lạt đang xem lại cả năm bán hàng để tính năm sau. Bản phân tích ban đầu cho thấy tháng 2 bán thấp, nhưng chủ tiệm biết tháng Tết mới là lúc đông khách nhất. Hoá ra file ghi ngày trước tháng nên cách đọc ban đầu đã làm lệch cả bức tranh. Ai xử lý số liệu xuất từ phần mềm bán hàng nên kiểm tra thứ tự ngày/tháng trước khi tin xu hướng theo tháng.
**Bối cảnh:** Chủ tiệm có 48 món và muốn biết món nào lời để bớt việc bếp. Agent ghép lịch sử hoá đơn chi tiết với file giá vốn từng món.
**Chuyện gì xảy ra:** Sáu món đầu làm ra khoảng 71% tổng lãi gộp cả năm. Mười lăm món bán chậm nhất cộng lại chỉ lãi 6,2 triệu cả năm. Chủ tiệm quyết định cắt 15 món và agent xuất danh sách ra file cho bếp. Agent đề nghị giữ bánh flan kiểu đặt trước vì có khách quen hỏi.
**Bài học:** Xếp món theo lãi gộp rồi cộng dồn thường cho thấy đuôi bảng ít lãi, nhưng nên kiểm tra thêm công làm sáng và món khách đặc biệt quan tâm trước khi cắt.
**Artefact:** Bảng top món theo lãi gộp và tỷ lệ cộng dồn, che giá vốn chi tiết nếu cần.
**Góc người ngoài:** cách làm phổ biến là Thường người ta chỉ đưa bảng xếp hạng hoặc con số, không nói đánh đổi cụ thể; ở đây khác ở Câu trả lời được viết để người ra quyết định dùng ngay, nêu rõ cái được và cái mất. Người đọc sẽ muốn bắt chước cách trình bày này.
