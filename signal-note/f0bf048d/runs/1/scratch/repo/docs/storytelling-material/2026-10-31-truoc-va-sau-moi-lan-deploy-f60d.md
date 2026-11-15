---
id: 2026-10-31-truoc-va-sau-moi-lan-deploy-f60d
code: M-TN42
aliases: [M-TN42]
date: 2026-10-31
repo: repo
status: raw
signals: []
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:f0bf048d#L1780", "claude:f0bf048d#L2459", "claude:f0bf048d#L2466", "claude:f0bf048d#L2555", "claude:f0bf048d#L2556"]
hook: "Deploy xong plan phải báo 0 thay đổi, có thay đổi lạ thì dừng"
tension: none
sides: []
strength: 0
stakes: 1
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Trước và sau mỗi lần deploy, chạy lệnh plan. Sau deploy, plan lại phải báo 0 thay đổi. Khi plan có thay đổi ngoài yêu cầu thì dừng lại hỏi.

**Chuyện gì xảy ra:** Trước và sau mỗi lần deploy, chạy lệnh plan. Sau deploy, plan lại phải báo 0 thay đổi. Khi plan có thay đổi ngoài yêu cầu thì dừng lại hỏi.
**Góc người ngoài:** cách làm phổ biến là Thường deploy thẳng rồi kiểm tra bằng mắt, hoặc không có lệnh xem trước nên không biết lần deploy sẽ đụng vào đâu; ở đây khác ở Có một lệnh xem trước và một tiêu chí kiểm tra rõ ràng sau deploy. Người đọc sẽ muốn áp dụng điều này cho các hệ thống của mình.
