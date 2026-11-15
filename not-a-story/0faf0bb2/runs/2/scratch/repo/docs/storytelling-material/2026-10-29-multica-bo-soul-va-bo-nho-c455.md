---
id: 2026-10-29-multica-bo-soul-va-bo-nho-c455
code: M-DRMX
aliases: [M-DRMX]
date: 2026-10-29
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo, rang_buoc_thiet_ke]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L2105", "claude:0faf0bb2#L2126", "claude:0faf0bb2#L2336"]
hook: "Ghép hai hệ thống xong, agent mất luôn 'linh hồn' và trí nhớ"
tension: hop_ma_tan
sides: ["Ghép Multica với AICoworker để có thêm sức mạnh", "SOUL.md và MEMORY.md bị loại, agent mất danh tính và trí nhớ dài hạn"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án là bộ dựng công ty một người chạy bằng AI agent, nền là Multica, và người làm đang so sánh với AICoworker để chọn cách ghép. Người làm hỏi lại hai lần rằng Multica có định nghĩa agent như AICoworker không, tức là tưởng nó cũng giữ được danh tính agent. Đọc code thì Multica bỏ SOUL.md và MEMORY.md của agent OpenClaw, nên agent mất danh tính và bộ nhớ dài hạn khi chạy qua Multica. Ai ghép hai hệ thống agent nên kiểm tra lớp điều phối có ghi đè không gian làm việc của agent không."
audience: dev ghép hai hệ thống agent AI
spine_context: "Dự án là bộ dựng công ty một người chạy bằng AI agent, nền là Multica; người làm đang so sánh với AICoworker."
spine_context_lines: [profile, "claude:0faf0bb2#L2130"]
spine_want: Muốn biết Multica có định nghĩa agent như AICoworker không.
spine_want_lines: ["claude:0faf0bb2#L2081"]
spine_obstacle: Multica đặt workspace của agent OpenClaw thành thư mục của từng task.
spine_obstacle_lines: ["claude:0faf0bb2#L2105"]
spine_turn: "Hỏi lại rằng Multica có định nghĩa agent như AICoworker không; hoá ra Multica bỏ SOUL.md và MEMORY.md của host, nên agent mất danh tính và bộ nhớ dài hạn."
spine_turn_lines: ["claude:0faf0bb2#L2081", "claude:0faf0bb2#L2336"]
spine_action: Đọc code và ghi phát hiện vào tài liệu so sánh.
spine_action_lines: ["claude:0faf0bb2#L2104", "claude:0faf0bb2#L2114"]
spine_outcome: "Phát hiện đã được ghi vào lesson, vision.md và tài liệu so sánh."
spine_outcome_lines: ["claude:0faf0bb2#L2336"]
spine_takeaway: "Trước khi ghép hai hệ thống agent, tìm xem lớp điều phối có ghi đè không gian làm việc của agent không."
spine_takeaway_lines: ["claude:0faf0bb2#L2105"]
completeness: 7
---

# Multica bỏ SOUL và bộ nhớ của agent OpenClaw: mất 'con người' của agent khi ghép với AICoworker

**Góc kể:** Dự án là bộ dựng công ty một người chạy bằng AI agent, nền là Multica, và người làm đang so sánh với AICoworker để chọn cách ghép. Người làm hỏi lại hai lần rằng Multica có định nghĩa agent như AICoworker không, tức là tưởng nó cũng giữ được danh tính agent. Đọc code thì Multica bỏ SOUL.md và MEMORY.md của agent OpenClaw, nên agent mất danh tính và bộ nhớ dài hạn khi chạy qua Multica. Ai ghép hai hệ thống agent nên kiểm tra lớp điều phối có ghi đè không gian làm việc của agent không.
**Bối cảnh:** Câu hỏi: Multica có định nghĩa agent như AICoworker không. Đọc code thì thấy Multica cố ý đổi workspace OpenClaw thành thư mục của từng task.
**Chuyện gì xảy ra:** Trong openclaw_config.go, Multica đặt workspace của mọi agent OpenClaw thành thư mục task và ghi rõ SOUL.md và MEMORY.md của host bị loại trừ. Multica không có bộ nhớ dài hạn; chỉ nối lại được session theo cặp (agent, issue). Ở chế độ gateway thì có thể giữ được danh tính nhưng chưa kiểm chứng.
**Bài học:** Trước khi ghép hai hệ thống agent, tìm xem lớp điều phối có ghi đè không gian làm việc của agent hay không.
**Artefact:** Trích dẫn comment trong code 'Host-workspace SOUL.md and MEMORY.md are therefore excluded' (không kèm đường dẫn máy).
