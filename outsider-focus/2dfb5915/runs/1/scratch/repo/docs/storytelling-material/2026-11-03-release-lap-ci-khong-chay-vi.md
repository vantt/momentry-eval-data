---
id: 2026-11-03-release-lap-ci-khong-chay-vi
date: 2026-11-03
repo: repo
status: raw
signals: [Nguyên nhân bất ngờ, khác]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L3785", "claude:2dfb5915#L3794", "claude:2dfb5915#L3804", "claude:2dfb5915#L3808"]
hook: "CI đứng vì thẻ thanh toán lỗi, cách thoát là public repo"
tension: nho_ma_to
sides: ["Một khoản thanh toán thất bại", "Không job nào chạy, kể cả build binary, đến khi phải public repo"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Release lặp: CI không chạy vì hết hạn mức thanh toán, rồi public repo để thoát

**Bối cảnh:** Repo để private nên GitHub Actions tính phí theo phút; mọi job cho một tag rc.3 bị từ chối.
**Chuyện gì xảy ra:** Thông báo GitHub ghi 'recent account payments have failed or your spending limit needs to be increased', nên không job nào chạy kể cả build binary. Agent không tự dựng binary Windows/macOS được ở máy Linux nên dừng và chờ người dùng xử lý billing. Người dùng chuyển repo sang public, CI chạy lại xanh, rc.3 phát hành với 7 file và checksum khớp.
**Bài học:** Pipeline phát hành đa nền tảng phụ thuộc hạn mức Actions; kiểm billing trước khi gắn tag, không phải sau.
**Artefact:** Thông báo lỗi billing của GitHub (che tên tài khoản).
