---
id: 2026-11-02-bo-so-khop-an-danh-chi
date: 2026-11-02
repo: repo
status: raw
signals: [ràng buộc, người duyệt]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:2dfb5915#L83", "claude:2dfb5915#L95", "claude:2dfb5915#L397"]
hook: "Bộ so khớp ẩn danh chỉ in số lệch, không in tên note"
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

# Bộ so khớp ẩn danh: chỉ in số lệch, không in tên note hay đường dẫn

**Bối cảnh:** Phase 02 và 05 phải chạy thêm trên vault riêng của user.
**Chuyện gì xảy ra:** Agent hỏi đường dẫn và quyền chạy script chỉ đọc, user giữ cổng này. Chế độ private chỉ in số lệch, không in tên note, đường dẫn hay tên vault. Trên bộ thử, 55 mục khớp ở chế độ này.
**Bài học:** Thiết kế báo cáo ẩn danh ngay từ đầu, đừng sửa sau.
**Artefact:** Mẫu báo cáo lệch đã che.
**Góc người ngoài:** cách làm phổ biến là Thường dán dữ liệu thật vào prompt hoặc cho agent chạy thẳng trên dữ liệu thật, hoặc bỏ qua bước kiểm trên dữ liệu thật; ở đây khác ở Đây là cách vẫn kiểm được trên dữ liệu thật mà không lộ nội dung riêng tư. Dev làm một mình muốn dùng AI trên dữ liệu nhạy cảm sẽ muốn mẫu này: kiểm tự động bằng số liệu, không bằng nội dung.
