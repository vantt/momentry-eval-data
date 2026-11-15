---
id: 2026-11-03-ban-phat-hanh-thu-bi-github
date: 2026-11-03
repo: repo
status: raw
signals: [ràng buộc định hình thiết kế, nguyên nhân bất ngờ]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:2dfb5915#L3794", "claude:2dfb5915#L3804", "claude:2dfb5915#L3808"]
hook: "Bản rc.3 bị chặn vì thanh toán; chuyển repo sang public là chạy lại"
tension: it_ma_nhieu
sides: ["Actions chặn vì lỗi thanh toán hoặc hết hạn mức", "Chỉ đổi repo sang public là CI xanh, ra rc.3 với 7 file khớp checksum"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Bản phát hành thử bị GitHub Actions chặn vì thanh toán, phải đổi repo sang public

**Bối cảnh:** Repo private dùng số phút Actions tính phí. Mọi job bị từ chối, kể cả job dựng binary, dù code không lỗi.
**Chuyện gì xảy ra:** Thông báo báo lỗi thanh toán hoặc hết hạn mức. Người dùng đổi repo sang public, Actions miễn phí, CI chạy lại xanh rồi phát hành rc.3 với 7 file có checksum khớp.
**Bài học:** Kiểm tra billing và giới hạn Actions trước khi đẩy tag phát hành; lỗi chặn có thể không nằm ở code.
**Artefact:** Thông báo lỗi GitHub Actions (che tên tài khoản).
**Góc người ngoài:** cách làm phổ biến là Dev thường bấm chạy lại toàn bộ pipeline, hoặc cho rằng đỏ là do code rồi sửa code vô ích; ở đây khác ở Agent đọc log để tách 'lỗi code' khỏi 'lỗi hạ tầng', chạy lại chỉ job bị huỷ, và báo cho người dùng biết nguyên nhân thật (thanh toán, runner) thay vì đoán. Người đọc sẽ muốn biết cách phân biệt nhanh.
