---
id: 2026-10-29-nho-mot-lan-tra-cuu-nguon-c455
code: M-1BFV
aliases: [M-1BFV]
date: 2026-10-29
repo: repo
status: raw
signals: [dao_quyet_dinh, nguoi_duyet_may_soan]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:0faf0bb2#L1326", "claude:0faf0bb2#L2310", "claude:0faf0bb2#L2313"]
hook: "Ghi nhầm cả tài liệu: reviewPolicy không chặn nổi agent tự đóng task"
tension: tuong_ma_hoa_ra
sides: ["Đặt reviewPolicy human_only, tưởng đã chặn tự đóng", "Agent tự done sau 26 giây, cổng thật là executionPolicy"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án dựng công ty một người vận hành bằng AI agent, và người làm muốn biết Paperclip dùng được luôn hay phải tự xây. Trong lần thử, một task đặt cờ 'chỉ người duyệt' vẫn bị agent tự đóng, nên ban đầu kết luận Paperclip thiếu luồng duyệt. Đọc lại tài liệu mới thấy cờ đó chỉ áp khi trả lời xác nhận; cổng review thật là executionPolicy, và spike chưa đặt nó. Ai đặt một cờ 'chỉ người duyệt' rồi tin là đã khoá việc nên kiểm tra cơ chế trước khi kết luận."
audience: dev đang chọn công cụ điều phối agent có bước duyệt
spine_context: "Dự án dựng công ty một người vận hành bằng AI agent, đang thử xem Paperclip có dùng luôn được không."
spine_context_lines: [profile, "claude:0faf0bb2#L712"]
spine_want: Muốn biết Paperclip dùng được ngay hay phải tự làm; nếu dùng được thì chỉ cần setup.
spine_want_lines: ["claude:0faf0bb2#L712"]
spine_obstacle: Task SEN-3 đặt reviewPolicy human_only nhưng agent vẫn tự chuyển sang done sau khi chạy xong.
spine_obstacle_lines: ["claude:0faf0bb2#L1326"]
spine_turn: "Tưởng reviewPolicy human_only chặn được việc agent tự đóng nên kết luận Paperclip thiếu luồng duyệt; hoá ra reviewPolicy chỉ áp khi trả lời xác nhận, còn executionPolicy mới là cổng review thật và spike chưa đặt nó."
spine_turn_lines: ["claude:0faf0bb2#L1326", "claude:0faf0bb2#L2310"]
spine_action: "Đọc lại tài liệu semantics của Paperclip, sửa lesson và §6.3, §8 trong tài liệu so sánh, ghi đính chính vào báo cáo spike."
spine_action_lines: ["claude:0faf0bb2#L2306", "claude:0faf0bb2#L2312", "claude:0faf0bb2#L2313"]
spine_outcome: Đã đính chính §6.3 và §8 cùng một lesson mới; learning area có 51 lessons; chưa commit và chưa kiểm chứng trên server đang chạy.
spine_outcome_lines: ["claude:0faf0bb2#L2312", "claude:0faf0bb2#L2328"]
spine_takeaway: Một cờ 'chỉ người duyệt' chưa chắc là cổng cứng; đọc đúng cơ chế (xác nhận hay luồng duyệt) trước khi kết luận hệ thống thiếu tính năng.
spine_takeaway_lines: ["claude:0faf0bb2#L2310"]
completeness: 7
---

# Nhờ một lần tra cứu nguồn, phát hiện spike Paperclip bị ghi nhầm: 'reviewPolicy' không chặn được việc agent tự đóng task

**Góc kể:** Dự án dựng công ty một người vận hành bằng AI agent, và người làm muốn biết Paperclip dùng được luôn hay phải tự xây. Trong lần thử, một task đặt cờ 'chỉ người duyệt' vẫn bị agent tự đóng, nên ban đầu kết luận Paperclip thiếu luồng duyệt. Đọc lại tài liệu mới thấy cờ đó chỉ áp khi trả lời xác nhận; cổng review thật là executionPolicy, và spike chưa đặt nó. Ai đặt một cờ 'chỉ người duyệt' rồi tin là đã khoá việc nên kiểm tra cơ chế trước khi kết luận.
**Bối cảnh:** Trong spike Paperclip, một task được đặt reviewPolicy human_only nhưng agent vẫn tự chuyển sang done. Lúc đầu kết luận là Paperclip thiếu luồng duyệt.
**Chuyện gì xảy ra:** Task SEN-3 đặt reviewPolicy human_only, nhưng agent tự đóng task (done) sau 26 giây. Đọc lại doc/execution-semantics.md cho thấy reviewPolicy chỉ áp khi trả lời một xác nhận, còn executionPolicy mới là cổng review thật. Phải sửa lại kết luận trong tài liệu so sánh (§6.3, §8) và trong lesson.
**Bài học:** Một cờ ‘chỉ người duyệt’ chưa chắc là cổng cứng; đọc đúng cơ chế (xác nhận hay luồng duyệt) trước khi kết luận hệ thống thiếu tính năng.
**Artefact:** Bảng so sánh reviewPolicy và executionPolicy trong docs/comparison-aicoworker-vs-paperclip.md (che tên đường dẫn vault nếu có).
**Góc người ngoài:** cách làm phổ biến là Người làm một mình thường sửa lỗi im lặng hoặc để nguyên tài liệu cũ; ít khi công khai đính chính đến mức ghi thành một mục riêng; ở đây khác ở Người đọc muốn biết vì sao phiên này chủ động 'đính chính' thay vì che đi, và việc đó giữ tài liệu tin cậy ra sao.
