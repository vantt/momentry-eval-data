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
hook: "Muốn đăng nhập Multica? Mã nằm trong log, hoặc cứ đặt luôn 123456"
tension: khac
sides: ["Hệ thống chỉ có mã email, không có mật khẩu", "Không có SMTP nên mã nằm trong log, phải đặt mã cố định để test"]
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: none
spine_context: "Dự án là bộ dựng công ty một người vận hành bằng AI agent, nền Multica; người làm đang dựng workspace cho một khách và cần vào web UI để kiểm tra."
spine_context_lines: [profile]
spine_want: Muốn vào được web UI Multica để xem workspace và các issue.
spine_want_lines: ["claude:0faf0bb2#L3634"]
spine_obstacle: "Server không có SMTP hay Resend nên mã xác nhận chỉ nằm trong log, và Multica không có đăng nhập bằng mật khẩu."
spine_obstacle_lines: ["claude:0faf0bb2#L3650", "claude:0faf0bb2#L3772"]
spine_action: "Đặt mã cố định cho môi trường thử nghiệm (ban đầu là \"demo\", sau đổi thành 123456), khởi động lại backend và kiểm tra đăng nhập."
spine_action_lines: ["claude:0faf0bb2#L3775", "claude:0faf0bb2#L3850"]
spine_outcome: Kiểm tra đăng nhập với mã 123456 trả về 200 và thành công.
spine_outcome_lines: ["claude:0faf0bb2#L3851"]
spine_takeaway: Mã cố định kiểu dev chỉ dùng được khi APP_ENV không phải production; cần kiểm tra điều này trước khi dựa vào nó.
spine_takeaway_lines: ["claude:0faf0bb2#L3772"]
completeness: 6
---

# Chủ tự đăng nhập bằng mã cố định vì Multica không có mật khẩu và chỉ gửi mã vào log

**Bối cảnh:** Chủ muốn đăng nhập web Multica trên tailnet, nhưng server không gửi email (không có SMTP hay Resend) nên mã xác nhận chỉ nằm trong log.
**Chuyện gì xảy ra:** Multica không có đăng nhập bằng mật khẩu; chỉ có mã email và Google OAuth. Vì không có SMTP, mã nằm trong log của backend và phải lấy bằng lệnh docker logs. Để test, đặt MULTICA_DEV_VERIFICATION_CODE=123456, chỉ hoạt động khi APP_ENV không phải production.
**Bài học:** Mã cố định kiểu dev chỉ dùng được cho môi trường thử, không dùng cho sản xuất; luôn kiểm tra APP_ENV trước khi dựa vào nó.
**Artefact:** Ảnh màn hình trang đăng nhập (che email thật, không chụp mã).
**Góc người ngoài:** cách làm phổ biến là Cấu hình SMTP hoặc đăng nhập bằng Google/mật khẩu thật; ít khi đặt mã cố định, dù chỉ dùng trong tailnet; ở đây khác ở Người đọc muốn biết có an toàn không khi đặt mã cố định, và vì sao không cần gửi email thật cho bước thử nghiệm.
