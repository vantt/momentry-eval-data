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
hook: "Ba agent kẹt vì lệch giao thức, rồi budget lại chặn mọi lần đánh thức"
tension: nho_ma_to
sides: ["Vá một dòng là đưa 3 agent về ready", "Đặt budget thì Paperclip chặn mọi lần đánh thức bằng lỗi 409 vì gói thuê bao không có giá"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Spike Paperclip: 3 agent vào trạng thái 'paused' vì lệch giao thức v3/v4 và một lỗi budget im lặng

**Bối cảnh:** Dựng công ty mẫu Sen Coffee trên Paperclip gắn với gateway OpenClaw của AICoworker. Agent kẹt ở 'verifying' và comment của chủ không đánh thức được agent.
**Chuyện gì xảy ra:** Ba agent kẹt ở trạng thái verifying. Nguyên nhân là Paperclip đòi giao thức v4, gateway chỉ có v3 (một commit của Paperclip ghi nội dung không đổi). Vá một dòng trong bản cài đã đưa 3 agent về ready. Sau đó, đặt budget làm Paperclip chặn mọi lần đánh thức với lỗi 409 'no reliable price' vì gói thuê bao không có giá, nên phải đặt budget về 0.
**Bài học:** Lỗi im lặng kiểu 'không có giá nên chặn' có thể làm agent đứng hẳn mà không báo; kiểm tra budget trước khi đổ lỗi cho gateway.
**Artefact:** Ảnh chụp đoạn log 'Gateway connect probe succeeded' và bảng trạng thái agent (đã che token và đường dẫn).
**Góc người ngoài:** cách làm phổ biến là Hỏi người phát triển hoặc chờ bản cập nhật; hoặc bỏ cuộc khi gặp lỗi phiên bản; ở đây khác ở Người đọc sẽ hỏi làm sao biết đúng biến môi trường hay hằng số cần đổi mà không có tài liệu, và vì sao việc vá trong bản cài đặt được ghi kèm bản gốc '.orig' để hoàn tác.
