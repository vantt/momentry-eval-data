---
id: 2026-11-02-thu-5-thu-vien-yaml-libyaml-3c6e
code: M-C4KM
aliases: [M-C4KM]
date: 2026-11-02
repo: repo
status: raw
signals: [khac, dao_quyet_dinh]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L335", "claude:2dfb5915#L352"]
hook: "Thư viện YAML cũ khớp từng ca, bản an toàn hơn panic 242 note"
tension: giup_ma_hai
sides: ["libyaml-safer, bản được cho là an toàn hơn", "Panic trên 242 note, còn unsafe-libyaml lệch 0"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: none
spine_context: "Một công cụ giúp hỏi Claude Desktop về graph của vault Obsidian, đang viết lại lõi bằng Rust để thay bản Python cũ."
spine_context_lines: [profile]
spine_want: Phân tích frontmatter YAML giống hệt PyYAML để chỉ mục khớp với bản Python.
spine_want_lines: ["claude:2dfb5915#L335"]
spine_obstacle: Năm phương án thư viện YAML cho số note lệch khác nhau trên cùng bộ dữ liệu.
spine_obstacle_lines: ["claude:2dfb5915#L335"]
spine_action: "Thử 5 phương án trên 746 note kg-solo, 58 ca biên và 25.000 note sinh ngẫu nhiên, đối chiếu với hành vi của Python."
spine_action_lines: ["claude:2dfb5915#L335"]
spine_outcome: unsafe-libyaml lệch 0 note ở cả ba bộ; libyaml-safer panic 242 note khi khối | hoặc > nằm cuối frontmatter.
spine_outcome_lines: ["claude:2dfb5915#L335"]
completeness: 5
---

# Thử 5 thư viện YAML: libyaml cũ khớp Python đến từng ca, bản an toàn hơn lại panic trên 242 note

**Bối cảnh:** Note của người dùng có frontmatter YAML đủ kiểu, và phải phân tích giống hệt PyYAML để chỉ mục khớp với bản Python.
**Chuyện gì xảy ra:** Thử 5 phương án trên 746 note kg-solo, 58 ca biên và 25.000 note sinh ngẫu nhiên. unsafe-libyaml cho 0 lệch ở cả ba bộ; libyaml-safer panic 242 note khi khối | hoặc > nằm cuối frontmatter; serde_norway lệch 20.916 note. Chọn unsafe-libyaml kèm lớp tương thích PyYAML.
**Bài học:** Đừng chọn thư viện theo độ an toàn trên giấy; chạy một bộ fuzz so với hành vi thật của bản tham chiếu rồi mới quyết.
**Artefact:** Bảng 5 phương án với số lệch ở ba bộ thử. Không đưa nội dung note.
