---
id: 2026-10-21-may-kiem-374-vi-pham-khong-fd46
code: M-SWVC
aliases: [M-SWVC]
date: 2026-10-21
repo: repo
status: raw
signals: [nguyên nhân bất ngờ]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L95", "claude:9514b261#L262", "claude:9514b261#L282"]
hook: "374 vi phạm không chạy ở đâu, một lệnh ghi đè nuốt luôn vi phạm mới"
tension: giup_ma_hai
sides: ["Có máy kiểm và baseline để chặn vi phạm", "Chạy lại lệnh ghi đè baseline thì vi phạm mới thành đã biết, không ai báo"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Máy kiểm 374 vi phạm không chạy ở đâu, và --write-baseline ghi đè nuốt vi phạm mới

**Bối cảnh:** Hai script kiểm mã quyết định trong tên test và trích dẫn đều có cờ --write-baseline.
**Chuyện gì xảy ra:** check-decision-codes báo 374 vi phạm nhưng không nằm trong npm test, nên như không tồn tại. Cả hai script ghi đè baseline vô điều kiện. Ai chạy lại lệnh thì mọi vi phạm mới thành đã biết mà không báo. Pre-commit còn trỏ tới hai file không tồn tại. Kế hoạch đề xuất so với baseline cũ và chỉ cho tăng khi có cờ --allow-growth tường minh.
**Bài học:** Máy kiểm không nằm trong đường chạy thường xuyên thì coi như không có. Baseline chỉ được tăng khi có cờ rõ ràng.
**Artefact:** Sơ đồ ba cửa chạy máy kiểm: pre-commit, npm test, chạy tay.
