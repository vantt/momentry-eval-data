---
id: 2026-11-02-seed-11-nam-trong-preset-cua-3c6e
code: M-AKS6
aliases: [M-AKS6]
date: 2026-11-02
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L103", "claude:2dfb5915#L474"]
hook: "Tài liệu ghi seed 11, agent vẫn đọc mã để chắc"
tension: none
sides: []
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Seed 11 nằm trong preset của fixture, test Python không truyền seed

**Bối cảnh:** Cần đặt seed cho fixture trong spec.lock để bản Rust dựng cùng vault.
**Chuyện gì xảy ra:** Test Python gọi generate không có --seed, nên giá trị thật lấy từ mặc định của preset, là 11. Tài liệu bench cũng ghi 11. Agent đọc mặc định trong mã thay vì tin vào tài liệu.
**Bài học:** Đọc giá trị mặc định trong mã, không chỉ tài liệu.
