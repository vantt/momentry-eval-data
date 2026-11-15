---
id: 2026-10-25-phieu-on-trung-de-thi-that-63a6
code: M-KCBG
aliases: [M-KCBG]
date: 2026-10-25
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo, dao_quyet_dinh, rang_buoc_thiet_ke]
source: "chat Claude, claude:5a1e7c03"
sessions: ["claude:5a1e7c03"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:5a1e7c03#L36", "claude:5a1e7c03#L38", "claude:5a1e7c03#L39", "claude:5a1e7c03#L40", "claude:5a1e7c03#L41", "claude:5a1e7c03#L42", "claude:5a1e7c03#L43", "claude:5a1e7c03#L44", "claude:5a1e7c03#L45", "claude:5a1e7c03#L49", "claude:5a1e7c03#L50", "claude:5a1e7c03#L51"]
hook: "Đề thi thật nằm sẵn trong phiếu ôn đã gửi qua Zalo hai ngày"
tension: cam_ma_van_lot
sides: ["Đề thi được giữ bí mật, chỉ giáo viên biết", "Bản nháp dán vào prompt khiến phần Viết trùng đề luyện đã phát cho học sinh"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một giáo viên Ngữ văn lớp 10 đang chấm bài và soạn đề giữa kỳ cùng trợ lý AI trước buổi thi thứ Ba. Cô tin dán đề thật vào prompt để nhờ soạn phiếu ôn sát dạng là an toàn, nhưng phiếu ôn đã gửi Zalo phụ huynh có một đề luyện gần nguyên văn đề thật, đã lộ hai ngày. Trợ lý đổi đề thật sang câu khác cùng dạng và kiểm tra bằng grep, vì đề đã phát ra ngoài thì không rút lại được. Ai nhờ AI soạn đề luyện từ tài liệu thật nên đọc để biết cách xử lý khi lỡ lộ đề."
audience: người dùng AI soạn tài liệu học tập và đề kiểm tra
spine_context: "Giáo viên Ngữ văn lớp 10 đang chấm bài nghị luận, sửa rubric và soạn đề giữa kỳ với trợ lý AI, thi thứ Ba tuần sau."
spine_context_lines: ["claude:5a1e7c03#L1", "claude:5a1e7c03#L36"]
spine_want: "Có đề giữa kỳ chính thức, và phiếu ôn sát dạng để học sinh luyện."
spine_want_lines: ["claude:5a1e7c03#L36", "claude:5a1e7c03#L42"]
spine_obstacle: "Bản nháp đề có ghi BẢO MẬT, nhưng phiếu ôn đã gửi qua Zalo có một đề luyện gần nguyên văn đề đó."
spine_obstacle_lines: ["claude:5a1e7c03#L38", "claude:5a1e7c03#L40"]
spine_turn: "Tưởng dán đề nháp vào prompt để soạn đề luyện 'na ná' là an toàn; hoá ra đề luyện số 3 trùng gần nguyên văn đề thật, và đề thật đã nằm ngoài tay giáo viên hai ngày."
spine_turn_lines: ["claude:5a1e7c03#L40", "claude:5a1e7c03#L41", "claude:5a1e7c03#L42"]
spine_action: "Đổi đề Phần II sang câu khác cùng dạng 600 chữ, ghi quy tắc không dán đề thật khi nhờ soạn đề luyện, rồi grep câu mới trên tài liệu."
spine_action_lines: ["claude:5a1e7c03#L44", "claude:5a1e7c03#L45", "claude:5a1e7c03#L47", "claude:5a1e7c03#L51"]
spine_outcome: Đề Phần II đã đổi; grep câu mới không có kết quả. Đề cũ đã lộ hai ngày qua Zalo và không rút lại được.
spine_outcome_lines: ["claude:5a1e7c03#L41", "claude:5a1e7c03#L51"]
spine_takeaway: "Trước khi nhờ AI soạn đề luyện, đừng dán đề thật vào; chỉ đưa dạng bài. Sau khi đổi đề, grep cụm mới trên mọi tài liệu đã phát."
spine_takeaway_lines: ["claude:5a1e7c03#L43", "claude:5a1e7c03#L51"]
completeness: 7
---

# Phiếu ôn trùng đề thi thật: bản nháp bị dán vào prompt, đề đã lộ qua Zalo

**Góc kể:** Một giáo viên Ngữ văn lớp 10 đang chấm bài và soạn đề giữa kỳ cùng trợ lý AI trước buổi thi thứ Ba. Cô tin dán đề thật vào prompt để nhờ soạn phiếu ôn sát dạng là an toàn, nhưng phiếu ôn đã gửi Zalo phụ huynh có một đề luyện gần nguyên văn đề thật, đã lộ hai ngày. Trợ lý đổi đề thật sang câu khác cùng dạng và kiểm tra bằng grep, vì đề đã phát ra ngoài thì không rút lại được. Ai nhờ AI soạn đề luyện từ tài liệu thật nên đọc để biết cách xử lý khi lỡ lộ đề.
**Bối cảnh:** Giáo viên nhờ soạn phiếu ôn giữa kỳ và đã dán bản nháp đề thật vào để "soạn sát dạng". Phiếu ôn được gửi nhóm Zalo phụ huynh hôm thứ Tư, trước buổi thi thứ Ba tuần sau.
**Chuyện gì xảy ra:** Agent định soạn đề chính thức từ bản nháp thì phát hiện phần Viết của đề thật trùng gần nguyên văn với một đề luyện trong phiếu ôn đã gửi, dòng 34. Đề bảo mật đã nằm ngoài tay giáo viên khoảng hai ngày. Agent không gỡ phiếu ôn hay nhắn đính chính vì sẽ gây chú ý, mà đổi hẳn đề Phần II, giữ nguyên dạng nghị luận 600 chữ. Sau khi đổi, agent tìm cụm từ mới trong toàn bộ tài liệu bằng grep và không thấy trùng. Từ nay quy tắc là không dán đề thật vào khi nhờ soạn đề luyện, chỉ đưa dạng bài.
**Bài học:** Trước khi soạn đề luyện, đừng đưa đề thật vào prompt; sau khi đổi đề, grep cụm từ mới trên toàn bộ tài liệu đã phát để chắc không còn trùng.
**Artefact:** Kết quả grep cho thấy đề cũ trùng trong phiếu ôn và kết quả grep cụm từ mới không có kết quả (che nội dung đề thật).
**Góc người ngoài:** cách làm phổ biến là Gỡ hoặc gửi thông báo đính chính ngay để xử lý sự cố, rồi sửa đề sau; ở đây khác ở Agent cân nhắc hậu quả của cách xử lý công khai (gây chú ý, làm lộ thêm) và chọn cách ít gây hại nhất, sau đó kiểm chứng bằng tìm kiếm thay vì tin vào suy đoán. Người đọc muốn biết cách xử lý sự cố lộ thông tin khi không thể rút lại thông tin đã phát ra ngoài.
