---
id: 2026-10-09-loi-walkdir-bi-nuot-trong-migration-4257
code: M-8GZC
aliases: [M-8GZC]
date: 2026-10-09
repo: repo
status: raw
signals: []
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L3656", "omp:cd4449ab#L3960", "omp:cd4449ab#L3962", "omp:cd4449ab#L3978", "omp:cd4449ab#L3980", "omp:cd4449ab#L3989", "omp:cd4449ab#L3996", "omp:cd4449ab#L3999"]
hook: "Một dấu '_ =' nuốt lỗi, migration âm thầm thiếu dữ liệu"
tension: nho_ma_to
sides: ["một dòng bỏ qua lỗi bé xíu", "migration báo xong mà thiếu dữ liệu"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Lỗi WalkDir bị nuốt trong migration: lead bắt bằng grep '_ ='

**Bối cảnh:** Migration v4 duyệt thư mục insight để gom evidence. Lệnh WalkDir trả lỗi nhưng bị gán vào _.
**Chuyện gì xảy ra:** Lead grep '_ =' và thấy một chỗ trong v4.go. Lỗi duyệt bị bỏ qua, nghĩa là migration có thể preview thiếu dữ liệu mà không báo. Agent viết lại để trả lỗi kèm tên file, và thêm test với một file insight bị hỏng: preview phải fail và workspace không đổi. Test đầu tiên chạy đỏ và phải sửa tiếp.
**Bài học:** Trong migration, mọi lỗi đọc hoặc duyệt phải thành lỗi có tên file. Fail-closed tốt hơn bỏ qua.
**Artefact:** Đoạn code trước và sau khi sửa. Không cần ảnh.
