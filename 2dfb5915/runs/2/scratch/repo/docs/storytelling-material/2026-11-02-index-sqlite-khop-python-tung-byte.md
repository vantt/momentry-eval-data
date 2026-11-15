---
id: 2026-11-02-index-sqlite-khop-python-tung-byte
date: 2026-11-02
repo: repo
status: raw
signals: [số trước sau]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:2dfb5915#L941", "claude:2dfb5915#L949"]
hook: "Index khớp Python từng byte, build nhanh gấp 2,8 lần"
tension: it_ma_nhieu
sides: ["khớp từng byte với bản gốc", "nhanh gấp 2,8 lần, 21 ms so với 58 ms"]
strength: 1
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Index SQLite khớp Python từng byte, build nhanh gấp 2,8 lần

**Bối cảnh:** Phase 09 so toàn bộ DB với Python ở commit đã ghim.
**Chuyện gì xảy ra:** So SQL của mọi bảng và view, cùng thứ tự rowid, sau sáu kịch bản build: giống nhau, trừ rowid của schema_field và schema_link. Python chèn hai bảng này theo thứ tự set() thay đổi mỗi lần chạy. Build đầy đủ: Python 58,6 ms, Rust 21,2 ms. Build không đổi: 2,4 ms và 2,1 ms.
**Bài học:** Với bản gốc dùng set, so sánh nội dung chứ đừng so thứ tự chèn.
**Artefact:** Bảng thời gian hai bản.
**Góc người ngoài:** cách làm phổ biến là Port sang ngôn ngữ khác thường dựa vào vài test thủ công, hoặc viết lại test đơn vị rồi hy vọng hành vi giống nhau. Hiếm ai có kiểm tra so khớp tự động với bản cũ; ở đây khác ở Người đọc muốn biết cách biến bản cũ thành đặc tả chạy được. Mỗi phase song song có thước đo khách quan 'khớp hay lệch', nên agent nào xong cũng tự kiểm được và lead không phải đọc code để tin.
