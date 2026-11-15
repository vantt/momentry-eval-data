---
id: 2026-10-21-doi-ten-tai-khoan-theo-nha
date: 2026-10-21
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L3070", "claude:9514b261#L3091", "claude:9514b261#L3153", "claude:9514b261#L3162", "claude:9514b261#L3178"]
hook: "Đổi tên tài khoản mà không xoá gì: profile trống được dời đi, không mất"
tension: none
sides: []
strength: 0
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đổi tên tài khoản theo nhà cung cấp: di chuyển thư mục thay vì xoá, sau khi kiểm tham chiếu

**Bối cảnh:** Một tài khoản đặt tên lệch với các tài khoản khác cùng nhà cung cấp, cần thống nhất trước khi cấu hình chạy.
**Chuyện gì xảy ra:** Trước khi đổi, em đếm số bảng auth để chắc profile mới tạo chưa có đăng nhập. Profile chưa đăng nhập được chuyển sang scratchpad thay vì xoá. Alias cũ được giữ trong lệnh unalias để source lại không lỗi. Sau khi đổi, bước đăng nhập mới được kiểm và nối vào fgOS.
**Bài học:** Đặt tên theo nhà cung cấp ngay từ đầu. Khi đổi, kiểm tham chiếu trước và di chuyển thay vì xoá.
**Artefact:** Danh sách tên trước và sau khi đổi, không ghi đường dẫn đăng nhập.
