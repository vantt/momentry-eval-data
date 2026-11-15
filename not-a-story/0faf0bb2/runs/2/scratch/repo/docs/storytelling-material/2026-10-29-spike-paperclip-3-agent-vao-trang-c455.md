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
hook: "Ba agent bị 'paused' vì lệch giao thức, vá một dòng là xong"
tension: nho_ma_to
sides: ["Commit ghi 'nội dung không đổi', vá chỉ một dòng là đưa 3 agent về ready", "Rồi đặt budget lại chặn mọi lần đánh thức bằng lỗi 409 vì gói thuê bao không có giá"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án là bộ dựng công ty một người bằng AI agent, và người làm đang thử Paperclip để dựng một công ty mẫu chạy thật. Ba agent kẹt ở 'verifying' với lỗi chung 'thử lại', người làm tưởng là lỗi vặt, nhưng hoá ra Paperclip đòi giao thức v4 còn gateway chỉ nói v3. Vá một dòng đưa gateway kết nối được, nhưng lại vướng một lỗi im lặng khác: budget bị chặn 409 vì gói không có giá. Ai tự host agent gateway nên kiểm tra cả hai chỗ này trước khi nghi gateway."
audience: dev tự host agent gateway và thử nền tảng điều phối agent
spine_context: Dự án là bộ dựng công ty một người vận hành bằng AI agent; người làm đang thử Paperclip để dựng một công ty mẫu chạy thật.
spine_context_lines: [profile, "claude:0faf0bb2#L724"]
spine_want: "Muốn biết Paperclip dùng được luôn hay phải làm thêm, rồi chạy thử một công ty mẫu."
spine_want_lines: ["claude:0faf0bb2#L712", "claude:0faf0bb2#L724"]
spine_obstacle: Ba agent kẹt ở trạng thái 'verifying' với lỗi chung 'thử lại'.
spine_obstacle_lines: ["claude:0faf0bb2#L916"]
spine_turn: Tưởng là lỗi vặt của vòng đời agent; hoá ra bản cài Paperclip đòi giao thức v4 trong khi gateway chỉ nói v3.
spine_turn_lines: ["claude:0faf0bb2#L916", "claude:0faf0bb2#L984", "claude:0faf0bb2#L988"]
spine_action: "Vá minProtocol thành 3 trong bản cài (giữ bản gốc .orig), khởi động lại Paperclip, rồi đặt budget của agent về 0 để gỡ chặn."
spine_action_lines: ["claude:0faf0bb2#L987", "claude:0faf0bb2#L988", "claude:0faf0bb2#L1174"]
spine_outcome: "Gateway kết nối được; nhưng đánh thức bị chặn 409 vì không có giá, và SEN-3 chạy xong ở trạng thái 'done' dù task đặt human_only."
spine_outcome_lines: ["claude:0faf0bb2#L1021", "claude:0faf0bb2#L1170", "claude:0faf0bb2#L1326"]
spine_takeaway: Lỗi chung kiểu 'thử lại' có thể là lệch giao thức hoặc budget; kiểm tra cả hai trước khi đổ lỗi cho gateway.
spine_takeaway_lines: ["claude:0faf0bb2#L984", "claude:0faf0bb2#L988", "claude:0faf0bb2#L1170"]
completeness: 7
---

# Spike Paperclip: 3 agent vào trạng thái 'paused' vì lệch giao thức v3/v4 và một lỗi budget im lặng

**Góc kể:** Dự án là bộ dựng công ty một người bằng AI agent, và người làm đang thử Paperclip để dựng một công ty mẫu chạy thật. Ba agent kẹt ở 'verifying' với lỗi chung 'thử lại', người làm tưởng là lỗi vặt, nhưng hoá ra Paperclip đòi giao thức v4 còn gateway chỉ nói v3. Vá một dòng đưa gateway kết nối được, nhưng lại vướng một lỗi im lặng khác: budget bị chặn 409 vì gói không có giá. Ai tự host agent gateway nên kiểm tra cả hai chỗ này trước khi nghi gateway.
**Bối cảnh:** Dựng công ty mẫu Sen Coffee trên Paperclip gắn với gateway OpenClaw của AICoworker. Agent kẹt ở 'verifying' và comment của chủ không đánh thức được agent.
**Chuyện gì xảy ra:** Ba agent kẹt ở trạng thái verifying. Nguyên nhân là Paperclip đòi giao thức v4, gateway chỉ có v3 (một commit của Paperclip ghi nội dung không đổi). Vá một dòng trong bản cài đã đưa 3 agent về ready. Sau đó, đặt budget làm Paperclip chặn mọi lần đánh thức với lỗi 409 'no reliable price' vì gói thuê bao không có giá, nên phải đặt budget về 0.
**Bài học:** Lỗi im lặng kiểu 'không có giá nên chặn' có thể làm agent đứng hẳn mà không báo; kiểm tra budget trước khi đổ lỗi cho gateway.
**Artefact:** Ảnh chụp đoạn log 'Gateway connect probe succeeded' và bảng trạng thái agent (đã che token và đường dẫn).
**Góc người ngoài:** cách làm phổ biến là Hỏi người phát triển hoặc chờ bản cập nhật; hoặc bỏ cuộc khi gặp lỗi phiên bản; ở đây khác ở Người đọc sẽ hỏi làm sao biết đúng biến môi trường hay hằng số cần đổi mà không có tài liệu, và vì sao việc vá trong bản cài đặt được ghi kèm bản gốc '.orig' để hoàn tác.
