---
id: 2026-10-25-bai-mau-giup-hoc-sinh-yeu-63a6
code: M-3F1F
aliases: [M-3F1F]
date: 2026-10-25
repo: repo
status: raw
signals: [khac, nguyen_nhan_bat_ngo, dao_quyet_dinh, rang_buoc_thiet_ke]
source: "chat Claude, claude:5a1e7c03"
sessions: ["claude:5a1e7c03"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:5a1e7c03#L9", "claude:5a1e7c03#L11", "claude:5a1e7c03#L12", "claude:5a1e7c03#L13", "claude:5a1e7c03#L14", "claude:5a1e7c03#L15", "claude:5a1e7c03#L16", "claude:5a1e7c03#L17"]
hook: "Bài mẫu cứu 7 em bỏ giấy trắng, nhưng 17/42 bài chép khung"
tension: giup_ma_hai
sides: ["Bài mẫu giúp cả 7 em hay bỏ trống đều viết đủ ba đoạn", "17 em dùng đúng ví dụ mẫu, cô không còn thấy suy nghĩ riêng, cả ở em giỏi"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một giáo viên Ngữ văn 10 đang chấm bài nghị luận về lòng biết ơn và soạn đề kiểm tra giữa kỳ. Giáo viên nhờ soạn bài mẫu để giúp 6–7 em học yếu hay bỏ giấy trắng, và tưởng bài mẫu chỉ có lợi cho các em đó. Hoá ra 17 trong 42 bài chép đúng ví dụ của bài mẫu, cả những em khá, nên không còn thấy suy nghĩ riêng của học sinh. Người đọc làm chấm bài hay kiểm tra sao chép hàng loạt sẽ thấy cách đếm bằng grep và lý do chuyển sang chỉ phát câu hỏi gợi ý là dùng được ngay."
audience: dev và giáo viên muốn kiểm tra sao chép hàng loạt
spine_context: Giáo viên Ngữ văn 10 chấm bài nghị luận xã hội về lòng biết ơn (42 bài) và soạn đề kiểm tra giữa kỳ.
spine_context_lines: ["claude:5a1e7c03#L1"]
spine_want: Muốn bài mẫu giúp 6–7 em học yếu biết bài văn trông thế nào.
spine_want_lines: ["claude:5a1e7c03#L15"]
spine_obstacle: "Chấm theo rubric thì bài nào cũng đủ ý, nhưng không thấy học sinh tự nghĩ gì; có vẻ nhiều em đã chép khung."
spine_obstacle_lines: ["claude:5a1e7c03#L14", "claude:5a1e7c03#L15"]
spine_turn: "Tưởng bài mẫu chỉ giúp các em yếu; hoá ra 17 bài chép đúng ví dụ, cả em khá cũng chép."
spine_turn_lines: ["claude:5a1e7c03#L14", "claude:5a1e7c03#L15"]
spine_action: "Đếm bằng grep các cụm từ của bài mẫu, chọn cả ba hướng xử lý, rồi soạn dàn ý mở chỉ có câu hỏi gợi ý."
spine_action_lines: ["claude:5a1e7c03#L12", "claude:5a1e7c03#L17", "claude:5a1e7c03#L18"]
spine_outcome: "17 bài dùng ví dụ của bài mẫu, 14 bài mở giống câu mở; 7 em hay bỏ giấy trắng giờ viết đủ ba đoạn; đã tạo file dàn ý."
spine_outcome_lines: ["claude:5a1e7c03#L13", "claude:5a1e7c03#L16", "claude:5a1e7c03#L19"]
spine_takeaway: "Khi giúp người yếu, phát câu hỏi gợi ý thay vì bài đã viết sẵn; đếm cụm trùng bằng grep để biết có sao chép hàng loạt không."
spine_takeaway_lines: ["claude:5a1e7c03#L17"]
completeness: 7
---

# Bài mẫu giúp học sinh yếu, nhưng 17/42 bài bị chép khung

**Góc kể:** Một giáo viên Ngữ văn 10 đang chấm bài nghị luận về lòng biết ơn và soạn đề kiểm tra giữa kỳ. Giáo viên nhờ soạn bài mẫu để giúp 6–7 em học yếu hay bỏ giấy trắng, và tưởng bài mẫu chỉ có lợi cho các em đó. Hoá ra 17 trong 42 bài chép đúng ví dụ của bài mẫu, cả những em khá, nên không còn thấy suy nghĩ riêng của học sinh. Người đọc làm chấm bài hay kiểm tra sao chép hàng loạt sẽ thấy cách đếm bằng grep và lý do chuyển sang chỉ phát câu hỏi gợi ý là dùng được ngay.
**Bối cảnh:** Giáo viên Ngữ văn 10 nhờ soạn bài mẫu nghị luận xã hội để giúp các em học yếu biết bài văn trông thế nào. Bài mẫu được đưa cho cả lớp khi chấm bài.
**Chuyện gì xảy ra:** Khi kiểm tra 42 bài bằng tìm chuỗi văn bản, agent thấy 17 bài dùng đúng ví dụ trong bài mẫu và 14 bài mở đầu gần nguyên văn câu mở của bài mẫu. Số em hay bỏ giấy trắng giảm: cả 7 em đó đều viết đủ ba đoạn. Đổi lại, giáo viên không còn thấy suy nghĩ riêng của 17 em, kể cả những em vốn tự viết được. Giáo viên chọn làm cả ba hướng: chấm theo rubric nhưng ghi nhận xét riêng, cho viết lại phần dẫn chứng không có tài liệu, và từ nay chỉ phát dàn ý câu hỏi thay cho bài mẫu.
**Bài học:** Bài mẫu trọn vẹn cứu được người đang trắng tay nhưng khóa tư duy của người khá; khi cần khung cho người yếu, chỉ phát câu hỏi gợi ý, không phát bài đã viết sẵn.
**Artefact:** Bảng đếm số bài dùng chung cụm từ hoặc câu mở của bài mẫu (che tên học sinh và mã số bài).
**Góc người ngoài:** cách làm phổ biến là Đọc lướt vài bài mẫu rồi tóm tắt từng bài, hoặc đọc hết từng file mà không kiểm tra xem các bài có giống nhau không; ở đây khác ở Agent dùng grep để định lượng một vấn đề chất lượng bằng vài lệnh tìm kiếm, nên kết luận có số liệu để kiểm chứng, không chỉ là cảm nhận. Người đọc muốn biết cách làm này để áp dụng khi kiểm tra đạo văn hoặc sao chép hàng loạt.
