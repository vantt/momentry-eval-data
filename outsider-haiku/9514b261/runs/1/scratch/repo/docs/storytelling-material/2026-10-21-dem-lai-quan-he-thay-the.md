---
id: 2026-10-21-dem-lai-quan-he-thay-the
date: 2026-10-21
repo: repo
status: raw
signals: [số trước sau, đảo quyết định]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [hotspot, harvest, outsider]
lines: ["claude:9514b261#L1121", "claude:9514b261#L1237"]
hook: "Tưởng quan hệ thay thế chưa có, đếm ra 18"
tension: tuong_ma_hoa_ra
sides: ["Giả định đề xuất chưa nhắc dữ liệu có sẵn", "Event log đã có 18 quan hệ supersedes"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đếm lại quan hệ thay thế: giả định 'chưa có' bị sửa

**Bối cảnh:** Đề xuất reducer giả định rằng quyết định mới thay quyết định cũ đều được ghi bằng một quan hệ có cấu trúc.
**Chuyện gì xảy ra:** Đếm trong event log: 36 quyết định, 18 quan hệ supersedes, nhưng chỉ 8 quyết định có trường relation. Trong 7 cặp nền tảng có quan hệ, 5 cặp chỉ thay một phần. Ít nhất 4 quyết định chỉ nêu việc thay thế trong câu chữ. Agent đính chính nhận định ban đầu rằng đề xuất không nhắc đến dữ liệu hiện có.
**Bài học:** Đếm trên dữ liệu trước khi kết luận 'có' hay 'không'. Một quan hệ chỉ viết trong văn bản thì không phải dữ liệu có cấu trúc.
**Artefact:** Bảng: loại quan hệ | số lượng.
**Góc người ngoài:** cách làm phổ biến là Chuyển nguyên kết quả của subagent cho người dùng, coi đó là sự thật đã kiểm; ở đây khác ở Mỗi con số trong báo cáo cuối có ít nhất một lần đối chiếu, và các chỗ không kiểm được được ghi là chưa kiểm. Người đọc muốn biết cách tránh lỗi lan truyền từ agent phụ sang báo cáo cuối.
