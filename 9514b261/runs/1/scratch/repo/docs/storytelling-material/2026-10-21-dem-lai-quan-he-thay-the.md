---
id: 2026-10-21-dem-lai-quan-he-thay-the
date: 2026-10-21
repo: repo
status: raw
signals: [số trước sau, đảo quyết định]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:9514b261#L1121", "claude:9514b261#L1237"]
hook: "36 quyết định, 18 quan hệ thay thế, chỉ 8 được ghi"
tension: tuong_ma_hoa_ra
sides: ["tưởng dữ liệu thay thế chưa hề có", "nó có sẵn, nhưng nằm trong câu chữ thay vì trường dữ liệu"]
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
