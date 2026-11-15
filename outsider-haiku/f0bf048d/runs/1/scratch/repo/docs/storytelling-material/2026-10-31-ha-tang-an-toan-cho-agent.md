---
id: 2026-10-31-ha-tang-an-toan-cho-agent
date: 2026-10-31
repo: repo
status: raw
signals: [ràng buộc định hình thiết kế, đảo quyết định có lý do, người duyệt thứ máy soạn]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L1794", "claude:f0bf048d#L1855", "claude:f0bf048d#L1867", "claude:f0bf048d#L1884", "claude:f0bf048d#L2284", "claude:f0bf048d#L2373", "claude:f0bf048d#L2578", "claude:f0bf048d#L3327", "claude:f0bf048d#L3340"]
hook: "Bản thiết kế quyền có mã đăng nhập 6 ký tự cho phép vào làm chủ"
tension: cam_ma_van_lot
sides: ["thiết kế quyền để agent an toàn", "mã dev 6 ký tự trong .env đăng nhập thành chủ, daemon quyền như root"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Hạ tầng 'an toàn cho agent' bằng cơ chế, không bằng lời dặn

**Bối cảnh:** Máy chạy daemon Multica có agent đọc web và nội dung khách; cần quyết định agent được tự làm gì và bị chặn bằng gì.
**Chuyện gì xảy ra:** Bản thiết kế quyền đầu tiên được một agent độc lập phản biện và tìm ra: mã đăng nhập dev 6 ký tự trong .env cho phép đăng nhập thành chủ, daemon đặc quyền chạy dưới user có docker tương đương root, và không có backup. Giai đoạn 0 làm trong phiên: dừng daemon, tách PAT của chủ khỏi user daemon bằng cách tạo member riêng, và thay PAT cũ. Bot không có quyền chỉ đọc trên repo private cá nhân nên phương án (c) bị loại sau khi kiểm tài liệu GitHub; chọn hoãn. Lệnh sudo lần 2 báo lỗi vì file PAT đã bị xoá sau lần chạy thứ nhất.
**Bài học:** Mỗi quyền phải được chặn bằng cơ chế (uid, token, firewall), vì lời dặn trong instructions có thể bị prompt injection bỏ qua; kiểm tài liệu nền tảng trước khi chốt một phương án.
**Artefact:** Bảng lộ trình Giai đoạn 0–2 với cột trạng thái; che token, email, IP tailnet.
