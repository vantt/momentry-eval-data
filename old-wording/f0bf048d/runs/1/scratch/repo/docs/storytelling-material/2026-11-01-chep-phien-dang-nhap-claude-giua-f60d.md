---
id: 2026-11-01-chep-phien-dang-nhap-claude-giua-f60d
code: M-P1T2
aliases: [M-P1T2]
date: 2026-11-01
repo: repo
status: raw
signals: [rang_buoc_thiet_ke]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [hotspot, harvest, outsider]
lines: ["claude:f0bf048d#L3502", "claude:f0bf048d#L3505", "claude:f0bf048d#L3510", "claude:f0bf048d#L3516"]
hook: "Chép đăng nhập Claude sang user khác, hai bên đá nhau 401"
tension: giup_ma_hai
sides: ["Chép file credentials sang user khác, chạy ngay", "Token xoay vòng, hai user thay nhau làm token kia chết"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Chép phiên đăng nhập Claude giữa hai user Linux: token xoay vòng

**Bối cảnh:** User mới của System Operator cần đăng nhập Claude. Chủ hỏi tại sao phải login lại khi máy đã có Claude.
**Chuyện gì xảy ra:** Claude Code lưu phiên theo từng user Linux. Chép file credentials sang user khác thì chạy được lúc đầu, nhưng mỗi lần làm mới token thì token cũ bị thay. Hai user dùng chung một bản chép sẽ đá nhau và gây lỗi 401 giữa chừng cho agent nghiệp vụ. Về an toàn không thêm quyền, nhưng rủi ro là gián đoạn. Khuyến nghị: login riêng, khoảng một phút.
**Bài học:** Đừng chép token OAuth đang làm mới giữa các user. Mỗi user cần phiên riêng.
**Artefact:** Không có. Lệnh chép gốc chứa đường dẫn token nên không dán.
**Góc người ngoài:** cách làm phổ biến là Thường người dùng tự làm hết hoặc copy file credential sang máy khác, dễ hỏng vì token xoay vòng; ở đây khác ở Phiên này giải thích vì sao không chép token giữa hai user Linux và chọn đăng nhập riêng cho từng user. Người đọc cần biết lý do token làm mới làm hỏng bản sao.
