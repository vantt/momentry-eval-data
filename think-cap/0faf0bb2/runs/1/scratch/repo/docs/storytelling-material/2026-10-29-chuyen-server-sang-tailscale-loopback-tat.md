---
id: 2026-10-29-chuyen-server-sang-tailscale-loopback-tat
date: 2026-10-29
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, số trước/sau]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:0faf0bb2#L1434", "claude:0faf0bb2#L1447", "claude:0faf0bb2#L1452", "claude:0faf0bb2#L1490", "claude:0faf0bb2#L1505"]
hook: "Server đã chuyển sang Tailscale, nhưng 3 agent vẫn gõ cửa địa chỉ cũ"
tension: tuong_ma_hoa_ra
sides: ["Đổi địa chỉ server là xong, health check cũ fail đúng dự kiến", "3 agent vẫn trỏ loopback nên không làm việc được"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Chuyển server sang Tailscale: loopback tắt, nhưng agent vẫn trỏ địa chỉ cũ

**Bối cảnh:** Mở Paperclip cho các máy trong tailnet, chuyển từ bind loopback sang bind tailnet với chế độ đăng nhập.
**Chuyện gì xảy ra:** Health check trên 127.0.0.1 trả exit 7, đúng như dự kiến vì server không còn nghe loopback. Nhưng cấu hình paperclipApiUrl của 3 agent vẫn trỏ địa chỉ loopback, nên agent không làm việc được cho tới khi chủ đăng nhập. Link xác thực CLI hết hạn sau vài phút, phải tạo lại. Lỗi nằm ở chỗ đổi địa chỉ server mà không quét các client đang trỏ địa chỉ cũ.
**Bài học:** Khi đổi địa chỉ dịch vụ, liệt kê mọi client đang trỏ địa chỉ cũ và đổi cùng lúc, không để chúng hỏng âm thầm.
**Artefact:** Bảng 2 cách mở tailnet: bind trực tiếp và tailscale serve (HTTPS).
