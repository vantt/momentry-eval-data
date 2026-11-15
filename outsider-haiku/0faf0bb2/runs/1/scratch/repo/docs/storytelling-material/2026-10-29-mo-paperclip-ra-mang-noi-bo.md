---
id: 2026-10-29-mo-paperclip-ra-mang-noi-bo
date: 2026-10-29
repo: repo
status: raw
signals: [ràng buộc thiết kế]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L1413", "claude:0faf0bb2#L1434", "claude:0faf0bb2#L1452", "claude:0faf0bb2#L1487", "claude:0faf0bb2#L1490"]
hook: "Mở ra mạng nội bộ, loopback tắt ngay, và chủ phải nhận quyền bằng URL dùng một lần"
tension: khac
sides: ["trước đó ai vào cũng là chủ", "mở mạng nội bộ thì chính máy mình cũng phải nhận quyền"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Mở Paperclip ra mạng nội bộ: đổi từ 'ai vào cũng là chủ' sang đăng nhập

**Bối cảnh:** Paperclip đang chạy chế độ local_trusted, ai truy cập được là có toàn quyền chủ. Người dùng muốn truy cập từ điện thoại qua mạng riêng, nơi có 9 máy khác.
**Chuyện gì xảy ra:** Mình chuyển sang chế độ authenticated, bind vào địa chỉ mạng riêng và giữ bản sao cấu hình cũ. Sau khi đổi, loopback không còn trả lời, đúng như dự kiến. Chủ phải nhận quyền bằng một URL claim dùng một lần; URL phê duyệt CLI thì hết hạn sau vài phút trong lúc chờ người dùng.
**Bài học:** Mở một dịch vụ ra mạng có nhiều máy thì chuyển sang chế độ có đăng nhập trước, rồi mới mở. Ghi lại URL hết hạn để không mất lượt phê duyệt.
**Artefact:** Bảng hai cách truy cập: bind tailnet so với tailscale serve kèm HTTPS. Che hostname và IP.
