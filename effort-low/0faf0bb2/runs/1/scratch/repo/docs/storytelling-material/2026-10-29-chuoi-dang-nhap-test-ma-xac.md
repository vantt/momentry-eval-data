---
id: 2026-10-29-chuoi-dang-nhap-test-ma-xac
date: 2026-10-29
repo: repo
status: raw
signals: [ràng buộc định hình thiết kế, nguyên nhân bất ngờ]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:0faf0bb2#L3650", "claude:0faf0bb2#L3656", "claude:0faf0bb2#L3784", "claude:0faf0bb2#L3788", "claude:0faf0bb2#L3793", "claude:0faf0bb2#L3850", "claude:0faf0bb2#L3856"]
hook: "Mã đăng nhập chỉ nằm trong log server, cuối cùng đặt cứng 123456"
tension: khac
sides: ["mã xác nhận bảo mật chỉ có trong log container", "giải pháp là đặt cố định 123456 cho môi trường test"]
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Chuỗi đăng nhập test: mã xác nhận chỉ nằm trong log server, rồi đặt mã cố định 123456

**Bối cảnh:** Multica không có mật khẩu, chỉ có mã email. Không cấu hình SMTP nên mã chỉ in ra log backend.
**Chuyện gì xảy ra:** Mã được ghi vào log của container, nên phải đọc log để lấy. Multica không có đăng nhập mật khẩu; chỉ biến MULTICA_DEV_VERIFICATION_CODE bị bỏ qua nếu APP_ENV=production. Đặt mã cố định 135790, sau đó đổi thành 123456 theo yêu cầu, backend restart và đăng nhập thử thành công.
**Bài học:** Với công cụ không có mật khẩu, mã cố định chỉ dùng được ngoài production; cần ghi rõ để không đưa cấu hình test lên môi trường thật.
**Artefact:** Dòng log 'no email backend configured... Verification code'. Che: mã thật, email.
**Góc người ngoài:** cách làm phổ biến là Nhiều người dùng sẽ bỏ qua bước đăng nhập, hoặc đặt mật khẩu yếu mà không biết mình đang tạo rủi ro gì; ở đây khác ở Người đọc sẽ hỏi làm sao để biết cách đăng nhập nào an toàn đủ cho thử nghiệm và cách hoàn tác khi chuyển sang môi trường thật.
