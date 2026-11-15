---
id: 2026-11-01-doi-khoa-bi-mat-an-toan
date: 2026-11-01
repo: repo
status: raw
signals: []
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:f0bf048d#L2536", "claude:f0bf048d#L2549", "claude:f0bf048d#L2550"]
hook: "Thu hồi key cũ xong mới nhớ: còn một bản sao ở file khác"
tension: cam_ma_van_lot
sides: ["đã thu hồi key cũ và tạo key mới an toàn", "bản sao key cũ vẫn nằm ở file cấu hình khác"]
strength: 2
stakes: 1
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đổi khoá bí mật an toàn: tạo PAT mới, cập nhật mọi chỗ chứa bản cũ (tìm bằng grep nội dung khắp home), kiểm PAT mới chạy được rồi mới thu hồi PAT cũ, và xác nhận bản cũ hết hiệu lực.

**Chuyện gì xảy ra:** Đổi khoá bí mật an toàn: tạo PAT mới, cập nhật mọi chỗ chứa bản cũ (tìm bằng grep nội dung khắp home), kiểm PAT mới chạy được rồi mới thu hồi PAT cũ, và xác nhận bản cũ hết hiệu lực.
**Góc người ngoài:** cách làm phổ biến là Thu hồi key cũ rồi tạo key mới, hoặc quên mất bản sao còn nằm ở file cấu hình khác; ở đây khác ở Thứ tự 'tạo mới, thay mọi bản sao, kiểm, rồi mới thu hồi' tránh tự khoá mình; grep nội dung khắp home để tìm hết bản sao là mẹo ít ai nghĩ tới. Người đọc hay bỏ sót các bản sao trong profile CLI.
