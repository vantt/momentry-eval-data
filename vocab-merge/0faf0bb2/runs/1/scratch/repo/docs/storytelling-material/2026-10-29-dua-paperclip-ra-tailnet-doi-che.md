---
id: 2026-10-29-dua-paperclip-ra-tailnet-doi-che
date: 2026-10-29
repo: repo
status: raw
signals: [ràng buộc định hình thiết kế, nguyên nhân]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:0faf0bb2#L1383", "claude:0faf0bb2#L1413", "claude:0faf0bb2#L1434", "claude:0faf0bb2#L1447", "claude:0faf0bb2#L1452", "claude:0faf0bb2#L1490"]
hook: "Mặc định ai vào được Paperclip là toàn quyền; đổi chế độ trước, đổi địa chỉ sau"
tension: none
sides: []
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đưa Paperclip ra tailnet: đổi chế độ xác thực trước, rồi mới đổi địa chỉ nghe

**Bối cảnh:** Người dùng muốn truy cập từ xa qua Tailscale. Máy có 9 thiết bị khác trong tailnet.
**Chuyện gì xảy ra:** Paperclip mặc định chạy local_trusted, nghĩa là ai vào được là có toàn quyền. Agent chuyển sang authenticated/private và bind vào IP tailnet. Loopback không còn trả lời, curl exit 7 là đúng như kỳ vọng. Muốn có tài khoản chủ phải claim bằng URL dùng một lần, và URL đăng nhập CLI cũng hết hạn sau vài phút, nên phải làm lại.
**Bài học:** Khi mở bind ra mạng, phải đổi chế độ xác thực trước. Các URL claim và cli-auth có hạn rất ngắn.
**Artefact:** Bảng so sánh hai cách: bind tailnet và tailscale serve.
