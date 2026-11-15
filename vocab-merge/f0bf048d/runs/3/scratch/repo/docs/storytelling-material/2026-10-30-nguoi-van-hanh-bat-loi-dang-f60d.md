---
id: 2026-10-30-nguoi-van-hanh-bat-loi-dang-f60d
code: M-KDVW
aliases: [M-KDVW]
date: 2026-10-30
repo: repo
status: raw
signals: [người duyệt máy, ràng buộc định hình thiết kế]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:f0bf048d#L920", "claude:f0bf048d#L923", "claude:f0bf048d#L968"]
hook: "Tôi bảo agent tự làm, rồi bắt gặp chính mình đang làm hộ"
tension: nguoi_dung_may_sai
sides: ["Người vận hành tự xử lý việc chuyên môn", "Agent mới là bên phải tự làm bằng công cụ đã gắn"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Người vận hành bắt lỗi: đang tự làm việc của agent thay vì đóng gói

**Bối cảnh:** Trong phiên, tôi đã tự tìm property ID, chẩn đoán lỗi www và làm việc chuyên môn thay agent.
**Chuyện gì xảy ra:** Người vận hành nói rõ: agent phải tự làm được bằng công cụ đã gắn, việc của tôi là đóng gói. Sau đó việc chuyên môn được chuyển sang issue giao cho agent, và việc đầu tiên là chính vụ Search Console, để xem agent có tự phát hiện lỗi không. Phạm vi được chia rõ: hạ tầng cho người, chuyên môn cho agent.
**Bài học:** Khi đang dựng công cụ mà thấy mình đang giải bài toán thay agent, dừng lại và hỏi: công cụ này đã đủ để agent tự làm chưa?
**Artefact:** Issue giao việc chỉ có mục tiêu, không kể lỗi (che tên).
**Góc người ngoài:** cách làm phổ biến là Dev thường bảo AI viết code rồi tự tay chạy thử, tự tra cứu ID, tự đối chiếu cấu hình; ở đây khác ở Agent tự đi kiểm tra từng bước cho đến khi có số liệu thật, rồi mới báo. Người đọc muốn biết cách ra lệnh để AI làm đến cùng như vậy, không phải chỉ viết code.
