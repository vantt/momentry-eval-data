---
id: 2026-10-21-khi-can-doc-file-chua-bi
date: 2026-10-21
repo: repo
status: raw
signals: []
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:9514b261#L2304", "claude:9514b261#L2322", "claude:9514b261#L2358", "claude:9514b261#L3075", "claude:9514b261#L3162", "claude:9514b261#L3530", "claude:9514b261#L3570"]
hook: "Agent đọc file chứa khoá API mà không để lộ một ký tự"
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

# Khi cần đọc file chứa bí mật hoặc cấu hình nhạy cảm, agent chỉ đếm số dòng, số bảng, tên khoá, hoặc che giá trị bằng regex trước khi in ra. Email và khoá API không bao giờ hiện nguyên văn trong kết quả.

**Chuyện gì xảy ra:** Khi cần đọc file chứa bí mật hoặc cấu hình nhạy cảm, agent chỉ đếm số dòng, số bảng, tên khoá, hoặc che giá trị bằng regex trước khi in ra. Email và khoá API không bao giờ hiện nguyên văn trong kết quả.
**Góc người ngoài:** cách làm phổ biến là Thường người làm cat cả file ra màn hình, rồi mới nhận ra đã lộ khoá trong log hoặc lịch sử chat; ở đây khác ở Có thể kiểm tra trạng thái đăng nhập và cấu hình mà không làm lộ thông tin xác thực, nên an toàn hơn khi làm việc có log được lưu.
