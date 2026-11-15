---
id: 2026-10-21-doi-ten-tai-khoan-kiem-dang
date: 2026-10-21
repo: repo
status: raw
signals: [ràng buộc định hình thiết kế]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L3074", "claude:9514b261#L3075", "claude:9514b261#L3084", "claude:9514b261#L3118", "claude:9514b261#L3162", "claude:9514b261#L3171"]
hook: "Đếm số dòng đăng nhập trước khi đổi tên để không mất phiên"
tension: none
sides: []
strength: 0
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đổi tên tài khoản: kiểm đăng nhập trước khi đổi để không làm mất phiên

**Bối cảnh:** Người dùng yêu cầu đặt tên thống nhất theo họ nhà cung cấp cho các profile và tài khoản đã tạo.
**Chuyện gì xảy ra:** Trước khi xoá hoặc đổi tên, agent đếm số dòng trong bảng đăng nhập của từng profile. Một profile vừa tạo có 0 đăng nhập nên an toàn để chuyển đi. Profile còn lại có 1 đăng nhập và được nối vào fgOS sau khi đổi tên. Agent chỉ đếm số dòng, không đọc nội dung đăng nhập.
**Bài học:** Đếm dữ liệu đăng nhập trước khi đổi tên hoặc xoá; chuyển sang thư mục tạm thay vì xoá.
**Artefact:** Bảng profile với cột số đăng nhập, không kèm tên thật và không kèm nội dung.
