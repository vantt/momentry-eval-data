---
id: 2026-11-02-alias-bomb-yaml-lam-tran-bo
date: 2026-11-02
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, người duyệt thứ máy soạn]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L819", "claude:2dfb5915#L1000", "claude:2dfb5915#L1011"]
hook: "Một note 338 byte ngốn 1,45 GB RAM, tầng thứ 8 cần 14 GB"
tension: nho_ma_to
sides: ["Note chỉ 338 byte, 7 tầng alias", "11,1 triệu props, 1,45 GB RAM, tầng 8 cần 14 GB"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Alias bomb YAML làm tràn bộ nhớ, reviewer agent phát hiện trước khi chạy thật

**Bối cảnh:** Code YAML Rust khớp Python trên kg-solo, nhưng reviewer agent đọc code và viết test độc hại.
**Chuyện gì xảy ra:** Note 338 byte với 7 tầng alias tạo 11,1 triệu props và 1,45 GB RSS trong Rust; tầng thứ 8 cần khoảng 14 GB. Python cũng bị như vậy nên khớp đặc tả, nhưng vẫn là lỗ hổng từ chối dịch vụ. Sửa bằng ngân sách 1 triệu props và 64 MiB mỗi note.
**Bài học:** Khớp hành vi với bản gốc không có nghĩa là an toàn; reviewer phải thử đầu vào độc hại.
**Artefact:** Bảng số byte đầu vào và RSS theo tầng alias.
