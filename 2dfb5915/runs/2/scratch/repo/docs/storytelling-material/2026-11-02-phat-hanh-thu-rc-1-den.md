---
id: 2026-11-02-phat-hanh-thu-rc-1-den
date: 2026-11-02
repo: repo
status: raw
signals: [artefact, khác]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:2dfb5915#L2536", "claude:2dfb5915#L3551", "claude:2dfb5915#L3917"]
hook: "Ba bản phát hành thử, một job macOS bị huỷ vì chờ runner"
tension: none
sides: []
strength: 0
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Phát hành thử rc.1 đến rc.3: 7 file, sha256, job macOS bị huỷ

**Bối cảnh:** Phát hành thử từ v0.1.0-rc.1 đến rc.3 bằng workflow release.
**Chuyện gì xảy ra:** Mỗi bản có 7 file: 4 binary, 2 script cài và checksums. Ở rc.2, job macOS Intel bị GitHub huỷ vì chờ runner quá lâu, phải chạy lại. API trả HTTP 500 lần đầu khi yêu cầu chạy lại. rc.3 dựng từ nhánh tính năng, và chạy được sau khi repo public.
**Bài học:** Đừng coi job bị huỷ là lỗi code. Chạy lại đúng job rồi kiểm lại sha256.
**Artefact:** Danh sách 7 file của release, không cần nội dung.
**Góc người ngoài:** cách làm phổ biến là Gắn tag, thấy workflow xanh rồi coi như xong. Ít ai tải lại tài sản đã đăng để kiểm tra checksum; ở đây khác ở Gói nhị phân cho Windows và macOS không chạy được trên máy dev Linux. Cách duy nhất biết bản phát hành có đủ file và checksum đúng là tải về kiểm, và thử bằng dispatch trước khi gắn tag nên lỗi lộ ra mà chưa có bản nào bị đăng sai.
