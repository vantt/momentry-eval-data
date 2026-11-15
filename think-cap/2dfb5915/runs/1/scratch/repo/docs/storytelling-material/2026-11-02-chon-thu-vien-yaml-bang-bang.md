---
id: 2026-11-02-chon-thu-vien-yaml-bang-bang
date: 2026-11-02
repo: repo
status: raw
signals: [số trước sau, đảo quyết định]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L335", "claude:2dfb5915#L352"]
hook: "Thư viện YAML an toàn nhất lại panic trên 242 note thật"
tension: tuong_ma_hoa_ra
sides: ["Tên thư viện nghe an toàn, viết bằng Rust", "Panic trên 242 note khi block ở cuối"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Chọn thư viện YAML bằng bảng lệch trên 25.000 note sinh ngẫu nhiên

**Bối cảnh:** Cần đọc frontmatter YAML khớp PyYAML. Vault mẫu không có YAML rủi ro nên không phân biệt được các crate.
**Chuyện gì xảy ra:** Năm ứng viên được đo: unsafe-libyaml 0 lệch; libyaml-safer panic trên 242 note; saphyr-parser 6.510 lệch; serde_norway 20.916; saphyr 21.317. libyaml-safer panic khi khối block nằm cuối frontmatter, một dạng khá phổ biến. Chọn unsafe-libyaml cộng lớp tương thích PyYAML.
**Bài học:** Khi mẫu thật không phân biệt được ứng viên, sinh dữ liệu xấu có kiểm soát rồi đo lệch.
**Artefact:** Bảng 5 hàng, cột là mẫu chuẩn, ca biên, ngẫu nhiên. Không chụp note.
