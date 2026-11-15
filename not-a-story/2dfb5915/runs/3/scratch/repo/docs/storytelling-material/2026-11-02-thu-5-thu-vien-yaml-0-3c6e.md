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
hook: "746 note đều 0 lệch, 25.000 note ngẫu nhiên mới lộ panic"
tension: tuong_ma_hoa_ra
sides: ["Cả 5 thư viện YAML đều 0 lệch trên 746 note thật", "Trên 25.000 note ngẫu nhiên, libyaml-safer panic 242 lần"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Thử 5 thư viện YAML: 0 lệch trên 746 note, nhưng 25.000 note sinh ngẫu nhiên lộ panic

**Bối cảnh:** Cần một thư viện đọc YAML frontmatter sao cho khớp PyYAML trong toàn bộ index.
**Chuyện gì xảy ra:** Trên bộ kg-solo 746 note, cả 5 thư viện đều 0 lệch nên không phân biệt được. Trên 58 ca biên, số lệch là 0, 1, 9, 35 và 36. Trên 25.000 note ngẫu nhiên, libyaml-safer panic 242 lần, saphyr-parser lệch 6.510, còn bản chọn unsafe-libyaml 0 lệch. Bốn dạng YAML làm bản Python crash cũng được phát hiện.
**Bài học:** Bộ mẫu thật thường không phân biệt được lựa chọn, phải có bộ ca biên và dữ liệu sinh ngẫu nhiên để thấy khác biệt.
**Artefact:** Bảng so sánh 5 thư viện theo ba nhóm mẫu (không có nội dung note).
**Góc người ngoài:** cách làm phổ biến là Viết test đơn vị theo ý mình, rồi tin rằng khớp với bản cũ; ở đây khác ở Mỗi phần được so byte-for-byte với bản Python trên cùng vault và các ca fuzz sinh ngẫu nhiên; lệch do thứ tự hệ điều hành hay lỗi YAML được tìm ra và ghi thành quyết định. Người đọc muốn biết vì sao cách này lộ ra lỗi mà test đơn vị bỏ sót.
