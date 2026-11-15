---
id: 2026-10-29-va-lech-phien-ban-giao-thuc
date: 2026-10-29
repo: repo
status: raw
signals: [số trước/sau, nguyên nhân bất ngờ]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L959", "claude:0faf0bb2#L968", "claude:0faf0bb2#L984", "claude:0faf0bb2#L988", "claude:0faf0bb2#L1016", "claude:0faf0bb2#L1021", "claude:0faf0bb2#L1031"]
hook: "Agent kẹt ở verifying vì lệch phiên bản giao thức, sửa một số là xong"
tension: nho_ma_to
sides: ["chỉ lệch một số phiên bản giao thức, 4 so với 3", "cả ba agent kẹt verifying, sửa ba chỗ là ready"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Vá lệch phiên bản giao thức: agent kẹt ở verifying, sửa một dòng là kết nối được

**Bối cảnh:** Paperclip (control plane mở, MIT) nối vào gateway OpenClaw của AICoworker qua WebSocket. Ba agent đều kẹt ở trạng thái verifying và báo lỗi chung.
**Chuyện gì xảy ra:** Log cho thấy adapter của Paperclip yêu cầu giao thức phiên bản 4, còn gateway của AICoworker chỉ nói phiên bản 3. Commit upstream ghi rõ việc tăng từ 3 lên 4 không đổi ngữ nghĩa frame. Mình đổi minProtocol từ 4 xuống 3 ở ba chỗ trong bản đã cài, giữ file .orig để hoàn tác. Sau khi vá, probe kết nối thành công và cả ba agent chuyển sang ready.
**Bài học:** Khi hai bên lệch phiên bản giao thức, đọc commit của chính bên upstream xem thay đổi có làm đổi nội dung không trước khi vá, và luôn giữ bản gốc để hoàn tác.
**Artefact:** Bảng trước/sau: trạng thái agent verifying → ready, kèm dòng log 'Gateway connect probe succeeded'. Che id, token và đường dẫn home.
