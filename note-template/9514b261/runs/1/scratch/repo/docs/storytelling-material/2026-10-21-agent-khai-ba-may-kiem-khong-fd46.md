---
id: 2026-10-21-agent-khai-ba-may-kiem-khong-fd46
code: M-KRTA
aliases: [M-KRTA]
date: 2026-10-21
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L262", "claude:9514b261#L333", "claude:9514b261#L349", "claude:9514b261#L383", "claude:9514b261#L542"]
hook: "Agent khai ba máy kiểm không thuộc ai, nhưng tsk-1lv đã xong"
tension: tuong_ma_hoa_ra
sides: ["Bản đồ kiến trúc nói ba máy kiểm không thuộc component nào", "Work item cho thấy tsk-1lv đã làm xong 6 việc con, hai máy kiểm thuộc dòng này"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án là Forgent (fgOS), một lớp nền để dựng ứng dụng agent. Người làm đang lập plan sửa các luật và máy kiểm đang lệch trong một repo nhiều lane song song, và agent kết luận ba máy kiểm 'không thuộc component nào' chỉ vì tra bản đồ kiến trúc. Khi chủ dự án hỏi lại, việc tra work item cho thấy component canonical-decision-projection (tsk-1lv) đã xong sáu việc con và quản hai trong ba máy đó. Điều đáng nghe là một cơ chế trông như không có chủ có thể đã có chủ, chỉ là chủ nằm ở work item chứ không nằm trên sơ đồ."
audience: dev dùng agent để viết code và quản luật trong repo
spine_context: Forgent (fgOS) là lớp nền để dựng ứng dụng agent. Người làm đang lập plan nhóm 1A để sửa các luật và máy kiểm đang lệch trong một repo có nhiều lane làm song song.
spine_context_lines: [profile, "claude:9514b261#L262"]
spine_want: "Muốn agent không bị dẫn sai bởi chỉ dẫn cũ, và máy kiểm không bị tắt âm thầm."
spine_want_lines: ["claude:9514b261#L282"]
spine_obstacle: Agent không tìm được chủ của ba máy kiểm trong bản đồ kiến trúc.
spine_obstacle_lines: ["claude:9514b261#L333"]
spine_turn: Tưởng ba máy kiểm không thuộc component nào; hoá ra component canonical-decision-projection (tsk-1lv) đã làm xong và quản hai trong ba máy đó.
spine_turn_lines: ["claude:9514b261#L383", "claude:9514b261#L542"]
spine_action: "Tra work item và lịch sử quyết định thay vì chỉ tra bản đồ kiến trúc, rồi đính chính kết luận cũ."
spine_action_lines: ["claude:9514b261#L525", "claude:9514b261#L542"]
spine_outcome: Component đã xong sáu việc con; tsk-2yu đang blocked. Người làm yêu cầu viết report nghiên cứu chi tiết về component này.
spine_outcome_lines: ["claude:9514b261#L542", "claude:9514b261#L551"]
spine_takeaway: "Trước khi kết luận một cơ chế không có chủ, hãy tra cả work item và lịch sử quyết định, không chỉ bản đồ kiến trúc."
spine_takeaway_lines: ["claude:9514b261#L542"]
completeness: 7
---

# Agent khai ba máy kiểm 'không thuộc component nào', chủ dự án chỉ ra đã có tsk-1lv

**Góc kể:** Dự án là Forgent (fgOS), một lớp nền để dựng ứng dụng agent. Người làm đang lập plan sửa các luật và máy kiểm đang lệch trong một repo nhiều lane song song, và agent kết luận ba máy kiểm 'không thuộc component nào' chỉ vì tra bản đồ kiến trúc. Khi chủ dự án hỏi lại, việc tra work item cho thấy component canonical-decision-projection (tsk-1lv) đã xong sáu việc con và quản hai trong ba máy đó. Điều đáng nghe là một cơ chế trông như không có chủ có thể đã có chủ, chỉ là chủ nằm ở work item chứ không nằm trên sơ đồ.
**Bối cảnh:** Đang lập plan nhóm 1A (sửa luật và máy kiểm) cho một repo có nhiều lane làm song song. Agent phân loại chủ của từng máy kiểm bằng bản đồ kiến trúc và kết luận ba máy 'không thuộc component nào'.
**Chuyện gì xảy ra:** Chủ dự án hỏi lại 'vậy kiểm là kiểm gì', nhắc có một component gom và làm tươi luật. Agent tìm trong plan, lịch sử quyết định và work item, và thấy đó là canonical-decision-projection (tsk-1lv), đã xong với 6 việc con. Hai trong ba máy kiểm thuộc dòng việc này. Kết luận sai ban đầu đến từ việc chỉ tra bản đồ kiến trúc, không tra work item. Plan 1A ghi 374 vi phạm và bảng 161 vấn đề về cưỡng chế rải ở năm cửa.
**Bài học:** Trước khi kết luận một cơ chế 'không có chủ', hãy tra cả work item và lịch sử quyết định, không chỉ bản đồ kiến trúc.
**Artefact:** Bảng so sánh ba máy kiểm: nó canh gì, chạy khi nào, chủ theo bằng chứng. Không cần che gì.
