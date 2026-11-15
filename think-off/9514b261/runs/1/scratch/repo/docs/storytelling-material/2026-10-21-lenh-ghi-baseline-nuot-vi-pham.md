---
id: 2026-10-21-lenh-ghi-baseline-nuot-vi-pham
date: 2026-10-21
repo: repo
status: raw
signals: []
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L95", "claude:9514b261#L282", "claude:9514b261#L383"]
hook: "Máy báo 374 vi phạm nhưng không nối vào đâu, chạy lại baseline là xoá sạch"
tension: cam_ma_van_lot
sides: ["có máy kiểm và baseline để chặn vi phạm", "374 vi phạm không ai thấy, ghi đè baseline biến lỗi mới thành đã biết"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Lệnh ghi baseline nuốt vi phạm mới: 374 vi phạm không ai thấy vì máy kiểm không chạy

**Bối cảnh:** Repo có các máy kiểm ratchet chống mã quyết định lọt vào tên test và chống trích dẫn quyết định cũ.
**Chuyện gì xảy ra:** Hai script ghi baseline ghi đè vô điều kiện, nên chạy lại là mọi vi phạm mới thành đã biết. check-decision-codes báo 374 vi phạm nhưng không được nối vào đâu ngoài test của chính nó, nên như không có. Kế hoạch đề xuất chặn ghi đè và chỉ cho tăng baseline khi có cờ allow-growth tường minh.
**Bài học:** Máy kiểm chưa nối vào pipeline và lệnh ghi baseline không so với bản cũ là hai lỗ hổng cùng loại: vi phạm mới không có ai chặn.
**Artefact:** Bảng số 374 vi phạm và ghi chú không có chỗ chạy.
