---
id: 2026-10-21-may-kiem-da-viet-xong-nhung-fd46
code: M-R945
aliases: [M-R945]
date: 2026-10-21
repo: repo
status: raw
signals: [khac, nguyen_nhan_bat_ngo]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L233", "claude:9514b261#L262", "claude:9514b261#L282", "claude:9514b261#L349", "claude:9514b261#L383"]
hook: "Máy kiểm báo 374 vi phạm nhưng không chạy trong npm test"
tension: cam_ma_van_lot
sides: ["Có máy kiểm và có baseline, tưởng vi phạm mới sẽ bị bắt", "Máy kiểm không chạy ở đâu, lệnh baseline ghi đè nuốt vi phạm mới"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Máy kiểm đã viết xong nhưng không chạy ở đâu: 374 vi phạm và một lệnh ghi đè nuốt vi phạm mới

**Bối cảnh:** Repo có nhiều máy kiểm quyết định, nhưng agent phát hiện chúng chưa được nối vào đường chạy nào. Agent đang lập kế hoạch nhóm sửa luật 1A.
**Chuyện gì xảy ra:** check-decision-codes báo 374 vi phạm (tên test nhúng mã quyết định) nhưng chỉ chạy trong test của chính nó, không chạy trong npm test. Cả hai script baseline đều ghi đè vô điều kiện, nên chạy lại lệnh là mọi vi phạm mới thành 'đã biết' mà không ai hay. Agent cũng thấy hai đường dẫn chết trong thông báo của pre-commit. Kế hoạch chia 6 việc: phase 1 đến 4 làm ngay, phase 5 đến 6 chờ xác nhận manifest.
**Bài học:** Một máy kiểm không được nối vào đường chạy thì coi như không có; hãy kiểm xem nó thật sự chạy ở đâu trước khi tin nó.
**Artefact:** Bảng ba máy kiểm gồm tên, thứ nó canh và thời điểm chạy. Không cần ảnh.
