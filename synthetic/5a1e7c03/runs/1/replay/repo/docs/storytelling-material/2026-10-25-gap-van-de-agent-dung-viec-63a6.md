---
id: 2026-10-25-gap-van-de-agent-dung-viec-63a6
code: M-QXAR
aliases: [M-QXAR]
date: 2026-10-25
repo: repo
status: raw
signals: []
source: "chat Claude, claude:5a1e7c03"
sessions: ["claude:5a1e7c03"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:5a1e7c03#L14", "claude:5a1e7c03#L15", "claude:5a1e7c03#L16", "claude:5a1e7c03#L17"]
hook: "Agent gặp vấn đề thì dừng, đưa ba phương án và chờ giáo viên chọn"
tension: none
sides: []
strength: 0
stakes: 1
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một giáo viên Ngữ văn lớp 10A3 đang chấm 42 bài nghị luận về lòng biết ơn. Người làm đưa bài mẫu viết sẵn để giúp mấy em yếu hay bỏ giấy trắng, tưởng đó chỉ là chỗ tựa. Hoá ra 17 bài chép cả ví dụ lẫn khung, có cả em khá, nên chấm theo rubric vẫn đủ ý mà chẳng thấy các em nghĩ gì. Ai đưa ví dụ mẫu cho người học nên biết: thứ giúp người yếu dễ thành khuôn để chép."
audience: dev và người dạy dùng AI soạn ví dụ mẫu cho người học
spine_context: Một giáo viên Ngữ văn lớp 10A3 đang chấm 42 bài nghị luận xã hội về lòng biết ơn.
spine_context_lines: ["claude:5a1e7c03#L1"]
spine_want: "Muốn thấy các em tự nghĩ, chứ không chỉ đủ ý theo rubric."
spine_want_lines: ["claude:5a1e7c03#L15"]
spine_obstacle: Bài mẫu viết sẵn bị nhiều bài chép gần nguyên; 14 bài mở bằng câu của bài mẫu.
spine_obstacle_lines: ["claude:5a1e7c03#L14"]
spine_turn: "Tưởng bài mẫu chỉ giúp mấy em yếu hay bỏ giấy trắng; hoá ra 17 bài chép cả ví dụ lẫn khung, có cả em khá."
spine_turn_lines: ["claude:5a1e7c03#L14", "claude:5a1e7c03#L15", "claude:5a1e7c03#L16"]
spine_action: "Làm cả ba phương án: chấm theo rubric kèm nhận xét riêng, cho 17 em viết lại phần dẫn chứng không có tài liệu, và soạn dàn ý mở chỉ có câu hỏi gợi ý."
spine_action_lines: ["claude:5a1e7c03#L16", "claude:5a1e7c03#L17", "claude:5a1e7c03#L18"]
spine_outcome: "Trong 7 em hay bỏ giấy trắng, cả 7 em nay viết đủ ba đoạn; đổi lại, khó nhìn ra tư duy của 17 em."
spine_outcome_lines: ["claude:5a1e7c03#L16"]
spine_takeaway: Bài mẫu trọn vẹn dễ thành khuôn để chép; muốn đỡ người yếu thì đưa khung và câu hỏi gợi ý.
spine_takeaway_lines: ["claude:5a1e7c03#L17"]
completeness: 7
---

# Gặp vấn đề, agent dừng việc đang làm, báo cáo mô hình phát hiện được, đưa ba phương án có khuyến nghị rõ, rồi chờ giáo viên chọn trước khi làm tiếp.

**Góc kể:** Một giáo viên Ngữ văn lớp 10A3 đang chấm 42 bài nghị luận về lòng biết ơn. Người làm đưa bài mẫu viết sẵn để giúp mấy em yếu hay bỏ giấy trắng, tưởng đó chỉ là chỗ tựa. Hoá ra 17 bài chép cả ví dụ lẫn khung, có cả em khá, nên chấm theo rubric vẫn đủ ý mà chẳng thấy các em nghĩ gì. Ai đưa ví dụ mẫu cho người học nên biết: thứ giúp người yếu dễ thành khuôn để chép.
**Chuyện gì xảy ra:** Gặp vấn đề, agent dừng việc đang làm, báo cáo mô hình phát hiện được, đưa ba phương án có khuyến nghị rõ, rồi chờ giáo viên chọn trước khi làm tiếp.
**Góc người ngoài:** cách làm phổ biến là Hoàn thành yêu cầu đang được giao và chỉ nhắc vấn đề phát sinh ở cuối, hoặc tự chọn cách xử lý mà không hỏi; ở đây khác ở Việc dừng để hỏi không phải do thiếu thông tin hay thiếu quyền; agent đưa ra quyết định ảnh hưởng đến cách chấm và đánh giá học sinh, nên đưa cho người có quyền quyết định. Người đọc muốn biết ranh giới giữa việc tự làm và việc phải hỏi.
