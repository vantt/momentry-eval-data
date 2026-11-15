---
id: 2026-10-29-loi-hua-paperclip-khong-co-cong
date: 2026-10-29
repo: repo
status: raw
signals: [đảo quyết định có lý do, nguyên nhân bất ngờ]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:0faf0bb2#L1290", "claude:0faf0bb2#L1326", "claude:0faf0bb2#L2310", "claude:0faf0bb2#L2313", "claude:0faf0bb2#L2328"]
hook: "Báo cáo nói Paperclip thiếu cổng duyệt, đọc lại thì cổng nằm ở chỗ khác"
tension: tuong_ma_hoa_ra
sides: ["Đặt human_only, agent vẫn tự chuyển done trong 26 giây, tưởng thiếu cổng duyệt", "Cổng thật là executionPolicy, không phải reviewPolicy"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Lời hứa 'Paperclip không có cổng review' bị đính chính: reviewPolicy khác executionPolicy

**Bối cảnh:** Spike cài reviewPolicy 'human_only' cho task và giao cho agent, để kiểm tra agent có tự đóng việc không.
**Chuyện gì xảy ra:** Task SEN-3 vẫn do agent chuyển sang done trong 26 giây, dù đã đặt human_only. Báo cáo ban đầu kết luận Paperclip thiếu cổng duyệt. Đọc lại execution-semantics cho thấy reviewPolicy chỉ áp khi trả lời một lời xin xác nhận, còn executionPolicy mới là cổng review/approval thật. Đã đính chính trong lesson, tài liệu so sánh và báo cáo spike.
**Bài học:** Hai cờ có tên gần nhau có thể khác hẳn phạm vi; đọc tài liệu semantics trước khi kết luận 'hệ thống không có tính năng X'.
**Artefact:** Bảng so sánh reviewPolicy và executionPolicy: phạm vi áp dụng, thời điểm kiểm tra.
**Góc người ngoài:** cách làm phổ biến là Người ta thường giữ nguyên kết luận đã viết, hoặc chỉ sửa khi bị hỏi lại; ở đây khác ở Agent chủ động sửa lại kết luận trước đó ngay trong tài liệu và learning area, kèm ghi chú lý do; người đọc muốn biết cơ chế nào giữ cho tài liệu không bị cũ.
