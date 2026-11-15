---
id: 2026-11-03-bo-loc-lenh-chan-chuoi-dist-d5ef
code: M-MBVN
aliases: [M-MBVN]
date: 2026-11-03
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:ab9a1dd8#L1604", "claude:ab9a1dd8#L1613", "claude:ab9a1dd8#L3367"]
hook: "Lệnh bị chặn vì chứa chữ 'dist' và '.git', agent đổi cách làm"
tension: cam_ma_van_lot
sides: ["Bộ lọc chặn lệnh theo chuỗi ký tự", "Lệnh vô hại vẫn bị chặn, agent vòng sang công cụ Write"]
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Bộ lọc lệnh chặn chuỗi 'dist' và '.git' trong Bash

**Bối cảnh:** Bộ lọc của dự án chặn một số chuỗi trong lệnh Bash, gồm 'dist' và '.git'.
**Chuyện gì xảy ra:** Lệnh tạo workflow CI bị chặn vì chứa 'dist', nên agent chuyển sang công cụ Write. Lệnh thêm test quarantine cũng bị chặn vì chứa '.git'. Agent đổi cách làm thay vì sửa bộ lọc.
**Bài học:** Khi bộ lọc chặn chuỗi an toàn, hãy đổi công cụ chứ không sửa bộ lọc. Ghi lại để người duyệt biết.
**Artefact:** Thông báo chặn của bộ lọc. Không cần che.
