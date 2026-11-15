---
id: 2026-10-25-sau-khi-giao-vien-chi-ra-63a6
code: M-TQDJ
aliases: [M-TQDJ]
date: 2026-10-25
repo: repo
status: raw
signals: []
source: "chat Claude, claude:5a1e7c03"
sessions: ["claude:5a1e7c03"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:5a1e7c03#L43", "claude:5a1e7c03#L44"]
hook: "Giáo viên chỉ nhắc một lần, agent ghi thành quy tắc cố định"
tension: none
sides: []
strength: 0
stakes: 1
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một cô giáo Ngữ văn lớp 10A3 đang dùng AI soạn đề kiểm tra giữa kỳ, và muốn phiếu ôn sát dạng đề thật nên dán bản nháp đề vào. Cô tin đây là cách an toàn, nhưng đề luyện bị soạn quá sát đề gốc, trùng gần nguyên văn, rồi được gửi lên nhóm Zalo phụ huynh. Với ai nhờ AI tạo tài liệu luyện từ nội dung nhạy cảm, đây là lời cảnh báo: đừng đưa nội dung thật vào, chỉ đưa dạng bài."
audience: dev dùng AI để tạo tài liệu từ nội dung nhạy cảm hoặc nội bộ
spine_context: Cô giáo Ngữ văn lớp 10A3 đang chuẩn bị đề kiểm tra giữa kỳ với sự hỗ trợ của AI.
spine_context_lines: ["claude:5a1e7c03#L1"]
spine_want: "Có đề giữa kỳ sát dạng đề luyện, và đề không bị lộ."
spine_want_lines: ["claude:5a1e7c03#L36", "claude:5a1e7c03#L42"]
spine_obstacle: "Đề nháp đã nằm trong phiếu ôn gửi phụ huynh qua Zalo, và đề luyện trùng gần nguyên văn."
spine_obstacle_lines: ["claude:5a1e7c03#L36", "claude:5a1e7c03#L41"]
spine_turn: "Tưởng dán bản nháp vào để soạn đề luyện sát dạng là an toàn; hoá ra đề luyện bị soạn quá sát, trùng gần nguyên văn đề thật."
spine_turn_lines: ["claude:5a1e7c03#L41", "claude:5a1e7c03#L42"]
spine_action: "Đổi chủ đề Phần II sang đề mới, giữ dạng nghị luận 600 chữ."
spine_action_lines: ["claude:5a1e7c03#L44", "claude:5a1e7c03#L45"]
spine_outcome: File đề nháp đã được cập nhật thành công; chưa có xác nhận đã báo tổ trưởng hay ghi quy tắc vào ghi-chú.
spine_outcome_lines: ["claude:5a1e7c03#L46"]
spine_takeaway: "Khi nhờ AI soạn bài luyện từ đề thật, chỉ đưa dạng bài, không đưa nội dung đề."
spine_takeaway_lines: ["claude:5a1e7c03#L43"]
completeness: 7
---

# Sau khi giáo viên chỉ ra quy tắc không đưa đề thật vào prompt, agent ghi quy tắc đó thành một mục cố định trong file ghi chú của dự án để áp dụng cho các lần sau.

**Góc kể:** Một cô giáo Ngữ văn lớp 10A3 đang dùng AI soạn đề kiểm tra giữa kỳ, và muốn phiếu ôn sát dạng đề thật nên dán bản nháp đề vào. Cô tin đây là cách an toàn, nhưng đề luyện bị soạn quá sát đề gốc, trùng gần nguyên văn, rồi được gửi lên nhóm Zalo phụ huynh. Với ai nhờ AI tạo tài liệu luyện từ nội dung nhạy cảm, đây là lời cảnh báo: đừng đưa nội dung thật vào, chỉ đưa dạng bài.
**Chuyện gì xảy ra:** Sau khi giáo viên chỉ ra quy tắc không đưa đề thật vào prompt, agent ghi quy tắc đó thành một mục cố định trong file ghi chú của dự án để áp dụng cho các lần sau.
**Góc người ngoài:** cách làm phổ biến là Nhắc lại quy tắc trong cuộc trò chuyện hiện tại, hoặc chỉ tin vào việc người dùng sẽ tự nhớ; ở đây khác ở Quy tắc được lưu vào nơi các phiên làm việc sau đọc lại, nên không phụ thuộc vào trí nhớ của người dùng hay của một phiên cụ thể. Người đọc muốn biết cách biến một lỗi đã xảy ra thành ràng buộc lâu dài cho công cụ AI.
