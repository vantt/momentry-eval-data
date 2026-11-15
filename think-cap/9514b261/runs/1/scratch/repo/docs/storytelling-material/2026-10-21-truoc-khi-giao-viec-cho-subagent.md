---
id: 2026-10-21-truoc-khi-giao-viec-cho-subagent
date: 2026-10-21
repo: repo
status: raw
signals: []
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:9514b261#L923", "claude:9514b261#L1330", "claude:9514b261#L1347"]
hook: "Trước khi giao việc cho subagent, agent hỏi lệnh dispatch decide đã"
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

# Trước khi giao việc cho subagent, agent chạy một lệnh kiểm tra cách điều phối (`dispatch decide`) và lấy đường dẫn file báo cáo từ lệnh quy ước của repo, thay vì tự đặt tên file.

**Chuyện gì xảy ra:** Trước khi giao việc cho subagent, agent chạy một lệnh kiểm tra cách điều phối (`dispatch decide`) và lấy đường dẫn file báo cáo từ lệnh quy ước của repo, thay vì tự đặt tên file.
**Góc người ngoài:** cách làm phổ biến là Phần lớn người dùng AI mở thẳng một subagent, bảo nó ghi kết quả vào một file tự đặt tên, rồi đọc kết quả; ở đây khác ở Quy trình này tách việc quyết định cách chạy khỏi việc chạy, nên tên file và cách chạy nhất quán giữa các lượt. Người đọc muốn biết vì sao cần một bước kiểm trước khi chạy agent con.
