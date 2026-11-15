---
id: 2026-10-21-may-kiem-ghi-de-baseline-va
date: 2026-10-21
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, số trước/sau]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L262", "claude:9514b261#L282", "claude:9514b261#L349", "claude:9514b261#L383"]
hook: "Máy kiểm báo 374 vi phạm nhưng không ai thấy, vì không chạy trong npm test"
tension: cam_ma_van_lot
sides: ["Có máy kiểm quyết định và baseline để chặn vi phạm", "Baseline bị ghi đè vô điều kiện, 374 vi phạm không ai chạy tới"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Máy kiểm ghi đè baseline và không chạy ở đâu: 374 vi phạm bị giấu

**Bối cảnh:** Repo có nhiều máy kiểm nằm trong scripts/ và .githooks/ để giữ luật. Agent đọc từng script để lập kế hoạch sửa luật quản lý.
**Chuyện gì xảy ra:** Hai script kiểm quyết định đều ghi đè baseline vô điều kiện, nên chạy lại lệnh ghi baseline là mọi vi phạm mới thành “đã biết”. Script kiểm mã quyết định báo 374 vi phạm nhưng không được gọi từ npm test, nên không ai thấy. Đối chiếu với bản đồ kiến trúc thì ba máy kiểm này không có hàng chủ nào.
**Bài học:** Một máy kiểm không nằm trong lệnh test hoặc CI thì coi như không tồn tại, và lệnh “ghi lại baseline” phải từ chối khi số vi phạm tăng.
**Artefact:** Bảng ba máy kiểm với các cột: nó canh gì, chạy khi nào, ai quản. Ô “chạy khi nào” của máy thứ hai ghi “không chạy ở đâu”.
