---
id: 2026-10-29-paperclip-ket-o-verifying-vi-lech
date: 2026-10-29
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, số trước/sau]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:0faf0bb2#L959", "claude:0faf0bb2#L968", "claude:0faf0bb2#L981", "claude:0faf0bb2#L987", "claude:0faf0bb2#L1016", "claude:0faf0bb2#L1021", "claude:0faf0bb2#L1030", "claude:0faf0bb2#L1031"]
hook: "3 agent kẹt 'verifying' chỉ vì một con số: giao thức v3 gặp v4"
tension: nho_ma_to
sides: ["Một số phiên bản giao thức lệch từ 3 lên 4", "Cả 3 agent kẹt, phải vá 3 dòng trong bản đã cài"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Paperclip kẹt ở 'verifying' vì lệch giao thức v3/v4, phải vá 3 dòng trong bản đã cài

**Bối cảnh:** Paperclip (control plane MIT) nối vào gateway của AICoworker để đánh thức agent qua giao thức WebSocket.
**Chuyện gì xảy ra:** Cả 3 agent dừng ở trạng thái verifying với lỗi 'The lifecycle step failed'. Commit upstream nâng PROTOCOL_VERSION từ 3 lên 4 để khớp gateway, nhưng gateway đóng gói sẵn chỉ nói v3, và handler từ chối khi minProtocol lớn hơn phiên bản của client. Sửa minProtocol xuống 3 ở 3 chỗ trong bản đã cài (có file .orig để hoàn tác), khởi động lại, probe thành công, và 3 agent về trạng thái ready.
**Bài học:** Khi nối hai hệ thống qua giao thức, kiểm tra con số phiên bản ở cả hai phía trước khi nghi logic; một commit upstream ghi 'không đổi ngữ nghĩa' vẫn có thể chặn handshake.
**Artefact:** Bảng 3 agent: trạng thái trước (verifying, paused) và sau (ready), kèm dòng log 'Gateway connect probe succeeded'. Che token và id.
**Góc người ngoài:** cách làm phổ biến là Người dùng thường bỏ cuộc hoặc nhờ người khác khi agent kẹt không rõ lý do; ít người tự đọc mã nguồn bên thứ ba để tìm đúng dòng gây lỗi; ở đây khác ở Chẩn đoán đi từ triệu chứng (verifying kẹt, 409 no reliable price) đến dòng mã cụ thể, rồi vá đúng 3 chỗ và ghi lại trong runbook; người đọc muốn biết cách tiếp cận để áp dụng cho lỗi của mình.
