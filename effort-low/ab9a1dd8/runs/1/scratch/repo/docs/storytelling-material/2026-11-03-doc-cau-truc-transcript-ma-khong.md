---
id: 2026-11-03-doc-cau-truc-transcript-ma-khong
date: 2026-11-03
repo: repo
status: raw
signals: [ràng buộc định hình thiết kế]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [hotspot, harvest, outsider]
lines: ["claude:ab9a1dd8#L3502", "claude:ab9a1dd8#L3507", "claude:ab9a1dd8#L3510", "claude:ab9a1dd8#L3520", "claude:ab9a1dd8#L3521", "claude:ab9a1dd8#L3528", "claude:ab9a1dd8#L3529"]
hook: "Đọc cấu trúc transcript chỉ bằng tên khoá, không in nội dung"
tension: none
sides: []
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đọc cấu trúc transcript mà không in nội dung

**Bối cảnh:** Transcript của agy và omp chứa nội dung phiên có thể nhạy cảm. Agent cần biết cấu trúc để viết bộ đọc nhưng không được lộ giá trị.
**Chuyện gì xảy ra:** Agent viết một script chỉ in kiểu và tên khoá của mỗi bản ghi JSONL, không in giá trị. Lần chạy đầu dùng TypeScript trên Node 24 nên lỗi, chuyển sang script JS và tìm file bằng find. Kết quả: omp có 400 dòng trong một phiên, agy có các file transcript_full.jsonl trong thư mục logs.
**Bài học:** Khi đọc dữ liệu nhạy cảm để học cấu trúc, chỉ in khoá và kiểu; viết công cụ đọc dữ liệu trước khi viết parser.
**Artefact:** Mẫu output của script shape: chỉ tên khoá và kiểu, không có giá trị. Đây là chỗ đáng chụp nhất.
**Góc người ngoài:** cách làm phổ biến là Thường người ta mở file mẫu xem nội dung thật, hoặc đoán schema từ tài liệu, và có thể lộ dữ liệu riêng tư; ở đây khác ở Agent có cách kiểm cấu trúc mà không lộ nội dung, nên vừa đúng schema vừa an toàn riêng tư; người đọc sẽ muốn bắt chước cách này khi làm việc với dữ liệu nhạy cảm.
