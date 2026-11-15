---
id: 2026-11-03-dong-goi-tai-tao-duoc-hai
date: 2026-11-03
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L1377", "claude:ab9a1dd8#L1380", "claude:ab9a1dd8#L1384"]
hook: "Đóng gói hai lần ra cùng một sha256, sửa archive thì installer từ chối"
tension: none
sides: []
strength: 0
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đóng gói tái tạo được: hai lần cho cùng sha256

**Bối cảnh:** Installer kiểm sha256 của archive. Archive tự viết theo định dạng ustar, không dựa vào tar của hệ thống.
**Chuyện gì xảy ra:** Đóng gói hai lần cho cùng một checksum, và cài lại không đổi gì. Installer kiểm được archive khi bị sửa và từ chối cài.
**Bài học:** Archive phải tái tạo được để checksum có nghĩa. Tự viết ustar giúp không phụ thuộc tar của hệ thống.
**Artefact:** Dòng checksum của hai lần đóng gói.
