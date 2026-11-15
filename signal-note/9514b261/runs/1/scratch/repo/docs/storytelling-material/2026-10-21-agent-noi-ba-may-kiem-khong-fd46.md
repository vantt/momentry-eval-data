---
id: 2026-10-21-agent-noi-ba-may-kiem-khong-fd46
code: M-9QYC
aliases: [M-9QYC]
date: 2026-10-21
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L333", "claude:9514b261#L349", "claude:9514b261#L383", "claude:9514b261#L542"]
hook: "Agent bảo ba máy kiểm không thuộc component nào, nhưng component đó xong với sáu việc con"
tension: nguoi_dung_may_sai
sides: ["Agent kết luận ba máy kiểm không thuộc component nào", "Owner chỉ ra component đã xong, hai máy kiểm thuộc về nó"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Forgent là nền tảng để dev dựng ứng dụng agent, và người làm đang dọn các luật để agent không đọc nhầm luật cũ. Trước khi lập plan, người làm hỏi ai quản ba máy kiểm vệ sinh repo, và agent kết luận không ai quản vì bản đồ kiến trúc không có hàng nào. Hoá ra có một dòng việc tên canonical-decision-projection đã xong với sáu việc con, và hai trong ba máy kiểm thuộc dòng đó. Bài học: trước khi nói một thứ không có chủ, hãy tra cả danh sách việc và lịch sử quyết định, đừng chỉ tra bản đồ."
audience: dev dùng AI viết luật và tài liệu cho agent
spine_context: Forgent (fgOS) là tầng nền cho ứng dụng agent. Người làm đang dọn luật và decision để agent không đọc nhầm luật cũ.
spine_context_lines: [profile, "claude:9514b261#L8"]
spine_want: Biết ai quản ba máy kiểm vệ sinh repo trước khi lập plan sửa luật.
spine_want_lines: ["claude:9514b261#L363"]
spine_obstacle: Tra bản đồ kiến trúc không thấy hàng chủ nào cho ba máy kiểm.
spine_obstacle_lines: ["claude:9514b261#L383"]
spine_turn: "Tưởng ba máy kiểm không thuộc component nào; hoá ra hai trong ba thuộc canonical-decision-projection, một dòng việc đã xong."
spine_turn_lines: ["claude:9514b261#L383", "claude:9514b261#L394", "claude:9514b261#L542"]
spine_action: "Tra work item tsk-1lv và sáu việc con, rồi đính chính kết luận cũ trong plan."
spine_action_lines: ["claude:9514b261#L525", "claude:9514b261#L542"]
spine_outcome: "tsk-1lv và sáu việc con đều done, merge 83a3684b2."
spine_outcome_lines: ["claude:9514b261#L542"]
spine_takeaway: "Trước khi kết luận một thứ không có chủ, tra danh sách việc và lịch sử quyết định, đừng chỉ tra bản đồ kiến trúc."
spine_takeaway_lines: ["claude:9514b261#L525", "claude:9514b261#L542"]
completeness: 7
---

# Agent nói ba máy kiểm 'không thuộc component nào', rồi phát hiện một component đã xong với sáu item con

**Góc kể:** Forgent là nền tảng để dev dựng ứng dụng agent, và người làm đang dọn các luật để agent không đọc nhầm luật cũ. Trước khi lập plan, người làm hỏi ai quản ba máy kiểm vệ sinh repo, và agent kết luận không ai quản vì bản đồ kiến trúc không có hàng nào. Hoá ra có một dòng việc tên canonical-decision-projection đã xong với sáu việc con, và hai trong ba máy kiểm thuộc dòng đó. Bài học: trước khi nói một thứ không có chủ, hãy tra cả danh sách việc và lịch sử quyết định, đừng chỉ tra bản đồ.
**Bối cảnh:** Owner hỏi ai quản ba máy kiểm vệ sinh repo trước khi lập plan sửa luật. Agent đã tìm trong bản đồ kiến trúc và kết luận không có chủ.
**Chuyện gì xảy ra:** Agent kết luận ba máy kiểm không thuộc component nào. Owner nói có một component tên canonical-decision-projection. Kiểm bằng work item thì tsk-1lv và sáu item con đều done (merge 83a3684b2). Hai trong ba máy kiểm thuộc dòng việc này. Agent đính chính kết luận cũ và viết lại plan.
**Bài học:** Trước khi kết luận một thứ 'không có chủ', tra work item và lịch sử quyết định, đừng chỉ tra bản đồ kiến trúc.
**Artefact:** Bảng ba máy kiểm: tên script, nó canh gì, chạy khi nào, chủ theo bằng chứng. Che tên người và đường dẫn vault.
