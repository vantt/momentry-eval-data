---
id: 2026-10-30-moi-lan-trien-khai-deu-chay
date: 2026-10-30
repo: repo
status: raw
signals: []
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:f0bf048d#L1211", "claude:f0bf048d#L1277", "claude:f0bf048d#L2459", "claude:f0bf048d#L2467", "claude:f0bf048d#L2556"]
hook: "Deploy xong chưa tính: phải chạy plan lại và ra đúng 0 thay đổi"
tension: none
sides: []
strength: 0
stakes: 2
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Mọi lần triển khai đều chạy plan trước, deploy sau, rồi chạy plan lại và phải ra đúng 0 thay đổi mới coi là xong.

**Chuyện gì xảy ra:** Mọi lần triển khai đều chạy plan trước, deploy sau, rồi chạy plan lại và phải ra đúng 0 thay đổi mới coi là xong.
**Góc người ngoài:** cách làm phổ biến là Chạy script deploy rồi tin là đã xong, không có bước kiểm tra lại trạng thái thực trên hệ thống; ở đây khác ở Kiểm tra idempotent bằng plan là cách biết trạng thái thật khớp với khai báo. Người đọc sẽ muốn áp dụng lại được cho hạ tầng của họ.
