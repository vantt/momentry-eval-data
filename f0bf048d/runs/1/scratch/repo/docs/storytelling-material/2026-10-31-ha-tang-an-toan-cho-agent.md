---
id: 2026-10-31-ha-tang-an-toan-cho-agent
date: 2026-10-31
repo: repo
status: raw
signals: [ràng buộc định hình thiết kế, đảo quyết định có lý do, người duyệt thứ máy soạn]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:f0bf048d#L1794", "claude:f0bf048d#L1855", "claude:f0bf048d#L1867", "claude:f0bf048d#L1884", "claude:f0bf048d#L2284", "claude:f0bf048d#L2373", "claude:f0bf048d#L2578", "claude:f0bf048d#L3327", "claude:f0bf048d#L3340"]
hook: "Mã đăng nhập 6 ký tự trong .env mở được quyền chủ"
tension: nho_ma_to
sides: ["một mã dev chỉ 6 ký tự trong file .env", "đăng nhập được thành chủ, daemon có quyền ngang root"]
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
**Góc người ngoài:** cách làm phổ biến là Cấp key quyền rộng, dặn agent 'đừng làm gì tốn tiền' trong prompt, hoặc theo dõi hoá đơn sau; ở đây khác ở Cách 'không gắn billing account' biến câu hỏi 'agent có làm tốn tiền không' thành không thể xảy ra về mặt cơ chế. Dev làm một mình dễ áp dụng ngay cho mọi API key giao cho agent. cách làm phổ biến là Tự viết tài liệu thiết kế bảo mật rồi triển khai, hoặc để AI review rồi tin nguyên văn; ở đây khác ở Red-team bằng agent thứ hai rồi xác minh từng phát hiện bằng lệnh đọc thật (không tin cả hai bên) là quy trình rẻ, dev đơn lẻ làm được ngay. Một phát hiện hoá ra đã được sửa bởi commit khác, nên bước kiểm lại tránh báo động giả.
