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
hook: "Ghép agent với Multica, agent mất luôn 'linh hồn' và trí nhớ"
tension: hop_ma_tan
sides: ["Ghép hai hệ thống để agent mạnh hơn", "SOUL.md và MEMORY.md bị loại, agent mất danh tính"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án là bộ dựng công ty một người chạy bằng AI agent, nền là Multica, và người làm đang so sánh Multica với AICoworker. Câu hỏi đặt ra giả định rằng Multica cũng định nghĩa agent đầy đủ như AICoworker, có danh tính và bộ nhớ. Đọc code thì thấy Multica cố ý thay workspace của agent OpenClaw bằng thư mục riêng của từng task, bỏ SOUL.md và MEMORY.md của máy chủ, nên ai định ghép hai hệ thống nên kiểm tra điều này trước."
audience: dev ghép nhiều hệ thống agent với nhau
spine_context: "Dự án là bộ dựng công ty một người vận hành bằng AI agent, nền là Multica. Người làm đang so sánh Multica với AICoworker."
spine_context_lines: [profile, "claude:0faf0bb2#L2081"]
spine_want: Muốn biết Multica có định nghĩa agent như AICoworker không.
spine_want_lines: ["claude:0faf0bb2#L2081"]
spine_obstacle: "Mỗi task chạy trong thư mục mới, nên Multica chỉ nối lại được session cũ của cùng một cặp (agent, issue)."
spine_obstacle_lines: ["claude:0faf0bb2#L2126"]
spine_turn: "Tưởng Multica định nghĩa agent đầy đủ như AICoworker, có danh tính và bộ nhớ; hoá ra Multica bỏ SOUL.md và MEMORY.md của workspace host khi chạy agent OpenClaw."
spine_turn_lines: ["claude:0faf0bb2#L2081", "claude:0faf0bb2#L2105"]
spine_action: "Đọc đoạn code cấu hình OpenClaw trong Multica, rồi ghi kết luận vào tài liệu so sánh."
spine_action_lines: ["claude:0faf0bb2#L2104", "claude:0faf0bb2#L2107", "claude:0faf0bb2#L2114"]
spine_outcome: "Multica bỏ 2 file SOUL.md và MEMORY.md của host; với Multica + AICoworker, agent mất danh tính và bộ nhớ."
spine_outcome_lines: ["claude:0faf0bb2#L2105", "claude:0faf0bb2#L2126"]
spine_takeaway: "Trước khi ghép hai hệ thống agent, xem lớp điều phối có ghi đè workspace của agent không."
spine_takeaway_lines: ["claude:0faf0bb2#L2105"]
completeness: 7
---

# Multica bỏ SOUL và bộ nhớ của agent OpenClaw: mất 'con người' của agent khi ghép với AICoworker

**Góc kể:** Dự án là bộ dựng công ty một người chạy bằng AI agent, nền là Multica, và người làm đang so sánh Multica với AICoworker. Câu hỏi đặt ra giả định rằng Multica cũng định nghĩa agent đầy đủ như AICoworker, có danh tính và bộ nhớ. Đọc code thì thấy Multica cố ý thay workspace của agent OpenClaw bằng thư mục riêng của từng task, bỏ SOUL.md và MEMORY.md của máy chủ, nên ai định ghép hai hệ thống nên kiểm tra điều này trước.
**Bối cảnh:** Câu hỏi: Multica có định nghĩa agent như AICoworker không. Đọc code thì thấy Multica cố ý đổi workspace OpenClaw thành thư mục của từng task.
**Chuyện gì xảy ra:** Trong openclaw_config.go, Multica đặt workspace của mọi agent OpenClaw thành thư mục task và ghi rõ SOUL.md và MEMORY.md của host bị loại trừ. Multica không có bộ nhớ dài hạn; chỉ nối lại được session theo cặp (agent, issue). Ở chế độ gateway thì có thể giữ được danh tính nhưng chưa kiểm chứng.
**Bài học:** Trước khi ghép hai hệ thống agent, tìm xem lớp điều phối có ghi đè không gian làm việc của agent hay không.
**Artefact:** Trích dẫn comment trong code 'Host-workspace SOUL.md and MEMORY.md are therefore excluded' (không kèm đường dẫn máy).
