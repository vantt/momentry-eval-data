---
id: 2026-10-29-ngan-sach-0-dong-am-tham
date: 2026-10-29
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, ràng buộc thiết kế]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L1160", "claude:0faf0bb2#L1170", "claude:0faf0bb2#L1174", "claude:0faf0bb2#L1175", "claude:0faf0bb2#L1183", "claude:0faf0bb2#L1337", "claude:0faf0bb2#L1338"]
hook: "Ngân sách 0 đồng chặn agent, comment của chủ không đánh thức được ai"
tension: cam_ma_van_lot
sides: ["Gói thuê bao nên không tốn đồng nào", "Hệ thống coi chi phí không xác định và chặn mọi lần chạy"]
strength: 3
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Ngân sách 0 đồng âm thầm chặn agent: comment của chủ không đánh thức được ai

**Bối cảnh:** Sau khi chạy được, comment của người chủ trên một task không tạo ra run mới. Agent marketing vẫn ở trạng thái paused.
**Chuyện gì xảy ra:** Lệnh đánh thức trả về HTTP 409 với thông báo 'recorded usage has no reliable price'. Model đang dùng là gói thuê bao nên không có đơn giá, Paperclip coi chi phí là không xác định và chặn mọi lần chạy. Mình đặt budget về 0 cho ba agent, resume agent, và run mới bắt đầu sau khoảng 20 giây.
**Bài học:** Đặt ngân sách cho agent trên model không có đơn giá sẽ khiến hệ thống chặn im lặng. Kiểm tra cách tính chi phí trước khi đặt budget.
**Artefact:** Dòng lỗi 409 đã che id, cùng bảng trạng thái paused/idle trước và sau khi đổi budget.
