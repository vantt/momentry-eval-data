---
id: 2026-10-29-lay-ma-dang-nhap-multica-tu-c455
code: M-2TME
aliases: [M-2TME]
date: 2026-10-29
repo: repo
status: raw
signals: [ràng buộc định hình thiết kế]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L3650", "claude:0faf0bb2#L3772", "claude:0faf0bb2#L3785", "claude:0faf0bb2#L3806", "claude:0faf0bb2#L3856"]
hook: "Muốn mã đăng nhập cố định, nhưng production tự bỏ qua biến dev"
tension: none
sides: []
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Lấy mã đăng nhập Multica từ log: không có mật khẩu, dev code bị bỏ qua khi production

**Bối cảnh:** Web UI của Multica chỉ đăng nhập bằng mã gửi qua email. Không có mật khẩu.
**Chuyện gì xảy ra:** Vì chưa cấu hình SMTP, mã xác nhận được ghi vào log của backend. Muốn có mã cố định phải dùng biến môi trường dev, và biến này bị bỏ qua khi APP_ENV là production. Mã phải có 6 chữ số. Sau khi đặt mã, đăng nhập thử thành công và daemon vẫn online.
**Bài học:** Chế độ dev bypass dễ thành lỗ hổng. Chỉ bật trong mạng riêng và ghi rõ trong runbook.
**Artefact:** Dòng log 'Verification code for'. Mã đã che.
