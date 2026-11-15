---
id: 2026-10-21-khong-in-gia-tri-bi-mat-fd46
code: M-WP6E
aliases: [M-WP6E]
date: 2026-10-21
repo: repo
status: raw
signals: []
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:9514b261#L2024", "claude:9514b261#L2038", "claude:9514b261#L3531", "claude:9514b261#L3864", "claude:9514b261#L3895"]
hook: "Khoá API nhập bằng read -s, chỉ kiểm độ dài chứ không bao giờ in ra"
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

# Không in giá trị bí mật. Email được che, khóa API chỉ được kiểm bằng độ dài và loại ký tự, và khóa được nhập bằng read -s để không vào lịch sử shell.

**Chuyện gì xảy ra:** Không in giá trị bí mật. Email được che, khóa API chỉ được kiểm bằng độ dài và loại ký tự, và khóa được nhập bằng read -s để không vào lịch sử shell.
**Góc người ngoài:** cách làm phổ biến là Dùng cat để xem file cấu hình hoặc dán thẳng khóa vào lệnh; ở đây khác ở Agent vẫn xác minh được khóa đúng định dạng mà không lộ nội dung. Người dùng có thể làm theo cách này mà không để khóa nằm trong log hay lịch sử.
