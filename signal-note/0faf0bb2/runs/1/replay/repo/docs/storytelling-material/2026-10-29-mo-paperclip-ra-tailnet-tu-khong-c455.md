---
id: 2026-10-29-mo-paperclip-ra-tailnet-tu-khong-c455
code: M-F129
aliases: [M-F129]
date: 2026-10-29
repo: repo
status: raw
signals: [rang_buoc_thiet_ke, nguyen_nhan_bat_ngo]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:0faf0bb2#L1383", "claude:0faf0bb2#L1413", "claude:0faf0bb2#L1417", "claude:0faf0bb2#L1433", "claude:0faf0bb2#L1447", "claude:0faf0bb2#L1452", "claude:0faf0bb2#L1490", "claude:0faf0bb2#L1505"]
hook: "Bật đăng nhập cho Paperclip xong, agent ngừng làm vì địa chỉ đổi"
tension: giup_ma_hai
sides: ["Bật đăng nhập để an toàn hơn", "Agent vẫn trỏ 127.0.0.1 nên ngừng làm việc"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Mở Paperclip ra tailnet: từ không đăng nhập sang có đăng nhập, agent tạm ngừng vì địa chỉ đổi

**Bối cảnh:** Chủ muốn vào Paperclip từ điện thoại qua Tailscale. Chế độ local_trusted cho phép ai truy cập cũng có quyền chủ.
**Chuyện gì xảy ra:** Chủ chọn cách A: bind tailnet và chế độ authenticated. Sau khi đổi, loopback không còn trả lời (exit 7, đúng như dự kiến), UI mở được qua hostname và IP. Vì agent vẫn trỏ 127.0.0.1 nên không làm việc được cho tới khi chủ nhận quyền chủ và đổi địa chỉ; link claim và link CLI đều hết hạn sau vài phút.
**Bài học:** Đổi bind hoặc chế độ xác thực sẽ đổi địa chỉ mà agent đang giữ; liệt kê các chỗ phụ thuộc địa chỉ trước khi đổi.
**Artefact:** Bảng so sánh hai cách A và B, không kèm địa chỉ.
