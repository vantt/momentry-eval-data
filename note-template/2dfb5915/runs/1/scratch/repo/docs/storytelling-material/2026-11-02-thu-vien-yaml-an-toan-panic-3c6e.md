---
id: 2026-11-02-thu-vien-yaml-an-toan-panic-3c6e
code: M-6TDH
aliases: [M-6TDH]
date: 2026-11-02
repo: repo
status: raw
signals: [dao_quyet_dinh]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L335", "claude:2dfb5915#L352"]
hook: "Thư viện 'an toàn' panic 242 lần, thư viện đã archive lệch 0"
tension: tuong_ma_hoa_ra
sides: ["Thư viện an toàn, còn được bảo trì", "Panic 242 lần, bản đã archive lại khớp hoàn toàn"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án là công cụ Obsidian viết lại bằng Rust, và mục tiêu là kết quả phải khớp bản Python trên cùng vault. Người làm tưởng một thư viện YAML 'an toàn' và còn được bảo trì là lựa chọn hiển nhiên, nhưng nó panic 242 lần trên 25.000 note. Thư viện đã archive unsafe-libyaml lại khớp PyYAML hoàn toàn, nên dev viết lại công cụ parse cần chọn theo thứ đối chiếu chứ không theo tiêu chí chung."
audience: dev viết lại công cụ parse file cho khớp bản gốc
spine_context: "Công cụ dòng lệnh cho vault Obsidian, viết lại bằng Rust để kết quả khớp với bản Python trên cùng một vault."
spine_context_lines: [profile, "claude:2dfb5915#L11"]
spine_want: Kết quả parse frontmatter phải khớp PyYAML trên cùng vault.
spine_want_lines: ["claude:2dfb5915#L11"]
spine_obstacle: "Chọn thư viện YAML nào cho Rust, khi thư viện 'an toàn' và còn bảo trì panic trên nhiều note."
spine_obstacle_lines: ["claude:2dfb5915#L335"]
spine_turn: "Tưởng thư viện 'an toàn', còn bảo trì là lựa chọn đúng; hoá ra thư viện đã archive (unsafe-libyaml) khớp PyYAML hoàn toàn, còn libyaml-safer panic 242 lần trên 25.000 note."
spine_turn_lines: ["claude:2dfb5915#L335"]
spine_action: "Chọn unsafe-libyaml 0.2.11 chỉ để parse, cộng một lớp tương thích PyYAML của riêng mình; merge và push."
spine_action_lines: ["claude:2dfb5915#L352"]
spine_outcome: "Trên 25.000 note sinh ngẫu nhiên, unsafe-libyaml cùng lớp tương thích lệch 0; libyaml-safer panic 242 lần; saphyr lệch 6.510."
spine_outcome_lines: ["claude:2dfb5915#L335"]
spine_takeaway: "Chọn thư viện theo thứ đang đối chiếu, không theo 'an toàn' chung chung; đo trên dữ liệu thật trước khi quyết."
spine_takeaway_lines: ["claude:2dfb5915#L335"]
completeness: 7
---

# Thư viện YAML 'an toàn' panic trên 242 note, thư viện đã archive lại khớp 0 lệch

**Góc kể:** Dự án là công cụ Obsidian viết lại bằng Rust, và mục tiêu là kết quả phải khớp bản Python trên cùng vault. Người làm tưởng một thư viện YAML 'an toàn' và còn được bảo trì là lựa chọn hiển nhiên, nhưng nó panic 242 lần trên 25.000 note. Thư viện đã archive unsafe-libyaml lại khớp PyYAML hoàn toàn, nên dev viết lại công cụ parse cần chọn theo thứ đối chiếu chứ không theo tiêu chí chung.
**Bối cảnh:** Chọn thư viện parse YAML cho frontmatter, phải khớp PyYAML.
**Chuyện gì xảy ra:** Trên 25.000 note sinh ngẫu nhiên, libyaml-safer panic 242 lần, saphyr lệch 6.510 note, còn unsafe-libyaml lệch 0 trên cả 58 ca biên lẫn 25.000 note. Chọn unsafe-libyaml dù đã archive, vì nó là cùng libyaml 0.2.5 với PyYAML.
**Bài học:** Chọn thư viện theo tiêu chí khớp với thứ đang đối chiếu, không theo 'an toàn' chung chung.
