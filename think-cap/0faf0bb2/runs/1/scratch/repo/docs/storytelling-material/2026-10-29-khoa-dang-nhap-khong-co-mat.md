---
id: 2026-10-29-khoa-dang-nhap-khong-co-mat
date: 2026-10-29
repo: repo
status: raw
signals: [ràng buộc định hình thiết kế, nguyên nhân bất ngờ]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L3650", "claude:0faf0bb2#L3654", "claude:0faf0bb2#L3772", "claude:0faf0bb2#L3785", "claude:0faf0bb2#L3787", "claude:0faf0bb2#L3806", "claude:0faf0bb2#L3851"]
hook: "Hệ thống không có mật khẩu, mã đăng nhập nằm ngay trong log server"
tension: khac
sides: ["Đăng nhập chỉ bằng mã email, không mật khẩu", "Không có email backend, mã chỉ được in ra log"]
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Khoá đăng nhập không có mật khẩu: mã xác nhận chỉ nằm trong log và cờ test bị bỏ qua khi production

**Bối cảnh:** Multica self-host không cấu hình SMTP nên không gửi được email đăng nhập, cần đăng nhập để test.
**Chuyện gì xảy ra:** Hệ thống chỉ có đăng nhập bằng mã email và Google, không có mật khẩu. Vì không có email backend, mã xác nhận được in ra log server. Đặt biến MULTICA_DEV_VERIFICATION_CODE để cố định mã, nhưng biến này bị bỏ qua và cảnh báo khi APP_ENV là production. Chỉ dùng cho môi trường test trong tailnet.
**Bài học:** Trước khi dùng một cờ test, đọc điều kiện nó bị bỏ qua; và đừng để cờ test chạy trên môi trường thật.
**Artefact:** Dòng cảnh báo 'ignored because APP_ENV=production' (không kèm mã).
