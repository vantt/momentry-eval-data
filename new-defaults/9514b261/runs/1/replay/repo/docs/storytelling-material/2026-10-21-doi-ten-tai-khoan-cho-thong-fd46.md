---
id: 2026-10-21-doi-ten-tai-khoan-cho-thong-fd46
code: M-YSBE
aliases: [M-YSBE]
date: 2026-10-21
repo: repo
status: raw
signals: [nguoi_duyet_may_soan]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L2982", "claude:9514b261#L3070", "claude:9514b261#L3111", "claude:9514b261#L3127", "claude:9514b261#L3131", "claude:9514b261#L3153"]
hook: "Đổi tên tài khoản: liệt kê mọi chỗ tham chiếu trước, không xoá profile nhầm"
tension: none
sides: []
strength: 0
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đổi tên tài khoản cho thống nhất: nhiều chỗ tham chiếu, và một profile tạo nhầm phải chuyển đi

**Bối cảnh:** Người dùng muốn tên profile theo họ nhà cung cấp thay cho tên cũ.
**Chuyện gì xảy ra:** Agent tạo một profile theo yêu cầu đầu, rồi người dùng đổi ý. Agent kiểm profile đó chưa đăng nhập (0 dòng credential) và chuyển đi thay vì xoá. Khi đổi tên thư mục pi, agent liệt kê mọi chỗ tham chiếu trong zshrc và config trước rồi mới đổi. Kiểm lại thì fgOS không còn chỗ nào trỏ tới tên cũ.
**Bài học:** Trước khi đổi tên một tài khoản, grep mọi nơi tham chiếu gồm alias, config và trạng thái. Chuyển đi thay vì xoá.
**Artefact:** Danh sách alias trước và sau khi đổi tên, không kèm đường dẫn cá nhân.
