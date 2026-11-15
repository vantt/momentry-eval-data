---
id: 2026-11-03-plan-8-phase-45-viec-qua-d5ef
code: M-QF1K
aliases: [M-QF1K]
date: 2026-11-03
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L558", "claude:ab9a1dd8#L561", "claude:ab9a1dd8#L565", "claude:ab9a1dd8#L569"]
hook: "Validator cho qua plan 8 phase, nhưng đếm được 0 việc"
tension: tuong_ma_hoa_ra
sides: ["Validator qua, tưởng plan đã chuẩn", "Việc viết dạng đánh số nên đếm checkbox ra 0; sửa xong có 45 việc"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Plan 8 phase, 45 việc qua validator: bước đánh số không được tính là checkbox

**Bối cảnh:** Plan dựng bằng 'ak plan create' và 'ak plan add-phase', sau đó viết nội dung từng phase.
**Chuyện gì xảy ra:** 'ak plan validate' qua ngay với 8 phase. Phần Tasks viết dạng đánh số nên lệnh đếm checkbox thấy 0 việc. Agent dùng awk đổi số thành '- [ ]' và có 45 việc, ước khoảng 9 ngày công.
**Bài học:** Validator xanh không có nghĩa checklist đếm được. Kiểm số việc bằng đúng lệnh mà tool dùng để theo dõi tiến độ.
**Artefact:** Kết quả đếm checkbox theo phase trước và sau khi sửa.
