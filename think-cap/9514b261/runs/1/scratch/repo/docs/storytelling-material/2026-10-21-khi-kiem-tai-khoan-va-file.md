---
id: 2026-10-21-khi-kiem-tai-khoan-va-file
date: 2026-10-21
repo: repo
status: raw
signals: []
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:9514b261#L2322", "claude:9514b261#L2358", "claude:9514b261#L3075", "claude:9514b261#L3162", "claude:9514b261#L3899"]
hook: "Kiểm file đăng nhập mà không in ra một ký tự khoá nào"
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

# Khi kiểm tài khoản và file đăng nhập, agent chỉ đọc số dòng, số bảng, độ dài khoá và loại ký tự. Email được che. Cơ sở dữ liệu được mở ở chế độ chỉ đọc. Nội dung khoá không bao giờ được in ra.

**Chuyện gì xảy ra:** Khi kiểm tài khoản và file đăng nhập, agent chỉ đọc số dòng, số bảng, độ dài khoá và loại ký tự. Email được che. Cơ sở dữ liệu được mở ở chế độ chỉ đọc. Nội dung khoá không bao giờ được in ra.
**Góc người ngoài:** cách làm phổ biến là Nhiều người mở file đăng nhập bằng cat hoặc dán nguyên nội dung vào chat để xem, hoặc không kiểm gì mà cứ thử; ở đây khác ở Cách này vẫn xác định được trạng thái đăng nhập mà không làm lộ bí mật. Người đọc muốn có cách kiểm tương tự khi làm việc với khoá API và phiên đăng nhập.
