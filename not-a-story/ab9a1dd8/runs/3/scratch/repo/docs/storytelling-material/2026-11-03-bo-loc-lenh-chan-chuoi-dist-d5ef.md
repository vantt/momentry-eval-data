---
id: 2026-11-03-bo-loc-lenh-chan-chuoi-dist-d5ef
code: M-MBVN
aliases: [M-MBVN]
date: 2026-11-03
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:ab9a1dd8#L1388", "claude:ab9a1dd8#L1604", "claude:ab9a1dd8#L1613", "claude:ab9a1dd8#L3367"]
hook: "Bộ lọc chặn ba lệnh, agent đổi công cụ thay vì lách"
tension: cam_ma_van_lot
sides: ["Bộ lọc chặn chuỗi nguy hiểm như rm -rf với biến, dist, .git", "Agent làm tiếp việc đúng bằng Node, Write, Edit mà không lách bộ lọc"]
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Bộ lọc lệnh chặn chuỗi 'dist', 'rm -rf' với biến shell và '.git'; agent đổi công cụ thay vì lách

**Bối cảnh:** Claude Code có bộ lọc kiểm tra lệnh bash trước khi chạy.
**Chuyện gì xảy ra:** Lần 1: lệnh xoá với biến shell bị chặn vì có thể thành rm -rf /, dù biến có đường dẫn đúng. Agent chạy lại bằng Node. Lần 2: lệnh ghi file workflow bị chặn vì heredoc chứa chuỗi dist, agent chuyển sang công cụ Write. Lần 3: chỉnh test bị chặn vì lệnh có .git, agent sửa bằng Edit.
**Bài học:** Bộ lọc theo chuỗi khớp cả nội dung heredoc. Khi bị chặn, đổi sang công cụ ghi file có sẵn, đừng lách lệnh.
**Artefact:** Thông báo chặn có đường dẫn tới file cấu hình bộ lọc. Che HOME nếu có.
