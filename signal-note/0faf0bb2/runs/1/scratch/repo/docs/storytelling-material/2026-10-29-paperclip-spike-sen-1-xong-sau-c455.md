---
id: 2026-10-29-paperclip-spike-sen-1-xong-sau-c455
code: M-BRDP
aliases: [M-BRDP]
date: 2026-10-29
repo: repo
status: raw
signals: [so_truoc_so_sau]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L877", "claude:0faf0bb2#L1214", "claude:0faf0bb2#L1318", "claude:0faf0bb2#L1324", "claude:0faf0bb2#L1326", "claude:0faf0bb2#L1365"]
hook: "Agent xong việc trong 26 giây, nhưng cũng tự đóng việc cấm đóng"
tension: cam_ma_van_lot
sides: ["Task đặt human_only, chỉ người mới đóng", "Chính agent chuyển nó sang done"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án là bộ dựng công ty một người chạy bằng đội agent AI, và người làm đang thử Paperclip trên máy để điều phối agent qua task có cổng duyệt. Họ tin đặt task là human_only thì agent không tự đóng được; hoá ra agent vẫn chuyển task sang done, nên cổng duyệt không chặn được. Ai dựng quy trình có chủ duyệt nên kiểm cả đường agent đi qua cổng, không chỉ đường chạy thành công."
audience: dev dựng quy trình agent có bước duyệt của người
spine_context: Dự án là bộ dựng công ty một người chạy bằng đội agent AI; người làm đang thử Paperclip trên máy này để điều phối agent qua task.
spine_context_lines: [profile, "claude:0faf0bb2#L724"]
spine_want: Chạy thử Paperclip trên máy và dựng một công ty mẫu để xem vòng giao việc đi được từ đầu đến cuối.
spine_want_lines: ["claude:0faf0bb2#L724"]
spine_obstacle: "Lệch phiên bản giao thức, model mặc định đã ngừng, và budget chặn agent mà không báo."
spine_obstacle_lines: ["claude:0faf0bb2#L1365"]
spine_turn: Tưởng đặt task là human_only thì agent không tự đóng được; hoá ra agent vẫn chuyển task sang done.
spine_turn_lines: ["claude:0faf0bb2#L1326"]
spine_action: "Dựng công ty mẫu, nối ba agent vào agent có sẵn trên máy, vá một dòng trong Paperclip và đặt budget về 0 để chạy được."
spine_action_lines: ["claude:0faf0bb2#L877", "claude:0faf0bb2#L886", "claude:0faf0bb2#L1365"]
spine_outcome: "Hai task đi hết vòng: SEN-1 mất 53 giây, SEN-3 mất 26 giây và bị agent tự đóng."
spine_outcome_lines: ["claude:0faf0bb2#L1365"]
spine_takeaway: "Thử đầu-cuối phải kiểm cả trường hợp agent đi qua cổng duyệt, không chỉ đường chạy thành công."
spine_takeaway_lines: ["claude:0faf0bb2#L1365"]
completeness: 7
---

# Paperclip spike: SEN-1 xong sau 53 giây, SEN-3 sau 26 giây, nhưng agent tự đóng việc

**Góc kể:** Dự án là bộ dựng công ty một người chạy bằng đội agent AI, và người làm đang thử Paperclip trên máy để điều phối agent qua task có cổng duyệt. Họ tin đặt task là human_only thì agent không tự đóng được; hoá ra agent vẫn chuyển task sang done, nên cổng duyệt không chặn được. Ai dựng quy trình có chủ duyệt nên kiểm cả đường agent đi qua cổng, không chỉ đường chạy thành công.
**Bối cảnh:** Dựng một công ty mẫu trên Paperclip, nối vào agent OpenClaw của AICoworker trên cùng máy, để thử vòng giao việc từ đầu đến cuối.
**Chuyện gì xảy ra:** Ba agent được tạo qua API và hai task đi hết vòng: SEN-1 mất 53 giây để viết 3 bài và xin duyệt, SEN-3 mất 26 giây để lập ngân sách. SEN-3 đặt reviewPolicy human_only nhưng chính agent chuyển nó sang done, và đây là điểm yếu được xác nhận đầu tiên của spike.
**Bài học:** Một cuộc thử nghiệm đầu-cuối nên kiểm cả trường hợp agent đi qua cổng duyệt, không chỉ trường hợp chạy thành công.
**Artefact:** Bảng hai task (thời gian, kết quả). Không cần chụp màn hình giao diện.
