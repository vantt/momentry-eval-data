---
id: 2026-10-29-chu-tu-dang-nhap-bang-ma-c455
code: M-S1QZ
aliases: [M-S1QZ]
date: 2026-10-29
repo: repo
status: raw
signals: [rang_buoc_thiet_ke, nguyen_nhan_bat_ngo]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:0faf0bb2#L3643", "claude:0faf0bb2#L3650", "claude:0faf0bb2#L3772", "claude:0faf0bb2#L3850"]
hook: "Không có mật khẩu, không có SMTP: mã đăng nhập chỉ nằm trong log"
tension: khac
sides: ["Hệ thống đăng nhập chỉ bằng mã gửi qua email", "Không có SMTP nên mã nằm trong log, phải đặt mã cố định 123456 để test"]
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Chủ tự đăng nhập bằng mã cố định vì Multica không có mật khẩu và chỉ gửi mã vào log

**Bối cảnh:** Chủ muốn đăng nhập web Multica trên tailnet, nhưng server không gửi email (không có SMTP hay Resend) nên mã xác nhận chỉ nằm trong log.
**Chuyện gì xảy ra:** Multica không có đăng nhập bằng mật khẩu; chỉ có mã email và Google OAuth. Vì không có SMTP, mã nằm trong log của backend và phải lấy bằng lệnh docker logs. Để test, đặt MULTICA_DEV_VERIFICATION_CODE=123456, chỉ hoạt động khi APP_ENV không phải production.
**Bài học:** Mã cố định kiểu dev chỉ dùng được cho môi trường thử, không dùng cho sản xuất; luôn kiểm tra APP_ENV trước khi dựa vào nó.
**Artefact:** Ảnh màn hình trang đăng nhập (che email thật, không chụp mã).
**Góc người ngoài:** cách làm phổ biến là Cấu hình SMTP hoặc đăng nhập bằng Google/mật khẩu thật; ít khi đặt mã cố định, dù chỉ dùng trong tailnet; ở đây khác ở Người đọc muốn biết có an toàn không khi đặt mã cố định, và vì sao không cần gửi email thật cho bước thử nghiệm.
