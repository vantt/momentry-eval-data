---
id: 2026-11-03-hook-ckignore-chan-lenh-bash-vi-d5ef
code: M-5S2R
aliases: [M-5S2R]
date: 2026-11-03
repo: repo
status: raw
signals: [khac]
signal_note: "Chuyện vặt, nhưng cho thấy ràng buộc công cụ quyết định cách làm việc."
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:ab9a1dd8#L1604", "claude:ab9a1dd8#L1613", "claude:ab9a1dd8#L3367", "claude:ab9a1dd8#L3369"]
hook: "Hook chặn lệnh vì chuỗi 'dist'; agent chỉ việc đổi công cụ"
tension: cam_ma_van_lot
sides: ["Hook chặn lệnh bash có chuỗi dist và .git", "Agent đổi sang Write và Edit, vẫn ghi được file"]
strength: 3
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Hook .ckignore chặn lệnh bash vì có chuỗi dist và .git; agent đổi sang công cụ ghi file

**Bối cảnh:** Cấu hình .ckignore chặn các lệnh bash có chuỗi nhạy cảm.
**Chuyện gì xảy ra:** Lệnh tạo workflow ci.yml có chuỗi dist bị chặn, agent chuyển sang công cụ Write. Sau đó lệnh sửa test có .git cũng bị chặn, agent dùng Edit.
**Bài học:** Chặn theo chuỗi thô làm lệch cách làm. Khi bị chặn, đổi sang công cụ đúng mục đích, không vòng qua bằng lệnh khác.
**Artefact:** Thông báo chặn có đường dẫn cấu hình (che đường dẫn).
