---
id: 2026-11-01-chu-tai-khoan-bi-dua-vao-f60d
code: M-40FX
aliases: [M-40FX]
date: 2026-11-01
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, đảo quyết định có lý do]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:f0bf048d#L2400", "claude:f0bf048d#L2412", "claude:f0bf048d#L2543", "claude:f0bf048d#L2549", "claude:f0bf048d#L2550", "claude:f0bf048d#L2578"]
hook: "Script login tự xoá PAT sau lần chạy đầu, lần hai hỏng"
tension: giup_ma_hai
sides: ["Xoá PAT sau khi dùng cho an toàn", "Lần chạy thứ hai báo lỗi, backup login cũ vô dụng"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Chủ tài khoản bị đưa vào daemon chạy agent: thay bằng user riêng, script xoá PAT sau lần chạy đầu

**Bối cảnh:** Daemon của agent nghiệp vụ đăng nhập bằng PAT của chủ nên agent có quyền của chủ.
**Chuyện gì xảy ra:** Script login đã chạy thành công lần đầu và xoá file PAT sau khi dùng; lần hai báo lỗi vì file không còn. Tìm thấy 3 chỗ chứa PAT trong home (hai config CLI và một file). Tạo PAT mới, cập nhật cả 3, kiểm PAT mới chạy được, rồi mới thu hồi PAT cũ (HTTP 204). Hệ quả: bản backup login cũ không còn dùng được để quay lại.
**Bài học:** Thu hồi credential cũ chỉ sau khi xác nhận credential mới dùng được; script tiêu thụ secret phải ghi rõ trạng thái để lần chạy sau biết đã làm xong.
**Artefact:** Bảng kiểm trước và sau: PAT cũ hết dùng, PAT mới dùng được (che token).
**Góc người ngoài:** cách làm phổ biến là Thu hồi token cũ ngay sau khi đổi, rủi ro gián đoạn cao; ở đây khác ở Người đọc hay bỏ qua thứ tự này, và muốn biết vì sao thứ tự này giữ hệ thống chạy liên tục.
