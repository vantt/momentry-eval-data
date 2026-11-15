---
id: 2026-10-29-dang-nhap-khong-mat-khau-ma-c455
code: M-JB40
aliases: [M-JB40]
date: 2026-10-29
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:0faf0bb2#L3650", "claude:0faf0bb2#L3654", "claude:0faf0bb2#L3772", "claude:0faf0bb2#L3785", "claude:0faf0bb2#L3788", "claude:0faf0bb2#L3793", "claude:0faf0bb2#L3806", "claude:0faf0bb2#L3850", "claude:0faf0bb2#L3856"]
hook: "Mã xác nhận chỉ nhận đúng 6 chữ số, mã chữ bị từ chối"
tension: nho_ma_to
sides: ["Đặt mã cố định cho bản thử, tưởng chữ nào cũng được", "Chỉ 6 chữ số mới hợp lệ, và tuyệt đối không bật ở production"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đăng nhập không mật khẩu: mã xác nhận và mã cố định cho bản thử

**Bối cảnh:** Công cụ không có đăng nhập bằng mật khẩu, chỉ có mã 6 số gửi qua email hoặc Google.
**Chuyện gì xảy ra:** Chưa cấu hình email nên mã xác nhận nằm trong log và hết hạn sau 10 phút. Phương án mã cố định qua biến môi trường chỉ chấp nhận đúng 6 chữ số, nên phải đặt lại mã có 6 chữ số thay vì chữ. Sau khi đổi, đăng nhập thử thành công và daemon vẫn online. Mã này chỉ dùng cho bản thử trong mạng riêng và không được bật ở chế độ production.
**Bài học:** Công cụ không có mật khẩu chỉ an toàn khi mở trong mạng riêng và không ở chế độ production. Ghi rõ đó là bản thử để không bị đưa ra ngoài.
**Artefact:** Bảng bốn cách đăng nhập (email SMTP, Google, mã cố định, đọc log). Không chụp màn hình mã.
**Góc người ngoài:** cách làm phổ biến là Thiết lập tài khoản bằng mật khẩu hoặc SMTP thật; nếu không có email thì phải cấu hình dịch vụ gửi mail trước khi đăng nhập được; ở đây khác ở Agent phát hiện Multica không có mật khẩu, liệt kê 4 cách thay thế với ưu nhược, rồi user chọn mã cố định, agent kiểm tra quy tắc mã (6 chữ số) trong code và đổi giá trị khi user yêu cầu. Người đọc sẽ muốn làm tương tự khi cần truy cập demo nhanh.
