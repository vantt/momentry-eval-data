---
id: 2026-10-29-spike-paperclip-3-agent-vao-trang-c455
code: M-3RRH
aliases: [M-3RRH]
date: 2026-10-29
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo, so_truoc_so_sau, rang_buoc_thiet_ke]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:0faf0bb2#L916", "claude:0faf0bb2#L987", "claude:0faf0bb2#L1021", "claude:0faf0bb2#L1170", "claude:0faf0bb2#L1175", "claude:0faf0bb2#L1322"]
hook: "Ba agent kẹt 'paused' vì lệch v3/v4, vá một dòng là xong"
tension: nho_ma_to
sides: ["Vá một dòng giao thức đưa 3 agent về ready", "Đặt budget xong, Paperclip chặn mọi lần đánh thức với lỗi 409"]
strength: 3
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Người làm đang thử Paperclip trên máy để dựng một công ty mẫu, kỳ vọng nối được luôn vào gateway có sẵn. Họ tưởng hai bên ăn khớp, nhưng Paperclip đòi giao thức v4 còn gateway chỉ nói v3, nên ba agent kẹt ở bước verifying. Hạ phiên bản về v3 đưa agent sang sẵn sàng, nhưng một lỗi budget im lặng lại chặn mọi lần đánh thức. Ai dựng agent cho việc thật nên biết vì lỗi kiểu này không báo rõ, agent chỉ đứng yên."
audience: dev đang thử công cụ điều phối agent tự host
spine_context: "Bộ dựng công ty một người vận hành bằng AI agent. Người làm đang thử Paperclip trên máy, dựng một công ty mẫu để xem có dùng được ngay với gateway có sẵn không."
spine_context_lines: [profile, "claude:0faf0bb2#L724"]
spine_want: "Muốn Paperclip chạy được luôn với gateway, chỉ cần setup mà không phải viết thêm."
spine_want_lines: ["claude:0faf0bb2#L712", "claude:0faf0bb2#L724"]
spine_obstacle: "Ba agent đứng ở trạng thái verifying, paused với lỗi 'The lifecycle step failed'."
spine_obstacle_lines: ["claude:0faf0bb2#L916"]
spine_turn: Tưởng Paperclip và gateway ăn khớp; hoá ra Paperclip đòi giao thức v4 trong khi gateway chỉ nói v3.
spine_turn_lines: ["claude:0faf0bb2#L984", "claude:0faf0bb2#L988"]
spine_action: "Vá bản cài đặt đổi minProtocol từ 4 xuống 3 ở 3 chỗ, giữ bản gốc .orig, rồi khởi động lại Paperclip."
spine_action_lines: ["claude:0faf0bb2#L987", "claude:0faf0bb2#L988"]
spine_outcome: "Gateway connect probe succeeded. Task SEN-3 kết thúc với run succeeded, nhưng agent tự chuyển issue sang done dù task đặt human_only."
spine_outcome_lines: ["claude:0faf0bb2#L1021", "claude:0faf0bb2#L1324", "claude:0faf0bb2#L1326"]
spine_takeaway: "Khi agent đứng mà không báo, kiểm tra budget trước khi đổ lỗi cho gateway: một giá trị budget chưa có giá có thể chặn mọi lần đánh thức."
spine_takeaway_lines: ["claude:0faf0bb2#L1170", "claude:0faf0bb2#L1175"]
completeness: 7
---

# Spike Paperclip: 3 agent vào trạng thái 'paused' vì lệch giao thức v3/v4 và một lỗi budget im lặng

**Góc kể:** Người làm đang thử Paperclip trên máy để dựng một công ty mẫu, kỳ vọng nối được luôn vào gateway có sẵn. Họ tưởng hai bên ăn khớp, nhưng Paperclip đòi giao thức v4 còn gateway chỉ nói v3, nên ba agent kẹt ở bước verifying. Hạ phiên bản về v3 đưa agent sang sẵn sàng, nhưng một lỗi budget im lặng lại chặn mọi lần đánh thức. Ai dựng agent cho việc thật nên biết vì lỗi kiểu này không báo rõ, agent chỉ đứng yên.
**Bối cảnh:** Dựng công ty mẫu Sen Coffee trên Paperclip gắn với gateway OpenClaw của AICoworker. Agent kẹt ở 'verifying' và comment của chủ không đánh thức được agent.
**Chuyện gì xảy ra:** Ba agent kẹt ở trạng thái verifying. Nguyên nhân là Paperclip đòi giao thức v4, gateway chỉ có v3 (một commit của Paperclip ghi nội dung không đổi). Vá một dòng trong bản cài đã đưa 3 agent về ready. Sau đó, đặt budget làm Paperclip chặn mọi lần đánh thức với lỗi 409 'no reliable price' vì gói thuê bao không có giá, nên phải đặt budget về 0.
**Bài học:** Lỗi im lặng kiểu 'không có giá nên chặn' có thể làm agent đứng hẳn mà không báo; kiểm tra budget trước khi đổ lỗi cho gateway.
**Artefact:** Ảnh chụp đoạn log 'Gateway connect probe succeeded' và bảng trạng thái agent (đã che token và đường dẫn).
**Góc người ngoài:** cách làm phổ biến là Hỏi người phát triển hoặc chờ bản cập nhật; hoặc bỏ cuộc khi gặp lỗi phiên bản; ở đây khác ở Người đọc sẽ hỏi làm sao biết đúng biến môi trường hay hằng số cần đổi mà không có tài liệu, và vì sao việc vá trong bản cài đặt được ghi kèm bản gốc '.orig' để hoàn tác.
