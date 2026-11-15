---
id: 2026-11-03-ci-khong-chay-vi-thanh-toan
date: 2026-11-03
repo: repo
status: raw
signals: [ràng buộc, khác]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [hotspot, harvest, outsider]
lines: ["claude:2dfb5915#L3794", "claude:2dfb5915#L3804", "claude:2dfb5915#L3830", "claude:2dfb5915#L3847"]
hook: "CI không chạy vì thanh toán lỗi, repo public thì miễn phí"
tension: khac
sides: ["CI chết vì thanh toán lỗi", "chuyển public thì chạy miễn phí"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# CI không chạy vì thanh toán lỗi, repo chuyển public, và quét lịch sử git trước khi mở

**Bối cảnh:** Repo private dùng Actions tính phí. Release bị từ chối trước khi job nào khởi động.
**Chuyện gì xảy ra:** GitHub báo thanh toán lỗi hoặc hết hạn mức, nên mọi job không chạy, kể cả job dựng binary. Máy agent không cross-compile được binary Windows và macOS. Chủ repo chuyển sang public thì Actions miễn phí, CI xanh. Trước khi công khai, agent quét toàn bộ lịch sử git theo mẫu token GitHub, khoá Anthropic, khoá AWS và private key. Lần đầu lệnh quét bị cổng xác nhận chặn, lần sau thu hẹp lệnh thì không khớp.
**Bài học:** Kiểm hạn mức và thanh toán CI trước khi đặt ngày phát hành. Quét lịch sử git trước khi mở public.
**Artefact:** Ảnh thông báo job not started, che tên tài khoản.
**Góc người ngoài:** cách làm phổ biến là Đa số mở public rồi mới nhớ ra, hoặc chỉ xoá secret ở commit mới nhất và bỏ qua lịch sử; ở đây khác ở Secret nằm trong lịch sử git vẫn lộ dù đã xoá ở commit sau. Một lệnh grep trên `git log --all -p` rẻ và đủ để bắt các khoá phổ biến, người đọc có thể dùng ngay.
