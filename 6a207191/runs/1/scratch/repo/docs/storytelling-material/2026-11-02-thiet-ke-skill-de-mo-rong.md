---
id: 2026-11-02-thiet-ke-skill-de-mo-rong
date: 2026-11-02
repo: repo
status: raw
signals: []
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [hotspot, outsider]
lines: ["claude:6a207191#L317", "claude:6a207191#L486", "claude:6a207191#L833", "claude:6a207191#L1044"]
hook: "Thêm ngôn ngữ mới cho skill chỉ cần copy một file mẫu"
tension: it_ma_nhieu
sides: ["Chỉ copy một file _template, không sửa file chính", "Skill tự liệt kê thư mục và chọn đúng file để đọc"]
strength: 2
stakes: 2
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Thiết kế skill để mở rộng không cần sửa file chính. SKILL.md không liệt kê file cố định, agent tự liệt kê thư mục và đọc frontmatter (applies_when, detect) để chọn file phù hợp. Thêm ngôn ngữ, kênh phân phối hay chủ đề chỉ cần copy một file _template.

**Chuyện gì xảy ra:** Thiết kế skill để mở rộng không cần sửa file chính. SKILL.md không liệt kê file cố định, agent tự liệt kê thư mục và đọc frontmatter (applies_when, detect) để chọn file phù hợp. Thêm ngôn ngữ, kênh phân phối hay chủ đề chỉ cần copy một file _template.
**Góc người ngoài:** cách làm phổ biến là Hầu hết skill hay prompt là một file dài hoặc một mục lục gõ tay, mỗi lần thêm nội dung lại phải sửa mục lục; ở đây khác ở Cấu trúc này cho phép kiến thức tăng dần qua nhiều dự án mà SKILL.md không phình ra. Người đọc muốn cách tổ chức skill theo kiểu plugin này, kèm quy tắc ID không bao giờ đánh lại số và CONTRIBUTING để agent khác tự bổ sung đúng chỗ.
