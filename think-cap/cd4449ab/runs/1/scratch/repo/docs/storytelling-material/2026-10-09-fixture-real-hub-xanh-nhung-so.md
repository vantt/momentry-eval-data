---
id: 2026-10-09-fixture-real-hub-xanh-nhung-so
date: 2026-10-09
repo: repo
status: raw
signals: []
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest, outsider]
lines: ["omp:cd4449ab#L1618", "omp:cd4449ab#L1627", "omp:cd4449ab#L1639", "omp:cd4449ab#L1648", "omp:cd4449ab#L1713", "omp:cd4449ab#L1779", "omp:cd4449ab#L1828", "omp:cd4449ab#L1831", "omp:cd4449ab#L1888", "omp:cd4449ab#L1890"]
hook: "Test xanh mà tên skill đã đổi, so trước/sau mới lộ"
tension: cam_ma_van_lot
sides: ["Fixture chỉ kiểm trust, status và digest, đều xanh", "Tên 'test-audit' thành 'Test Audit' mà không test nào thấy"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Fixture real-hub xanh, nhưng so sánh skill show trước/sau bắt hồi quy

**Bối cảnh:** Test TestRealHubFixtureMigrationV1ToV2ToV3 đã xanh và lead yêu cầu diff skill show --json giữa binary cũ và mới.
**Chuyện gì xảy ra:** Test trước đó chỉ kiểm trust verdict, upstream status và ContentDigest nên bỏ sót tên và mô tả. Diff cho thấy test-audit đổi từ 'test-audit' thành 'Test Audit' và herdr-cook-plan đổi thứ tự tên. Lead yêu cầu assert riêng cho name, description, status, routing và danh sách resource (trừ .meta/*) cho cả ba skill.
**Bài học:** Test chỉ kiểm những gì bạn nghĩ tới; so sánh đầu ra thật của binary cũ với binary mới bắt được thứ test bỏ sót.
**Artefact:** Bảng hai cột trước/sau gồm name, description, status, che tên skill.
**Góc người ngoài:** cách làm phổ biến là Phần lớn người chỉ nhìn test xanh hoặc kiểm tra bằng mắt đầu ra; ở đây khác ở Diff trước/sau trên đầu ra thật bắt được những thay đổi mà test không kiểm tra (như description bị hỏng). Đây là cách kiểm tra có hệ thống khi refactor dữ liệu. cách làm phổ biến là Dev thường tự viết fixture đơn giản cho nhanh, rồi test xanh nhưng không khớp dữ liệu thật; ở đây khác ở Fixture thật bắt được lỗi (ví dụ block scalar, key 'repo', id thiếu) mà fixture viết tay bỏ sót. Đây là lý do fixture trước đó được lead yêu cầu thay.
