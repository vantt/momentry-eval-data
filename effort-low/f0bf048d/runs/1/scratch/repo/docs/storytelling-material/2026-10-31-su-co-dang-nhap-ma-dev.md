---
id: 2026-10-31-su-co-dang-nhap-ma-dev
date: 2026-10-31
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, số trước số sau]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L1966", "claude:f0bf048d#L1972", "claude:f0bf048d#L1975", "claude:f0bf048d#L2284"]
hook: "Lỗ đăng nhập nặng nhất đã tự biến mất nhờ một commit của phiên khác"
tension: cam_ma_van_lot
sides: ["Mã dev cố định cho máy nào trong mạng đăng nhập thành chủ", "Kiểm tra lại thì biến đã trống, vì commit song song đã xoá"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Sự cố đăng nhập: mã dev cố định và cách một commit dọn sạch

**Bối cảnh:** Biến MULTICA_DEV_VERIFICATION_CODE nằm trong .env, mã 6 ký tự, có thể đăng nhập thành chủ hệ thống.
**Chuyện gì xảy ra:** Phản biện xác định đây là lỗ nghiêm trọng nhất, cho phép bất kỳ máy trong tailnet đăng nhập thành chủ nếu biết email. Kiểm tra lại trên container thì biến đã trống, nhờ một commit của phiên song song xoá mã cố định và chuyển sang đăng nhập bằng mã email (5 lần thử, 1 mã/phút). Tài liệu ghi rủi ro dò mã còn lại là vài tháng.
**Bài học:** Trước khi tin một lỗ đã vá, kiểm trạng thái thật trong container đang chạy, không chỉ đọc commit.
**Artefact:** Bảng 'trước / sau' của biến cấu hình (độ dài, trạng thái); che mã và email.
