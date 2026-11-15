---
id: 2026-10-21-374-vi-pham-nam-trong-may
date: 2026-10-21
repo: repo
status: raw
signals: [số trước sau, nguyên nhân bất ngờ]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L262", "claude:9514b261#L282", "claude:9514b261#L349", "claude:9514b261#L383"]
hook: "Máy kiểm báo 374 vi phạm, nhưng không ai thấy"
tension: cam_ma_van_lot
sides: ["Có máy kiểm bắt được 374 vi phạm", "Nó không nối vào npm test nên không ai thấy"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# 374 vi phạm nằm trong máy kiểm không chạy ở đâu

**Bối cảnh:** Repo có hai script kiểm mã quyết định trong tên test và trích dẫn. Cả hai đều có cờ --write-baseline ghi đè vô điều kiện.
**Chuyện gì xảy ra:** Script check-decision-codes báo 374 vi phạm nhưng không được nối vào npm test, nên không ai thấy. Cờ --write-baseline ghi đè baseline mà không so với bản cũ, nên mọi vi phạm mới bị nuốt. Kế hoạch 1A tách sáu việc thành ba loại: máy canh yếu hoặc tắt, chỉ dẫn agent đọc sai, và giới hạn byte không có máy kiểm.
**Bài học:** Máy kiểm chưa được nối vào đường chạy chung thì coi như chưa tồn tại. Cờ làm mới baseline phải so với bản cũ trước khi ghi.
**Artefact:** Bảng sáu việc chia ba loại, cột bằng chứng là đường dẫn file.
