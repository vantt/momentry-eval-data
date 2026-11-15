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
hook: "Máy kiểm báo 374 vi phạm nhưng không chạy ở đâu, và chạy lại sẽ nuốt vi phạm mới"
tension: cam_ma_van_lot
sides: ["Đã viết máy kiểm, tưởng vi phạm bị chặn", "Nó không nằm trong npm test, và lệnh baseline ghi đè khiến vi phạm mới thành 'đã biết'"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Forgent là nền tảng để dựng app agent, và nhóm 1A đang sửa các luật gây hại ngay bây giờ. Người làm hỏi máy kiểm quyết định nào đang thật sự chạy và ai quản, rồi phát hiện plan của chính agent viết citation-drift 'chưa nối vào đâu'. Hoá ra một phần hàm của nó đã được lệnh ghi quyết định dùng, còn ba máy kiểm không thuộc component nào. Ai dựng máy kiểm tự động nên nghe chuyện này: máy kiểm không nối vào đường chạy thì coi như không có."
audience: dev viết máy kiểm và quy tắc cho repo có agent
spine_context: Forgent (fgOS) là nền tảng để dựng app agent; đang lập kế hoạch nhóm 1A để sửa các luật đang gây hại ngay bây giờ.
spine_context_lines: [profile, "claude:9514b261#L282"]
spine_want: Biết máy kiểm quyết định nào đang thật sự chạy và ai quản.
spine_want_lines: ["claude:9514b261#L363"]
spine_obstacle: "Máy kiểm có nhưng không chạy ở đâu, và không có chủ trong bản đồ kiến trúc."
spine_obstacle_lines: ["claude:9514b261#L383"]
spine_turn: Tưởng check-decision-citation-drift chưa nối vào đâu; hoá ra một phần hàm của nó đã được lệnh ghi quyết định dùng.
spine_turn_lines: ["claude:9514b261#L383"]
spine_action: "Đọc script, spec và pre-commit, rồi đính chính plan và lập bảng ba máy kiểm."
spine_action_lines: ["claude:9514b261#L366", "claude:9514b261#L383"]
spine_outcome: "Plan được sửa; bảng ba máy kiểm ghi rõ tên, việc canh và điều kiện chạy."
spine_outcome_lines: ["claude:9514b261#L383"]
spine_takeaway: "Trước khi tin một máy kiểm đang canh gì, xem nó chạy ở đâu và ai giữ nó."
spine_takeaway_lines: ["claude:9514b261#L383"]
completeness: 7
---

# Máy kiểm đã viết xong nhưng không chạy ở đâu: 374 vi phạm và một lệnh ghi đè nuốt vi phạm mới

**Góc kể:** Forgent là nền tảng để dựng app agent, và nhóm 1A đang sửa các luật gây hại ngay bây giờ. Người làm hỏi máy kiểm quyết định nào đang thật sự chạy và ai quản, rồi phát hiện plan của chính agent viết citation-drift 'chưa nối vào đâu'. Hoá ra một phần hàm của nó đã được lệnh ghi quyết định dùng, còn ba máy kiểm không thuộc component nào. Ai dựng máy kiểm tự động nên nghe chuyện này: máy kiểm không nối vào đường chạy thì coi như không có.
**Bối cảnh:** Repo có nhiều máy kiểm quyết định, nhưng agent phát hiện chúng chưa được nối vào đường chạy nào. Agent đang lập kế hoạch nhóm sửa luật 1A.
**Chuyện gì xảy ra:** check-decision-codes báo 374 vi phạm (tên test nhúng mã quyết định) nhưng chỉ chạy trong test của chính nó, không chạy trong npm test. Cả hai script baseline đều ghi đè vô điều kiện, nên chạy lại lệnh là mọi vi phạm mới thành 'đã biết' mà không ai hay. Agent cũng thấy hai đường dẫn chết trong thông báo của pre-commit. Kế hoạch chia 6 việc: phase 1 đến 4 làm ngay, phase 5 đến 6 chờ xác nhận manifest.
**Bài học:** Một máy kiểm không được nối vào đường chạy thì coi như không có; hãy kiểm xem nó thật sự chạy ở đâu trước khi tin nó.
**Artefact:** Bảng ba máy kiểm gồm tên, thứ nó canh và thời điểm chạy. Không cần ảnh.
