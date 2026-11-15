---
id: 2026-11-03-doc-schema-transcript-that-ma-khong
date: 2026-11-03
repo: repo
status: raw
signals: [ràng buộc]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [hotspot, harvest, outsider]
lines: ["claude:ab9a1dd8#L3502", "claude:ab9a1dd8#L3503", "claude:ab9a1dd8#L3507", "claude:ab9a1dd8#L3510", "claude:ab9a1dd8#L3520", "claude:ab9a1dd8#L3528", "claude:ab9a1dd8#L3539"]
hook: "Đọc cấu trúc transcript thật mà không in nội dung nào"
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

# Đọc schema transcript thật mà không in nội dung

**Bối cảnh:** Các phiên pi, omp và agy chứa nội dung riêng tư. Cần schema để viết bộ đọc.
**Chuyện gì xảy ra:** Script shape chỉ in kiểu và tên khoá, không in giá trị. Lần đầu lỗi vì chạy file .ts bằng Node cũ (evalTypeScript), sau đó dùng find theo kích thước để chọn phiên. Tìm được năm transcript agy thật để kiểm bộ đọc, và một phiên omp dài 400 dòng.
**Bài học:** Khi phải nhìn dữ liệu riêng tư để viết parser, chỉ in cấu trúc là đủ để viết đúng.
**Artefact:** Output shape chỉ có khoá và kiểu, không có giá trị.
**Góc người ngoài:** cách làm phổ biến là Dev thường đọc tài liệu định dạng, hoặc `head` file mẫu rồi viết parser; dễ lộ nội dung riêng tư ra log và ra cuộc trò chuyện với AI; ở đây khác ở Vừa có schema đúng của dữ liệu thật (khác tài liệu) vừa không để nội dung riêng tư lọt vào ngữ cảnh của AI. Người dùng AI hằng ngày sẽ muốn mẫu thủ tục này khi để agent đụng vào dữ liệu cá nhân.
