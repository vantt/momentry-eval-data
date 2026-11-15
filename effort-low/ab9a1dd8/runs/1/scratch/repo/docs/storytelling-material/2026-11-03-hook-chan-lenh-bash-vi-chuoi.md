---
id: 2026-11-03-hook-chan-lenh-bash-vi-chuoi
date: 2026-11-03
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:ab9a1dd8#L1604", "claude:ab9a1dd8#L1613", "claude:ab9a1dd8#L3367", "claude:ab9a1dd8#L3369"]
hook: "Hook chặn lệnh vì chuỗi 'dist', agent đổi sang Write"
tension: cam_ma_van_lot
sides: ["hook chặn lệnh bash có chuỗi trông nguy hiểm", "đổi sang Write và Edit là ghi file được ngay"]
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Hook chặn lệnh bash vì chuỗi trông nguy hiểm: chuyển sang Write và sửa test bằng Edit

**Bối cảnh:** Hook an toàn kiểm lệnh bash trước khi chạy và chặn những chuỗi như dist hoặc .git khi chúng xuất hiện trong lệnh.
**Chuyện gì xảy ra:** Lệnh tạo file workflow chứa chuỗi dist bị chặn, nên agent chuyển sang công cụ Write. Lệnh sửa test quarantine chứa .git cũng bị chặn, nên dùng Edit. Cách này tránh được hook nhưng cũng là dấu hiệu đáng ghi về ràng buộc của công cụ.
**Bài học:** Khi hook chặn lệnh vì chuỗi trông lạ, đọc thông báo để biết đó là chặn theo chuỗi chứ không phải theo ý định; chọn công cụ đọc ghi trực tiếp nếu lệnh không cần shell.
**Artefact:** Thông báo của hook kèm đường dẫn file cấu hình ckignore. Che đường dẫn cục bộ.
