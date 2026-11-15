---
id: 2026-10-21-truoc-khi-sua-file-cau-hinh-fd46
code: M-4VTR
aliases: [M-4VTR]
date: 2026-10-21
repo: repo
status: raw
signals: []
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:9514b261#L2422", "claude:9514b261#L2438", "claude:9514b261#L3038", "claude:9514b261#L3102", "claude:9514b261#L3847"]
hook: "Sửa file cấu hình toàn cục: sao lưu, chỉ thay khi khớp đúng một lần"
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

# Trước khi sửa file cấu hình toàn cục, agent sao lưu bản gốc có dấu thời gian, sửa bằng script chỉ thay khi chuỗi xuất hiện đúng một lần (assert count == 1), rồi kiểm lại cú pháp.

**Chuyện gì xảy ra:** Trước khi sửa file cấu hình toàn cục, agent sao lưu bản gốc có dấu thời gian, sửa bằng script chỉ thay khi chuỗi xuất hiện đúng một lần (assert count == 1), rồi kiểm lại cú pháp.
**Góc người ngoài:** cách làm phổ biến là Mở file bằng trình soạn thảo, sửa tay, và chỉ nhận ra lỗi khi chương trình khởi động không được; ở đây khác ở Có đường lùi rõ ràng và việc sửa không thể sai âm thầm. Lưu ý: vụ khoá TheHive cho thấy bước sao lưu chưa được áp dụng nhất quán. Người đọc sẽ muốn biết cách làm này đủ mạnh đến đâu.
