---
id: 2026-10-11-ai-de-xuat-sua-lai-suat-e024
code: M-CKN4
aliases: [M-CKN4]
date: 2026-10-11
repo: repo
status: raw
signals: [nguoi_duyet_may_soan, khac, rang_buoc_thiet_ke]
source: "chat Claude, claude:5a1e7c01"
sessions: ["claude:5a1e7c01"]
captured_by: harvest
hit_by: [hotspot, harvest, outsider]
lines: ["claude:5a1e7c01#L40", "claude:5a1e7c01#L41", "claude:5a1e7c01#L42", "claude:5a1e7c01#L43", "claude:5a1e7c01#L44", "claude:5a1e7c01#L45", "claude:5a1e7c01#L47", "claude:5a1e7c01#L48", "claude:5a1e7c01#L49"]
hook: "AI đòi sửa lãi suất 4,7% lên 6,5%, bảng ngân hàng hôm nay nói khác"
tension: nguoi_dung_may_sai
sides: ["AI cho rằng 4,7% là thấp, đề xuất 6,5% theo mặt bằng cũ", "bảng lãi suất trực tuyến trong ngày cho thấy 4,7%, các ngân hàng khác 4,7 đến 5%"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Người làm bản tin Thư Chủ Nhật đang viết số 48 về quỹ khẩn cấp và cần số lãi suất gửi 12 tháng đúng. AI tin rằng mức 6,5–7%/năm là đúng nên đề xuất sửa 4,7% thành 6,5%. Bảng lãi suất hôm nay cho thấy 4,7%; 6,5–7% là mặt bằng cũ, và AI không có cách tra bảng hôm nay. Chuyện đáng nghe vì một con số sai nhưng nghe hợp lý có thể lọt vào bài; quy tắc mới giữ AI ở vai đánh dấu, người tự tra nguồn."
audience: "người làm nội dung có số liệu tài chính, dùng AI để soạn hoặc kiểm tra bài"
spine_context: "Người làm bản tin Thư Chủ Nhật đang viết số 48 về quỹ khẩn cấp, có đoạn so sánh chỗ để quỹ."
spine_context_lines: ["claude:5a1e7c01#L1"]
spine_want: Muốn số liệu trong phần 3 đúng trước khi gửi.
spine_want_lines: ["claude:5a1e7c01#L38"]
spine_obstacle: "Bài ghi lãi gửi 12 tháng là 4,7%/năm, và AI tin con số đó thấp."
spine_obstacle_lines: ["claude:5a1e7c01#L40", "claude:5a1e7c01#L41"]
spine_turn: "AI tưởng lãi 12 tháng khoảng 6,5–7%/năm; hoá ra bảng lãi suất hôm nay là 4,7%, còn 6,5–7% là mức cuối 2023."
spine_turn_lines: ["claude:5a1e7c01#L41", "claude:5a1e7c01#L42"]
spine_action: "AI đề xuất sửa thành 6,5%, sau đó thêm nguồn và ngày vào bài, rồi thêm quy tắc vào sổ tay: AI chỉ đánh dấu số lãi suất, giá, tỉ giá để người tự kiểm tra."
spine_action_lines: ["claude:5a1e7c01#L41", "claude:5a1e7c01#L44", "claude:5a1e7c01#L45", "claude:5a1e7c01#L47", "claude:5a1e7c01#L49"]
spine_outcome: "Bài giữ 4,7% kèm nguồn và ngày; sổ tay có quy tắc mới."
spine_outcome_lines: ["claude:5a1e7c01#L46", "claude:5a1e7c01#L48"]
spine_takeaway: "Với số liệu đổi theo thời gian, AI không có dữ liệu hôm nay. Hãy ghi quy tắc để AI chỉ đánh dấu, còn người tự tra nguồn."
spine_takeaway_lines: ["claude:5a1e7c01#L43", "claude:5a1e7c01#L44"]
completeness: 7
---

# AI đề xuất sửa lãi suất từ 4,7% lên 6,5%, người làm tài chính bác vì đó là số cũ

**Góc kể:** Người làm bản tin Thư Chủ Nhật đang viết số 48 về quỹ khẩn cấp và cần số lãi suất gửi 12 tháng đúng. AI tin rằng mức 6,5–7%/năm là đúng nên đề xuất sửa 4,7% thành 6,5%. Bảng lãi suất hôm nay cho thấy 4,7%; 6,5–7% là mặt bằng cũ, và AI không có cách tra bảng hôm nay. Chuyện đáng nghe vì một con số sai nhưng nghe hợp lý có thể lọt vào bài; quy tắc mới giữ AI ở vai đánh dấu, người tự tra nguồn.
**Bối cảnh:** Bài nháp về quỹ khẩn cấp có một con số lãi suất gửi 12 tháng. Chủ bản tin là người kiểm tra số liệu cuối cùng trước khi gửi.
**Chuyện gì xảy ra:** Agent cho rằng lãi suất 4,7%/năm ở bài là thấp và đề xuất sửa thành khoảng 6,5%/năm, dựa trên mặt bằng cũ. Chủ bản tin mở bảng lãi suất trực tuyến của một ngân hàng lớn ngay trong ngày và thấy 4,7%, các ngân hàng khác quanh 4,7 đến 5%. Agent thừa nhận không có cách kiểm tra bảng hôm nay, nên con số đề xuất sai gần 2 điểm phần trăm. Sau đó con số được ghi nguồn kèm ngày, và quy tắc mới được thêm vào sổ tay giọng văn: AI chỉ đánh dấu [KIỂM TRA] cho số lãi suất, giá, tỉ giá, không đề xuất số thay thế.
**Bài học:** Với số liệu thay đổi theo thời gian, máy không có dữ liệu của hôm nay; hãy viết quy tắc để máy chỉ đánh dấu và người tự tra nguồn.
**Artefact:** Ảnh chụp bảng lãi suất có hiển thị ngày, che số tài khoản hoặc thông tin đăng nhập nếu có; hoặc ảnh dòng quy tắc mới trong sổ tay.
**Góc người ngoài:** cách làm phổ biến là Với AI, lỗi kiểu này thường được che bằng một con số khác nghe hợp lý. Ít người ghi lại quy tắc cấm AI bịa số trong tài liệu dự án; ở đây khác ở Biến một lần sai thành quy tắc bền trong file hướng dẫn, để lần sau mọi phiên làm việc đều đọc được. Người đọc sẽ muốn biết cách viết quy tắc cho AI như vậy.
