---
id: 2026-11-03-release-lap-ci-khong-chay-vi
date: 2026-11-03
repo: repo
status: raw
signals: [Nguyên nhân bất ngờ, khác]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:2dfb5915#L3785", "claude:2dfb5915#L3794", "claude:2dfb5915#L3804", "claude:2dfb5915#L3808"]
hook: "CI không chạy vì thẻ thanh toán lỗi, public repo là thoát"
tension: nho_ma_to
sides: ["Hạn mức thanh toán bị chặn, không job nào chạy", "Chuyển repo sang public là CI xanh lại, ra rc.3"]
strength: 2
stakes: 1
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
**Góc người ngoài:** cách làm phổ biến là Thường người làm sẽ chờ hoặc đổi cách làm mà không báo rõ nguyên nhân, hoặc tự ý đổi quyền truy cập; ở đây khác ở Người đọc sẽ quan tâm vì agent không tự quyết việc có tính rủi ro (đổi public) mà hỏi lại, và chỉ làm sau khi user đã chốt; đồng thời kiểm lịch sử git tìm bí mật trước khi public.
