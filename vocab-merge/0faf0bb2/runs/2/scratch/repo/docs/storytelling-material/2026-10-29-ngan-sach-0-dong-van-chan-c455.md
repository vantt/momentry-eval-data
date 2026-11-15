---
id: 2026-10-29-ngan-sach-0-dong-van-chan-c455
code: M-T6KC
aliases: [M-T6KC]
date: 2026-10-29
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, số trước sau]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L1138", "claude:0faf0bb2#L1148", "claude:0faf0bb2#L1160", "claude:0faf0bb2#L1170", "claude:0faf0bb2#L1174", "claude:0faf0bb2#L1183"]
hook: "Ngân sách 0 đồng vẫn chặn agent, và giao diện không báo lỗi"
tension: cam_ma_van_lot
sides: ["Đặt ngân sách để kiểm soát chi phí", "Gói thuê bao không có giá, nên mọi lần đánh thức bị từ chối ngầm"]
strength: 3
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Ngân sách 0 đồng vẫn chặn agent: comment của chủ không đánh thức được ai

**Bối cảnh:** Sau khi tạo task và chọn model cho agent, comment của người điều hành không tạo ra run mới.
**Chuyện gì xảy ra:** Đợi 10 phút không có run nào. Lệnh wake trả 409 với thông báo 'cannot start work because recorded usage has no reliable price'. Model gói thuê bao không có giá, nên khi budget được đặt, Paperclip từ chối mọi lần đánh thức. Lỗi không hiện trên UI. Đặt budget về 0 cho ba agent rồi resume, và run chạy ngay.
**Bài học:** Ngân sách theo token cần có giá cho model. Với model gói cố định không có giá, ngân sách sẽ chặn im lặng.
**Artefact:** Thông báo 409 'no reliable price'. Id đã che.
