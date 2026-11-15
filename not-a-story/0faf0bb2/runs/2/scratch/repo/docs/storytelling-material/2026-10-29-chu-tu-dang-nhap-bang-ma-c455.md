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
hook: "Không có SMTP, mã đăng nhập nằm trong log; chủ đặt cố định 123456"
tension: none
sides: []
strength: 0
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: none
spine_context: "Đang spike Multica trên tailnet để chạy công ty một người với agent, và cần đăng nhập web để theo dõi công việc."
spine_context_lines: [profile, "claude:0faf0bb2#L3643"]
spine_want: Muốn đăng nhập được web Multica để xem công việc của agent.
spine_want_lines: ["claude:0faf0bb2#L3634"]
spine_obstacle: "Server không gửi được email nên mã xác nhận chỉ nằm trong log, và Multica không có đăng nhập bằng mật khẩu."
spine_obstacle_lines: ["claude:0faf0bb2#L3650", "claude:0faf0bb2#L3772"]
spine_action: Đặt mã cố định 123456 cho backend spike rồi khởi động lại.
spine_action_lines: ["claude:0faf0bb2#L3850"]
spine_outcome: Đăng nhập thử bằng mã 123456 thành công.
spine_outcome_lines: ["claude:0faf0bb2#L3851", "claude:0faf0bb2#L3856"]
spine_takeaway: "Mã cố định kiểu dev chỉ dùng cho môi trường thử, và phải kiểm tra APP_ENV trước khi dựa vào nó."
spine_takeaway_lines: ["claude:0faf0bb2#L3772"]
completeness: 6
---

# Chủ tự đăng nhập bằng mã cố định vì Multica không có mật khẩu và chỉ gửi mã vào log

**Bối cảnh:** Chủ muốn đăng nhập web Multica trên tailnet, nhưng server không gửi email (không có SMTP hay Resend) nên mã xác nhận chỉ nằm trong log.
**Chuyện gì xảy ra:** Multica không có đăng nhập bằng mật khẩu; chỉ có mã email và Google OAuth. Vì không có SMTP, mã nằm trong log của backend và phải lấy bằng lệnh docker logs. Để test, đặt MULTICA_DEV_VERIFICATION_CODE=123456, chỉ hoạt động khi APP_ENV không phải production.
**Bài học:** Mã cố định kiểu dev chỉ dùng được cho môi trường thử, không dùng cho sản xuất; luôn kiểm tra APP_ENV trước khi dựa vào nó.
**Artefact:** Ảnh màn hình trang đăng nhập (che email thật, không chụp mã).
**Góc người ngoài:** cách làm phổ biến là Cấu hình SMTP hoặc đăng nhập bằng Google/mật khẩu thật; ít khi đặt mã cố định, dù chỉ dùng trong tailnet; ở đây khác ở Người đọc muốn biết có an toàn không khi đặt mã cố định, và vì sao không cần gửi email thật cho bước thử nghiệm.
