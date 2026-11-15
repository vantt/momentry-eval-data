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
hook: "374 vi phạm không chạy ở đâu, một lệnh còn nuốt vi phạm mới"
tension: cam_ma_van_lot
sides: ["Đã viết máy kiểm, tưởng vi phạm sẽ bị chặn", "Máy kiểm không nằm trong npm test, chạy lại baseline biến vi phạm mới thành đã biết"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án Forgent là nền tảng để xây app agent, và người làm đang gom các luật rải rác để agent không dùng lẫn luật cũ. Agent tin máy kiểm mã quyết định đang chặn vi phạm mới, nhưng nó không chạy trong npm test nào, và lệnh ghi baseline còn ghi đè vô điều kiện. Dev làm công cụ có quy tắc cho agent nên quan tâm, vì một máy kiểm không nối vào đường chạy thì không bảo vệ được gì."
audience: dev làm công cụ có quy tắc hoặc luật cho agent
spine_context: "Dự án Forgent, nền tảng để xây và chạy app agent. Người làm đang gom các luật rải rác để agent không dùng lẫn luật cũ."
spine_context_lines: [profile, "claude:9514b261#L226"]
spine_want: "Luật phải chặt, không xung đột, không trùng."
spine_want_lines: ["claude:9514b261#L226"]
spine_obstacle: "Có 374 vi phạm mã quyết định trong tên test, và lệnh ghi baseline ghi đè vô điều kiện nên có thể che vi phạm mới."
spine_obstacle_lines: ["claude:9514b261#L262"]
spine_turn: Agent tưởng máy kiểm mã quyết định đang chặn vi phạm mới. Hoá ra nó không chạy ở đâu ngoài test của chính nó.
spine_turn_lines: ["claude:9514b261#L262", "claude:9514b261#L383"]
spine_action: "Lập plan sáu phase cho nhóm sửa luật 1A, chưa sửa file luật hay code nào."
spine_action_lines: ["claude:9514b261#L262"]
spine_outcome: Plan đang chờ duyệt khung; phase 1 đến 4 chưa làm.
spine_outcome_lines: ["claude:9514b261#L262"]
spine_takeaway: Máy kiểm chưa nối vào đường chạy nào thì coi như không có. Hãy kiểm nó chạy ở đâu trước khi tin.
spine_takeaway_lines: ["claude:9514b261#L383"]
completeness: 7
---

# Máy kiểm đã viết xong nhưng không chạy ở đâu: 374 vi phạm và một lệnh ghi đè nuốt vi phạm mới

**Góc kể:** Dự án Forgent là nền tảng để xây app agent, và người làm đang gom các luật rải rác để agent không dùng lẫn luật cũ. Agent tin máy kiểm mã quyết định đang chặn vi phạm mới, nhưng nó không chạy trong npm test nào, và lệnh ghi baseline còn ghi đè vô điều kiện. Dev làm công cụ có quy tắc cho agent nên quan tâm, vì một máy kiểm không nối vào đường chạy thì không bảo vệ được gì.
**Bối cảnh:** Repo có nhiều máy kiểm quyết định, nhưng agent phát hiện chúng chưa được nối vào đường chạy nào. Agent đang lập kế hoạch nhóm sửa luật 1A.
**Chuyện gì xảy ra:** check-decision-codes báo 374 vi phạm (tên test nhúng mã quyết định) nhưng chỉ chạy trong test của chính nó, không chạy trong npm test. Cả hai script baseline đều ghi đè vô điều kiện, nên chạy lại lệnh là mọi vi phạm mới thành 'đã biết' mà không ai hay. Agent cũng thấy hai đường dẫn chết trong thông báo của pre-commit. Kế hoạch chia 6 việc: phase 1 đến 4 làm ngay, phase 5 đến 6 chờ xác nhận manifest.
**Bài học:** Một máy kiểm không được nối vào đường chạy thì coi như không có; hãy kiểm xem nó thật sự chạy ở đâu trước khi tin nó.
**Artefact:** Bảng ba máy kiểm gồm tên, thứ nó canh và thời điểm chạy. Không cần ảnh.
