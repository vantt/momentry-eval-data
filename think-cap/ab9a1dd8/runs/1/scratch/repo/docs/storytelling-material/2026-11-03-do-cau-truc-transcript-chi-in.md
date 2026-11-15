---
id: 2026-11-03-do-cau-truc-transcript-chi-in
date: 2026-11-03
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [hotspot, harvest, outsider]
lines: ["claude:ab9a1dd8#L3501", "claude:ab9a1dd8#L3503", "claude:ab9a1dd8#L3507", "claude:ab9a1dd8#L3510", "claude:ab9a1dd8#L3520", "claude:ab9a1dd8#L3521"]
hook: "Dò cấu trúc transcript chỉ in khoá và kiểu, không in nội dung"
tension: none
sides: []
strength: 0
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Dò cấu trúc transcript chỉ in khoá và kiểu, không in giá trị

**Bối cảnh:** Trước khi viết bộ đọc cho pi, omp và agy, agent cần biết schema thật nhưng không được đưa nội dung hội thoại vào log.
**Chuyện gì xảy ra:** Lần đầu, script dò chạy trên Node 24 bị lỗi evalTypeScript. Agent dùng find với bộ lọc kích thước để chọn một transcript 400 dòng và chỉ in khoá và kiểu bản ghi.
**Bài học:** Dò schema chỉ in khoá và kiểu, không in giá trị. Chọn mẫu bằng find với bộ lọc kích thước thay vì glob mặc định.
**Artefact:** Bảng khoá và kiểu bản ghi, không có giá trị.
**Góc người ngoài:** cách làm phổ biến là Người ta hay in cả dòng log hoặc file ra màn hình để xem, và vô tình lộ nội dung riêng tư hoặc bí mật; ở đây khác ở Agent chỉ lấy hình dạng dữ liệu nên có thể làm việc với dữ liệu thật của user mà không rò rỉ nội dung. Người đọc sẽ muốn biết cách làm vậy.
