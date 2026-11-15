---
id: 2026-11-02-mcp-install-ghi-duong-dan-exe
date: 2026-11-02
repo: repo
status: raw
signals: [ràng buộc định hình thiết kế]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:2dfb5915#L1063", "claude:2dfb5915#L3286"]
hook: "Chạy từ thư mục Downloads, config AI trỏ vào đúng chỗ đó"
tension: nho_ma_to
sides: ["Chạy file từ Downloads", "Config trỏ vĩnh viễn vào thư mục tạm"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# mcp install ghi đường dẫn exe đang chạy, nên cần cờ riêng cho vị trí lạ

**Bối cảnh:** mcp install ghi đường dẫn file exe đang chạy vào config của Claude Desktop.
**Chuyện gì xảy ra:** Nếu user chạy từ thư mục Downloads, config trỏ vào đó. Sửa: cảnh báo và yêu cầu cờ --allow-any-location để vượt. Cờ --force chỉ bỏ qua kiểm tra Claude Desktop đang chạy. Tách hai cờ để một cờ không tắt cả hai bảo vệ.
**Bài học:** Mỗi lớp bảo vệ nên có cờ riêng, không gộp chung.
**Artefact:** Không có.
**Góc người ngoài:** cách làm phổ biến là Hầu hết trình cài đặt ghi đè file cấu hình bằng cách sao chép cứng, không sao lưu hoặc không giữ mục của người dùng; ở đây khác ở Phiên này kiểm JSON trước khi ghi, sao lưu có dấu thời gian, ghi qua file tạm, giữ CRLF và tiếng Việt, và chỉ đổi mục do mình tạo. Người đọc sẽ muốn biết cách làm này và cách kiểm tra nó.
