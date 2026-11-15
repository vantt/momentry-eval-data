---
id: 2026-10-11-link-chu-thich-loi-thieu-dau-e024
code: M-4H21
aliases: [M-4H21]
date: 2026-10-11
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:5a1e7c01"
sessions: ["claude:5a1e7c01"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:5a1e7c01#L50", "claude:5a1e7c01#L51", "claude:5a1e7c01#L52", "claude:5a1e7c01#L53", "claude:5a1e7c01#L54", "claude:5a1e7c01#L55", "claude:5a1e7c01#L56", "claude:5a1e7c01#L57", "claude:5a1e7c01#L58", "claude:5a1e7c01#L59"]
hook: "Một dấu hai chấm thiếu suýt đưa link hỏng vào bản gửi"
tension: nho_ma_to
sides: ["Đổi định dạng chú thích chỉ mất hai lượt sửa", "Link thứ ba thiếu dấu ':' sau https, suýt gửi đi hỏng"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Chủ bản tin Thư Chủ Nhật đang viết số 48 về quỹ khẩn cấp và nhờ AI sửa bản nháp. Bản nháp coi lãi suất 6,5–7% là mức hiện tại, nhưng đó là con số cuối 2023; bảng Vietcombank hôm nay chỉ 4,7% cho gửi online 12 tháng. Ai viết bài có số liệu nhờ AI nên để ý, vì AI có thể mang số cũ vào bài mà không ai nhận ra."
audience: người viết bài có số liệu nhờ AI
spine_context: "Chủ bản tin Thư Chủ Nhật đang viết số 48 về quỹ khẩn cấp, nhờ AI đọc và sửa bản nháp."
spine_context_lines: ["claude:5a1e7c01#L1"]
spine_want: "Bài gửi đi có số liệu đúng, và chú thích hiển thị gọn trên MailerLite."
spine_want_lines: ["claude:5a1e7c01#L1", "claude:5a1e7c01#L50"]
spine_obstacle: "Bản nháp dùng con số lãi suất 6,5–7%, trong khi bảng lãi suất hiện nay quanh 4,7%."
spine_obstacle_lines: ["claude:5a1e7c01#L42"]
spine_turn: "Bản nháp coi 6,5–7% là mức hiện tại; hoá ra đó là mức cuối 2023, còn gửi online 12 tháng chỉ 4,7%."
spine_turn_lines: ["claude:5a1e7c01#L42", "claude:5a1e7c01#L44"]
spine_action: "Thêm nguồn cho bài và thêm quy tắc vào style.md: AI không tự điền hay sửa số liệu lãi suất, giá, tỉ giá, chỉ đánh dấu để người làm tự kiểm tra."
spine_action_lines: ["claude:5a1e7c01#L44", "claude:5a1e7c01#L49"]
spine_outcome: "Quy tắc đã được ghi vào style.md; từ nay con số kiểu này chỉ được đánh dấu [KIỂM TRA]."
spine_outcome_lines: ["claude:5a1e7c01#L49"]
spine_takeaway: "Với bài có số lãi suất, giá hay tỉ giá, để AI đánh dấu và tự đối chiếu với bảng hôm nay."
spine_takeaway_lines: ["claude:5a1e7c01#L44"]
completeness: 7
---

# Link chú thích: lỗi thiếu dấu hai chấm được bắt khi đổi định dạng

**Góc kể:** Chủ bản tin Thư Chủ Nhật đang viết số 48 về quỹ khẩn cấp và nhờ AI sửa bản nháp. Bản nháp coi lãi suất 6,5–7% là mức hiện tại, nhưng đó là con số cuối 2023; bảng Vietcombank hôm nay chỉ 4,7% cho gửi online 12 tháng. Ai viết bài có số liệu nhờ AI nên để ý, vì AI có thể mang số cũ vào bài mà không ai nhận ra.
**Bối cảnh:** Chủ bản tin muốn bỏ ba chú thích kiểu [1] [2] [3] vì MailerLite hiển thị xấu, và chuyển thành link đặt ngay trong câu.
**Chuyện gì xảy ra:** Khi đọc lại phần chú thích, agent thấy link thứ ba thiếu dấu hai chấm sau https và sửa ngay khi chuyển. Ba link được gắn vào ba cụm từ trong câu, rồi phần chú thích cuối bài được xoá trong hai lệnh sửa. Việc đổi định dạng chỉ mất hai lượt sửa nhưng suýt đưa một link hỏng vào bản gửi.
**Bài học:** Khi đổi định dạng link, đọc lại từng URL trước khi chuyển; một lỗi nhỏ như thiếu dấu hai chấm sẽ làm link không mở được.
**Artefact:** Danh sách ba link trước và sau khi chuyển, che nếu có thông tin cá nhân trong URL.
