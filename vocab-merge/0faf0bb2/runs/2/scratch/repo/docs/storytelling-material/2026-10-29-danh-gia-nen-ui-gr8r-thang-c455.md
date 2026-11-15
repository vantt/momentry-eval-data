---
id: 2026-10-29-danh-gia-nen-ui-gr8r-thang-c455
code: M-FS5P
aliases: [M-FS5P]
date: 2026-10-29
repo: repo
status: raw
signals: [số, điều tưởng đúng]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L3302", "claude:0faf0bb2#L3329"]
hook: "Thiết kế đẹp nhất lại thua vì không có nền để xây"
tension: tuong_ma_hoa_ra
sides: ["gr8r thắng về thiết kế", "Dữ liệu nằm trong localStorage, id sinh ở trình duyệt nên dễ trùng"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đánh giá nền UI: gr8r thắng về thiết kế, nhưng thua vì không có nền để xây

**Bối cảnh:** So sánh gr8r với Circle và Kaneo để chọn nền giao diện cho OPC.
**Chuyện gì xảy ra:** gr8r lưu cả khối dữ liệu trong localStorage và sinh id ở trình duyệt, nên dễ trùng khi nhiều người cùng ghi. Circle đọc khoảng 20 store zustand từ mock. Kaneo web gọi API thật qua Hono RPC, mã task do server cấp và có sẵn vi-VN.json. Cùng một thao tác sửa comment: gr8r ghi localStorage, Circle chỉ đổi bộ nhớ, Kaneo gửi HTTP PUT rồi phát sự kiện WebSocket.
**Bài học:** Đẹp chưa đủ. Kiểm tra nơi lưu dữ liệu, cách sinh id và i18n trước khi chọn nền.
**Artefact:** Bảng so sánh ba cột gr8r, Circle và Kaneo.
