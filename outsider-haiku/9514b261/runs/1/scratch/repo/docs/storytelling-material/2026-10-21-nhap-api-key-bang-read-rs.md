---
id: 2026-10-21-nhap-api-key-bang-read-rs
date: 2026-10-21
repo: repo
status: raw
signals: []
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:9514b261#L3864", "claude:9514b261#L3930"]
hook: "Nhập API key bằng một ô ẩn, không để lại dấu vết nào"
tension: none
sides: []
strength: 0
stakes: 0
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Nhập API key bằng `read -rs` trong terminal: key chỉ đi vào ô ẩn, không nằm trong lệnh, không vào lịch sử shell và không dán vào chat. Sau đó kiểm bằng một lệnh gọi thật, không in giá trị key.

**Chuyện gì xảy ra:** Nhập API key bằng `read -rs` trong terminal: key chỉ đi vào ô ẩn, không nằm trong lệnh, không vào lịch sử shell và không dán vào chat. Sau đó kiểm bằng một lệnh gọi thật, không in giá trị key.
**Góc người ngoài:** cách làm phổ biến là Nhiều người dán key thẳng vào lệnh (`export KEY=...`) hoặc gửi cho AI trong chat để nó 'ghi giúp'. Key khi đó nằm trong history shell và trong nội dung chat; ở đây khác ở Người đọc sẽ thấy key không đi qua chat hay history, và kiểm xác thực bằng một lệnh gọi thật thay vì tin rằng file đã ghi đúng. Đây là cách làm an toàn hơn mà người dùng AI hằng ngày ít khi biết.
