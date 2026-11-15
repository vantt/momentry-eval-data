---
id: 2026-11-02-bien-tai-lieu-huong-dan-cho-c4b4
code: M-93HF
aliases: [M-93HF]
date: 2026-11-02
repo: repo
status: raw
signals: []
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:6a207191#L317", "claude:6a207191#L536", "claude:6a207191#L856", "claude:6a207191#L2364"]
hook: "Biến tài liệu cho agent thành quy tắc có mã ID, có lint kiểm tra liên kết"
tension: none
sides: []
strength: 1
stakes: 1
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Biến tài liệu hướng dẫn cho agent thành bộ quy tắc có mã ID (ví dụ CMD-22), mỗi quy tắc một dòng. Một script lint kiểm tra cấu trúc và việc các ID được tham chiếu có tồn tại. Một script khác kiểm tra mọi đường dẫn tới code mẫu còn đúng trên GitHub.

**Chuyện gì xảy ra:** Biến tài liệu hướng dẫn cho agent thành bộ quy tắc có mã ID (ví dụ CMD-22), mỗi quy tắc một dòng. Một script lint kiểm tra cấu trúc và việc các ID được tham chiếu có tồn tại. Một script khác kiểm tra mọi đường dẫn tới code mẫu còn đúng trên GitHub.
**Góc người ngoài:** cách làm phổ biến là Skill hoặc prompt thường là file markdown tự do, không có ID, và thường không ai kiểm tra xem liên kết hay đường dẫn trong đó còn đúng sau khi sửa; ở đây khác ở Tài liệu cho agent được xử lý như code: có ID để tham chiếu và có kiểm tra tự động để phát hiện liên kết hỏng. Người đọc sẽ muốn biết cách làm này và vì sao cần đến.
