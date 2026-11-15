---
id: 2026-10-30-ngay-sau-khi-tao-credential-service-f60d
code: M-XAZ6
aliases: [M-XAZ6]
date: 2026-10-30
repo: repo
status: raw
signals: []
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:f0bf048d#L747", "claude:f0bf048d#L748", "claude:f0bf048d#L749", "claude:f0bf048d#L766", "claude:f0bf048d#L767"]
hook: "Có file key chưa đủ, phải gọi thử API ngay khi tạo"
tension: tuong_ma_hoa_ra
sides: ["có file key là tưởng xong", "lỗi xác thực chỉ lộ ra lúc cần gấp"]
strength: 1
stakes: 0
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Ngay sau khi tạo credential (service account key), gọi thử API bằng chính key đó để xác nhận xác thực chạy được, dù chưa có quyền truy cập dữ liệu. Kết quả rỗng được coi là đủ để biết bước xác thực đã thông.

**Chuyện gì xảy ra:** Ngay sau khi tạo credential (service account key), gọi thử API bằng chính key đó để xác nhận xác thực chạy được, dù chưa có quyền truy cập dữ liệu. Kết quả rỗng được coi là đủ để biết bước xác thực đã thông.
**Góc người ngoài:** cách làm phổ biến là Thường người ta chỉ kiểm tra có file key hay chưa, rồi đợi đến khi có quyền mới thử, nên lỗi xác thực chỉ lộ ra lúc cần dùng gấp; ở đây khác ở Tách được hai lớp lỗi: lỗi xác thực (do hệ thống) và lỗi thiếu quyền (do người). Người đọc sẽ muốn biết cách kiểm tra lớp đầu sớm để khỏi chờ vô ích.
