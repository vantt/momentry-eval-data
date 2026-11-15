---
id: 2026-10-29-kaneo-noi-that-moi-thao-tac
date: 2026-10-29
repo: repo
status: raw
signals: [artefact nhìn được, ràng buộc định hình thiết kế]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L3314", "claude:0faf0bb2#L3317", "claude:0faf0bb2#L3329", "claude:0faf0bb2#L3332"]
hook: "Đổi tên một field ở server, giao diện báo lỗi ngay lúc build"
tension: none
sides: []
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Kaneo nối thật: mọi thao tác đi qua API, hc<AppType> bắt lỗi kiểu lúc build

**Bối cảnh:** So sánh web Kaneo với gr8r và Circle về việc dữ liệu được lưu ở đâu.
**Chuyện gì xảy ra:** Khi sửa một comment, Kaneo đi qua hook, fetcher, Hono RPC client rồi tới server ghi Postgres và phát realtime qua WebSocket. gr8r sửa thẳng mảng trong bộ nhớ và ghi cả khối JSON vào localStorage, còn Circle chỉ có dữ liệu mẫu. Kiểu của route được lấy từ code server, nên đổi tên field là TypeScript báo lỗi ngay ở UI.
**Bài học:** Dữ liệu thật nằm ở server là điều kiện để nhiều người và agent cùng ghi; kiểu chia sẻ giữa client và server bắt lỗi trước khi chạy.
**Artefact:** Sơ đồ chuỗi xử lý một lần sửa comment: UI → hook → fetcher → RPC → server → WebSocket.
