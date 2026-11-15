---
id: 2026-10-25-doi-ten-42-anh-chup-theo-63a6
code: M-GPYM
aliases: [M-GPYM]
date: 2026-10-25
repo: repo
status: raw
signals: [số trước/sau, thứ tự ảnh chụp dựa vào lời giáo viên]
source: "chat Claude, claude:5a1e7c03"
sessions: ["claude:5a1e7c03"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:5a1e7c03#L2", "claude:5a1e7c03#L3", "claude:5a1e7c03#L4", "claude:5a1e7c03#L5", "claude:5a1e7c03#L6", "claude:5a1e7c03#L7", "claude:5a1e7c03#L8"]
hook: "Agent đổi tên 42 ảnh hàng loạt, chưa kiểm thử một tờ nào"
tension: nho_ma_to
sides: ["Báo xong, tin lời giáo viên rằng thứ tự chụp khớp sổ", "Nếu thứ tự lệch, cả 42 bài gắn nhầm tên học sinh"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: none
spine_context: "Cô giáo dạy văn lớp 10A3 đang chấm bài nghị luận xã hội về \"lòng biết ơn\" (42 bài scan) và chuẩn bị đề kiểm tra giữa kỳ."
spine_context_lines: ["claude:5a1e7c03#L1"]
spine_want: "Chấm xong bài, sửa rubric và soạn đề kiểm tra trong tối nay."
spine_want_lines: ["claude:5a1e7c03#L1"]
spine_obstacle: "Các file scan mang tên ảnh chụp từ điện thoại (IMG_...), khó đối chiếu với sổ điểm."
spine_obstacle_lines: ["claude:5a1e7c03#L4"]
spine_action: Đổi tên 42 file theo danh sách lớp bằng một script.
spine_action_lines: ["claude:5a1e7c03#L6", "claude:5a1e7c03#L8"]
spine_outcome: Đã đổi xong 42 file; cô giáo đã đọc được 20 bài và có ghi chú chấm điểm.
spine_outcome_lines: ["claude:5a1e7c03#L8", "claude:5a1e7c03#L9"]
completeness: 5
---

# Đổi tên 42 ảnh chụp theo sổ lớp bằng script, chạy trước khi kiểm tra thứ tự

**Bối cảnh:** 42 bài scan là ảnh chụp điện thoại tên IMG_..., không đối chiếu được với sổ điểm. Giáo viên xác nhận đã chụp theo đúng thứ tự trong sổ.
**Chuyện gì xảy ra:** Agent dùng script đổi 42 file từ tên ảnh sang dạng số thứ tự và tên học sinh theo danh sách lớp, rồi báo đã xong. Việc đổi tên dựa hoàn toàn vào lời giáo viên rằng thứ tự chụp khớp sổ, và chưa có bước kiểm tra mẫu vài tờ trước khi đổi hàng loạt. Nếu thứ tự lệch, toàn bộ bài sẽ gắn nhầm tên.
**Bài học:** Với thao tác đổi tên hàng loạt có tính đối chiếu, mở thử 2–3 file đầu và cuối để xác nhận trước khi chạy cho cả lô.
**Artefact:** Danh sách tên file trước và sau đổi (che tên học sinh).
