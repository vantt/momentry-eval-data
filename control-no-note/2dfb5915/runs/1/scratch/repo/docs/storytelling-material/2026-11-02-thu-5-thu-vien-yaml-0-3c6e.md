---
id: 2026-11-02-thu-5-thu-vien-yaml-0-3c6e
code: M-BA44
aliases: [M-BA44]
date: 2026-11-02
repo: repo
status: raw
signals: [khac, dao_quyet_dinh]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:2dfb5915#L335", "claude:2dfb5915#L352"]
hook: "5 thư viện đều 0 lệch trên 746 note, 25.000 note ngẫu nhiên mới lộ panic"
tension: tuong_ma_hoa_ra
sides: ["Cả 5 thư viện 0 lệch trên dữ liệu thật", "25.000 note ngẫu nhiên: panic 242 lần, lệch 6.510"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một công cụ dòng lệnh hỏi Claude Desktop về graph vault Obsidian đang thay phần lõi Python bằng Rust, và phải chọn thư viện đọc YAML frontmatter khớp với PyYAML. Trên 746 note thật, cả năm thư viện đều cho 0 lệch nên trông như chọn cái nào cũng được. Khi thêm 58 ca biên và 25.000 note sinh ngẫu nhiên, libyaml-safer panic 242 lần, saphyr-parser lệch 6.510 chỗ, còn unsafe-libyaml không lệch. Ai chọn thư viện chỉ bằng bộ mẫu thật có thể chọn sai mà không biết."
audience: dev viết test hoặc port code cần khớp với bản cũ
spine_context: "Một công cụ dòng lệnh hỏi Claude Desktop về graph của vault Obsidian, đang thay phần lõi Python bằng Rust. Mục tiêu hiện tại là hoàn tất plan port lõi sang Rust."
spine_context_lines: [profile, "claude:2dfb5915#L11"]
spine_want: Chọn thư viện đọc YAML frontmatter sao cho kết quả khớp PyYAML trên toàn bộ index.
spine_want_lines: ["claude:2dfb5915#L11"]
spine_obstacle: "Bộ mẫu thật 746 note không phân biệt được các thư viện, vì chỉ có chuỗi, số nguyên và list."
spine_obstacle_lines: ["claude:2dfb5915#L335"]
spine_turn: Tưởng năm thư viện ngang nhau vì cả năm cho 0 lệch trên 746 note thật; hoá ra chỉ bộ ca biên và 25.000 note sinh ngẫu nhiên mới lộ khác biệt.
spine_turn_lines: ["claude:2dfb5915#L335"]
spine_action: "Thử năm thư viện trên ba nhóm mẫu: 746 note thật, 58 ca biên và 25.000 note ngẫu nhiên."
spine_action_lines: ["claude:2dfb5915#L335", "claude:2dfb5915#L352"]
spine_outcome: Chọn unsafe-libyaml 0.2.11 kèm lớp tương thích PyYAML cho Q3; đã merge và push.
spine_outcome_lines: ["claude:2dfb5915#L352"]
spine_takeaway: Mẫu thật có thể cho 0 lệch mà vẫn không chứng minh hai bên giống nhau; cần thêm ca biên và dữ liệu sinh ngẫu nhiên.
spine_takeaway_lines: ["claude:2dfb5915#L335"]
completeness: 7
---

# Thử 5 thư viện YAML: 0 lệch trên 746 note, nhưng 25.000 note sinh ngẫu nhiên lộ panic

**Góc kể:** Một công cụ dòng lệnh hỏi Claude Desktop về graph vault Obsidian đang thay phần lõi Python bằng Rust, và phải chọn thư viện đọc YAML frontmatter khớp với PyYAML. Trên 746 note thật, cả năm thư viện đều cho 0 lệch nên trông như chọn cái nào cũng được. Khi thêm 58 ca biên và 25.000 note sinh ngẫu nhiên, libyaml-safer panic 242 lần, saphyr-parser lệch 6.510 chỗ, còn unsafe-libyaml không lệch. Ai chọn thư viện chỉ bằng bộ mẫu thật có thể chọn sai mà không biết.
**Bối cảnh:** Cần một thư viện đọc YAML frontmatter sao cho khớp PyYAML trong toàn bộ index.
**Chuyện gì xảy ra:** Trên bộ kg-solo 746 note, cả 5 thư viện đều 0 lệch nên không phân biệt được. Trên 58 ca biên, số lệch là 0, 1, 9, 35 và 36. Trên 25.000 note ngẫu nhiên, libyaml-safer panic 242 lần, saphyr-parser lệch 6.510, còn bản chọn unsafe-libyaml 0 lệch. Bốn dạng YAML làm bản Python crash cũng được phát hiện.
**Bài học:** Bộ mẫu thật thường không phân biệt được lựa chọn, phải có bộ ca biên và dữ liệu sinh ngẫu nhiên để thấy khác biệt.
**Artefact:** Bảng so sánh 5 thư viện theo ba nhóm mẫu (không có nội dung note).
**Góc người ngoài:** cách làm phổ biến là Viết test đơn vị theo ý mình, rồi tin rằng khớp với bản cũ; ở đây khác ở Mỗi phần được so byte-for-byte với bản Python trên cùng vault và các ca fuzz sinh ngẫu nhiên; lệch do thứ tự hệ điều hành hay lỗi YAML được tìm ra và ghi thành quyết định. Người đọc muốn biết vì sao cách này lộ ra lỗi mà test đơn vị bỏ sót.
