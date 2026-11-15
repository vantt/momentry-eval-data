---
id: 2026-11-02-sua-go-sai-lam-roi-tu
date: 2026-11-02
repo: repo
status: raw
signals: [Nguyên nhân bất ngờ]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L1470"]
hook: "Bộ sửa gõ sai làm một câu tụt từ hạng 4 xuống hạng 7"
tension: giup_ma_hai
sides: ["sửa lỗi gõ cho người dùng", "từ gốc mất nên lớp đồng nghĩa không khớp"]
strength: 3
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Sửa gõ sai làm rơi từ đồng nghĩa: hạng 4 thành hạng 7

**Bối cảnh:** Bộ sửa gõ sai một ký tự chạy trước lớp từ điển đồng nghĩa.
**Chuyện gì xảy ra:** Sau khi gộp, bộ sửa gõ sai viết lại từ người dùng gõ thành một từ gần đúng trong vault, nên lớp đồng nghĩa không còn nhận được từ gốc. Một câu tụt từ hạng 4 xuống hạng 7, vi-synonym Hit@5 xuống 0,73. Sửa: lớp đồng nghĩa khớp cả câu gốc lẫn câu đã sửa, và từ đã có trong lexicon không bị sửa gõ sai.
**Bài học:** Hai lớp viết lại truy vấn phải biết thứ tự của nhau; lớp sau không được thấy dạng đã bị lớp trước đổi.
**Artefact:** Bảng hạng của câu trước và sau khi sửa.
