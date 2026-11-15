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
hook: "5 thư viện YAML đều 0 lệch trên 746 note, 25.000 note ngẫu nhiên thì lộ 242 panic"
tension: tuong_ma_hoa_ra
sides: ["Cả 5 thư viện đều 0 lệch trên 746 note thật", "25.000 note ngẫu nhiên: một bản panic 242 lần, một bản lệch 6.510"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án là một công cụ dòng lệnh để hỏi Claude Desktop về graph của vault Obsidian, và người làm đang port lõi sang Rust. Ban đầu cả 5 thư viện YAML đều không lệch note nào trên 746 note thật, nên dễ tưởng bộ mẫu đó đủ để chọn. Nhưng trên 25.000 note sinh ngẫu nhiên, một thư viện panic 242 lần và một thư viện lệch 6.510 note, còn bản được chọn lệch 0. Ai port parser sang ngôn ngữ khác nên thử ca biên và dữ liệu ngẫu nhiên, vì bộ mẫu thật có thể không phân biệt được các lựa chọn."
audience: dev viết parser hoặc port thư viện sang ngôn ngữ khác
spine_context: "Một công cụ dòng lệnh để hỏi Claude Desktop về graph của vault Obsidian, đang port lõi sang Rust để thay bản Python."
spine_context_lines: [profile, "claude:2dfb5915#L11"]
spine_want: "Hoàn tất phần port lõi sang Rust theo plan, với bộ đọc YAML khớp bản Python."
spine_want_lines: ["claude:2dfb5915#L11", "claude:2dfb5915#L335"]
spine_obstacle: Bộ 746 note thật không phân biệt được 5 thư viện YAML.
spine_obstacle_lines: ["claude:2dfb5915#L335"]
spine_turn: "Tưởng bộ note thật đủ để chọn thư viện; hoá ra cả 5 đều 0 lệch, và chỉ ca biên với dữ liệu ngẫu nhiên mới lộ khác biệt: một bản panic 242 lần, một bản lệch 6.510 note."
spine_turn_lines: ["claude:2dfb5915#L335"]
spine_action: "Chạy probe so 5 thư viện với bản Python trên vault thật, 58 ca biên và 25.000 note ngẫu nhiên."
spine_action_lines: ["claude:2dfb5915#L335"]
spine_outcome: "Chọn unsafe-libyaml cộng lớp tương thích PyYAML, lệch 0 trên cả ba bộ mẫu."
spine_outcome_lines: ["claude:2dfb5915#L335", "claude:2dfb5915#L352"]
spine_takeaway: Bộ mẫu thật có thể không phân biệt được lựa chọn; cần ca biên và dữ liệu sinh ngẫu nhiên.
spine_takeaway_lines: ["claude:2dfb5915#L335"]
completeness: 7
---

# Thử 5 thư viện YAML: 0 lệch trên 746 note, nhưng 25.000 note sinh ngẫu nhiên lộ panic

**Góc kể:** Dự án là một công cụ dòng lệnh để hỏi Claude Desktop về graph của vault Obsidian, và người làm đang port lõi sang Rust. Ban đầu cả 5 thư viện YAML đều không lệch note nào trên 746 note thật, nên dễ tưởng bộ mẫu đó đủ để chọn. Nhưng trên 25.000 note sinh ngẫu nhiên, một thư viện panic 242 lần và một thư viện lệch 6.510 note, còn bản được chọn lệch 0. Ai port parser sang ngôn ngữ khác nên thử ca biên và dữ liệu ngẫu nhiên, vì bộ mẫu thật có thể không phân biệt được các lựa chọn.
**Bối cảnh:** Cần một thư viện đọc YAML frontmatter sao cho khớp PyYAML trong toàn bộ index.
**Chuyện gì xảy ra:** Trên bộ kg-solo 746 note, cả 5 thư viện đều 0 lệch nên không phân biệt được. Trên 58 ca biên, số lệch là 0, 1, 9, 35 và 36. Trên 25.000 note ngẫu nhiên, libyaml-safer panic 242 lần, saphyr-parser lệch 6.510, còn bản chọn unsafe-libyaml 0 lệch. Bốn dạng YAML làm bản Python crash cũng được phát hiện.
**Bài học:** Bộ mẫu thật thường không phân biệt được lựa chọn, phải có bộ ca biên và dữ liệu sinh ngẫu nhiên để thấy khác biệt.
**Artefact:** Bảng so sánh 5 thư viện theo ba nhóm mẫu (không có nội dung note).
**Góc người ngoài:** cách làm phổ biến là Viết test đơn vị theo ý mình, rồi tin rằng khớp với bản cũ; ở đây khác ở Mỗi phần được so byte-for-byte với bản Python trên cùng vault và các ca fuzz sinh ngẫu nhiên; lệch do thứ tự hệ điều hành hay lỗi YAML được tìm ra và ghi thành quyết định. Người đọc muốn biết vì sao cách này lộ ra lỗi mà test đơn vị bỏ sót.
