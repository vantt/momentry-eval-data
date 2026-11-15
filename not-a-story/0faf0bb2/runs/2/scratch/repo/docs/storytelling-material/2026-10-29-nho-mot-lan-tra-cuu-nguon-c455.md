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
hook: "Ghi nhầm kết luận: reviewPolicy không chặn được agent tự đóng task sau 26 giây"
tension: tuong_ma_hoa_ra
sides: ["Tưởng reviewPolicy human_only đã chặn agent tự đóng task", "Agent vẫn tự done sau 26 giây; executionPolicy mới là cổng review thật"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một người đang dựng công ty một người chạy bằng AI agent và thử Paperclip như một lựa chọn thay thế Multica. Phiên làm việc tin rằng Paperclip thiếu luồng duyệt, vì cờ reviewPolicy human_only không chặn được agent tự đóng task. Đọc kỹ tài liệu thì reviewPolicy chỉ áp khi trả lời xác nhận, còn executionPolicy mới là cổng review thật, nên kết luận cũ phải đính chính. Người dùng công cụ có cổng duyệt cần biết chi tiết này để không đánh giá sai một hệ thống chỉ vì đọc tên cờ."
audience: dev dùng AI agent và đang chọn công cụ quản lý task có cổng duyệt
spine_context: "Một người đang dựng bộ công ty một người vận hành bằng AI agent, nền Multica, và đang thử Paperclip như một lựa chọn thay thế."
spine_context_lines: [profile, "claude:0faf0bb2#L712"]
spine_want: "Muốn biết có thể dùng Paperclip luôn, chỉ cần setup, thay vì tự làm."
spine_want_lines: ["claude:0faf0bb2#L712"]
spine_obstacle: "Task đặt reviewPolicy human_only, nhưng agent vẫn tự chuyển sang done."
spine_obstacle_lines: ["claude:0faf0bb2#L1326"]
spine_turn: Tưởng Paperclip thiếu luồng duyệt vì reviewPolicy human_only không chặn được agent; hoá ra executionPolicy mới là cổng review thật.
spine_turn_lines: ["claude:0faf0bb2#L1326", "claude:0faf0bb2#L2310"]
spine_action: "Đọc doc/execution-semantics.md, sửa §6.3 và §8 trong bảng so sánh, thêm lesson mới."
spine_action_lines: ["claude:0faf0bb2#L2306", "claude:0faf0bb2#L2313"]
spine_outcome: Tài liệu và lesson đã sửa nhưng chưa commit; chưa kiểm chứng trên Paperclip đang chạy.
spine_outcome_lines: ["claude:0faf0bb2#L2328"]
spine_takeaway: Cờ tên 'người duyệt' có thể chỉ áp cho một loại xác nhận; đọc cơ chế trước khi kết luận hệ thống thiếu tính năng.
spine_takeaway_lines: ["claude:0faf0bb2#L2307", "claude:0faf0bb2#L2310"]
completeness: 7
---

# Nhờ một lần tra cứu nguồn, phát hiện spike Paperclip bị ghi nhầm: 'reviewPolicy' không chặn được việc agent tự đóng task

**Góc kể:** Một người đang dựng công ty một người chạy bằng AI agent và thử Paperclip như một lựa chọn thay thế Multica. Phiên làm việc tin rằng Paperclip thiếu luồng duyệt, vì cờ reviewPolicy human_only không chặn được agent tự đóng task. Đọc kỹ tài liệu thì reviewPolicy chỉ áp khi trả lời xác nhận, còn executionPolicy mới là cổng review thật, nên kết luận cũ phải đính chính. Người dùng công cụ có cổng duyệt cần biết chi tiết này để không đánh giá sai một hệ thống chỉ vì đọc tên cờ.
**Bối cảnh:** Trong spike Paperclip, một task được đặt reviewPolicy human_only nhưng agent vẫn tự chuyển sang done. Lúc đầu kết luận là Paperclip thiếu luồng duyệt.
**Chuyện gì xảy ra:** Task SEN-3 đặt reviewPolicy human_only, nhưng agent tự đóng task (done) sau 26 giây. Đọc lại doc/execution-semantics.md cho thấy reviewPolicy chỉ áp khi trả lời một xác nhận, còn executionPolicy mới là cổng review thật. Phải sửa lại kết luận trong tài liệu so sánh (§6.3, §8) và trong lesson.
**Bài học:** Một cờ ‘chỉ người duyệt’ chưa chắc là cổng cứng; đọc đúng cơ chế (xác nhận hay luồng duyệt) trước khi kết luận hệ thống thiếu tính năng.
**Artefact:** Bảng so sánh reviewPolicy và executionPolicy trong docs/comparison-aicoworker-vs-paperclip.md (che tên đường dẫn vault nếu có).
**Góc người ngoài:** cách làm phổ biến là Người làm một mình thường sửa lỗi im lặng hoặc để nguyên tài liệu cũ; ít khi công khai đính chính đến mức ghi thành một mục riêng; ở đây khác ở Người đọc muốn biết vì sao phiên này chủ động 'đính chính' thay vì che đi, và việc đó giữ tài liệu tin cậy ra sao.
