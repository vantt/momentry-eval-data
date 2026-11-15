---
id: 2026-10-29-multica-khong-co-dang-nhap-bang
date: 2026-10-29
repo: repo
status: raw
signals: [ràng buộc thiết kế]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L3650", "claude:0faf0bb2#L3772", "claude:0faf0bb2#L3785", "claude:0faf0bb2#L3787", "claude:0faf0bb2#L3806", "claude:0faf0bb2#L3856"]
hook: "Không có đăng nhập mật khẩu: mã xác nhận lấy từ log, test thì đặt mã cố định"
tension: none
sides: []
strength: 0
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Multica không có đăng nhập bằng mật khẩu: spike dùng mã xác nhận từ log rồi đổi sang mã test cố định

**Bối cảnh:** Người dùng hỏi có cách đặt mật khẩu cho chủ không. Multica chỉ có đăng nhập bằng mã email và Google OAuth, không có mật khẩu.
**Chuyện gì xảy ra:** Ban đầu mình lấy mã xác nhận từ log backend mỗi lần đăng nhập, mã có hiệu lực 10 phút. Để tiện test, mình đặt biến MULTICA_DEV_VERIFICATION_CODE, chỉ có tác dụng khi APP_ENV không phải production. Mình ghi rõ đây là cấu hình test và không dùng cho triển khai thật.
**Bài học:** Một công cụ không có mật khẩu sẽ buộc phải dùng đường đăng nhập khác khi test. Đặt cờ dev phải đi kèm ghi chú rõ đây là cấu hình chỉ dành cho test.
**Artefact:** Dòng log backend có mã đã che, và đoạn cấu hình cờ dev không hiện giá trị.
