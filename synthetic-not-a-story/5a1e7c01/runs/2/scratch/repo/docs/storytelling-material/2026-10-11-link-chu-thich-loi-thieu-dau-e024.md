---
id: 2026-10-11-link-chu-thich-loi-thieu-dau-e024
code: M-4H21
aliases: [M-4H21]
date: 2026-10-11
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:5a1e7c01"
sessions: ["claude:5a1e7c01"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:5a1e7c01#L50", "claude:5a1e7c01#L51", "claude:5a1e7c01#L52", "claude:5a1e7c01#L53", "claude:5a1e7c01#L54", "claude:5a1e7c01#L55", "claude:5a1e7c01#L56", "claude:5a1e7c01#L57", "claude:5a1e7c01#L58", "claude:5a1e7c01#L59"]
hook: "Đổi định dạng link, suýt gửi đi một link thiếu dấu hai chấm"
tension: nho_ma_to
sides: ["một dấu hai chấm bị thiếu sau https ở link thứ ba", "suýt đưa link hỏng vào bản gửi cho người đọc"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Chủ bản tin Thư Chủ Nhật đang viết số 48 về quỹ khẩn cấp, cần bài có số liệu đúng. AI đã tin con số lãi suất 6,5–7% còn đúng, nhưng chủ bản tin đối chiếu bảng lãi suất hôm đó và thấy gửi 12 tháng chỉ còn 4,7%; con số cũ là của cuối 2023. Điều đáng nhớ: AI dễ coi số trong trí nhớ là số hiện hành, nên từ nay số liệu được đánh dấu để người làm tự kiểm tra."
audience: người viết bản tin hoặc nội dung có dùng AI
spine_context: "Chủ bản tin Thư Chủ Nhật đang viết số 48 về quỹ khẩn cấp, cùng AI."
spine_context_lines: ["claude:5a1e7c01#L1"]
spine_want: "Muốn bài có link đặt ngay trong câu và số liệu đúng, không để số cũ lọt vào bản gửi."
spine_want_lines: ["claude:5a1e7c01#L1", "claude:5a1e7c01#L50"]
spine_obstacle: Con số lãi suất trong bản nháp là số cũ từ cuối 2023.
spine_obstacle_lines: ["claude:5a1e7c01#L42"]
spine_turn: "AI tin con số 6,5–7% còn đúng; hoá ra lãi suất gửi online 12 tháng hiện là 4,7%."
spine_turn_lines: ["claude:5a1e7c01#L42"]
spine_action: "Thêm nguồn vào bài và thêm quy tắc vào style.md: AI không tự điền hay sửa số liệu, chỉ đánh dấu để người làm kiểm tra."
spine_action_lines: ["claude:5a1e7c01#L44", "claude:5a1e7c01#L49"]
spine_outcome: "Bài dùng số 4,7% đã đối chiếu, và từ nay số liệu được đánh dấu [KIỂM TRA] thay vì được AI đề xuất."
spine_outcome_lines: ["claude:5a1e7c01#L42", "claude:5a1e7c01#L49"]
spine_takeaway: "AI dễ coi số trong trí nhớ là số hiện hành, nên số liệu thay đổi theo thời gian cần người kiểm tra trước khi đăng."
spine_takeaway_lines: ["claude:5a1e7c01#L44"]
completeness: 7
---

# Link chú thích: lỗi thiếu dấu hai chấm được bắt khi đổi định dạng

**Góc kể:** Chủ bản tin Thư Chủ Nhật đang viết số 48 về quỹ khẩn cấp, cần bài có số liệu đúng. AI đã tin con số lãi suất 6,5–7% còn đúng, nhưng chủ bản tin đối chiếu bảng lãi suất hôm đó và thấy gửi 12 tháng chỉ còn 4,7%; con số cũ là của cuối 2023. Điều đáng nhớ: AI dễ coi số trong trí nhớ là số hiện hành, nên từ nay số liệu được đánh dấu để người làm tự kiểm tra.
**Bối cảnh:** Chủ bản tin muốn bỏ ba chú thích kiểu [1] [2] [3] vì MailerLite hiển thị xấu, và chuyển thành link đặt ngay trong câu.
**Chuyện gì xảy ra:** Khi đọc lại phần chú thích, agent thấy link thứ ba thiếu dấu hai chấm sau https và sửa ngay khi chuyển. Ba link được gắn vào ba cụm từ trong câu, rồi phần chú thích cuối bài được xoá trong hai lệnh sửa. Việc đổi định dạng chỉ mất hai lượt sửa nhưng suýt đưa một link hỏng vào bản gửi.
**Bài học:** Khi đổi định dạng link, đọc lại từng URL trước khi chuyển; một lỗi nhỏ như thiếu dấu hai chấm sẽ làm link không mở được.
**Artefact:** Danh sách ba link trước và sau khi chuyển, che nếu có thông tin cá nhân trong URL.
