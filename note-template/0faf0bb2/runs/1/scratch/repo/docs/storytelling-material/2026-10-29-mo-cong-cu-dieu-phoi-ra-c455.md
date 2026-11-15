---
id: 2026-10-29-mo-cong-cu-dieu-phoi-ra-c455
code: M-3TA0
aliases: [M-3TA0]
date: 2026-10-29
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:0faf0bb2#L1383", "claude:0faf0bb2#L1387", "claude:0faf0bb2#L1413", "claude:0faf0bb2#L1417", "claude:0faf0bb2#L1433", "claude:0faf0bb2#L1434", "claude:0faf0bb2#L1447", "claude:0faf0bb2#L1452", "claude:0faf0bb2#L1490", "claude:0faf0bb2#L1505"]
hook: "Mở ra mạng riêng 9 máy, đổi địa chỉ làm toàn bộ agent chết"
tension: giup_ma_hai
sides: ["Bật chế độ đăng nhập để an toàn trước 9 máy khác", "Địa chỉ cũ ngừng trả lời, từng agent phải cập nhật lại và link hết hạn vài phút"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Mở công cụ điều phối ra mạng riêng: đổi sang chế độ có đăng nhập

**Bối cảnh:** Công cụ đang chạy ở chế độ tin tưởng cục bộ, nghĩa là ai truy cập được là có quyền chủ. Người dùng muốn vào từ máy khác trong mạng riêng.
**Chuyện gì xảy ra:** Mạng riêng có 9 máy khác, nên phải chuyển sang chế độ có đăng nhập trước khi mở ra. Đổi địa chỉ lắng nghe làm địa chỉ cũ ngừng trả lời, nên các agent vẫn trỏ về địa chỉ nội bộ và không hoạt động cho tới khi cập nhật từng agent. Link tạo quyền chủ và link cấp quyền CLI đều hết hạn trong vài phút, nên phải tạo lại link sau khi đăng ký xong. Sau đó giao diện mở được cả qua tên máy lẫn IP trong mạng riêng.
**Bài học:** Đổi địa chỉ lắng nghe là đổi địa chỉ của mọi client. Cập nhật cấu hình client trước khi báo là xong, và coi link đăng nhập một lần là thứ hết hạn nhanh.
**Artefact:** Ảnh trang đăng nhập và bảng so sánh hai cách mở (bind trực tiếp và HTTPS qua serve). Che URL và token.
