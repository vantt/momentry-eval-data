---
id: 2026-10-29-doi-huong-multica-claude-code-dat-c455
code: M-GAXP
aliases: [M-GAXP]
date: 2026-10-29
repo: repo
status: raw
signals: [dao_quyet_dinh, nguoi_duyet_may_soan, artefact_nhin_duoc]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L3398", "claude:0faf0bb2#L3404", "claude:0faf0bb2#L3712", "claude:0faf0bb2#L3747"]
hook: "Đổi sang Claude Code, Multica từ trượt thành đạt 5/5 tiêu chí"
tension: khac
sides: ["Multica + AICoworker trượt spike", "Multica + Claude Code đạt 5/5, agent tự dừng hỏi giá"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án Bộ dựng công ty một người chạy bằng AI agent trên nền Multica, và đang thử xem agent có làm việc theo cột có bước duyệt được không. Người làm tưởng Multica phải chạy trên runtime OpenClaw, nhưng chat nhiều phiên trên bản OpenClaw đang dùng không chạy được, còn đổi sang Claude Code thì đạt 5/5 tiêu chí. Ai định ghép agent vào việc có bước duyệt nên biết runtime nào thật sự chạy trước khi đầu tư."
audience: người muốn giao việc cho AI agent có bước duyệt
spine_context: "Dự án Bộ dựng công ty một người chạy bằng AI agent trên nền Multica, đang thử xem agent có làm việc theo cột có bước duyệt được không."
spine_context_lines: [profile, "claude:0faf0bb2#L3398"]
spine_want: Muốn biết Multica có chạy được với Claude Code và agent có tự giao việc theo cột không.
spine_want_lines: ["claude:0faf0bb2#L3398", "claude:0faf0bb2#L3404"]
spine_obstacle: Chat nhiều phiên trên OpenClaw không chạy được với bản 2026.3.13.
spine_obstacle_lines: ["claude:0faf0bb2#L3386"]
spine_turn: "Tưởng Multica phải chạy trên runtime OpenClaw; hoá ra chat nhiều phiên trên OpenClaw không chạy, còn Claude Code thì chạy."
spine_turn_lines: ["claude:0faf0bb2#L3373", "claude:0faf0bb2#L3386"]
spine_action: Đổi runtime sang Claude Code và chạy spike B' kiểm 5 tiêu chí.
spine_action_lines: ["claude:0faf0bb2#L3398", "claude:0faf0bb2#L3404"]
spine_outcome: "Đạt 5/5 tiêu chí; comment và chuyển in_review trong 16 giây, không agent nào tự chuyển done."
spine_outcome_lines: ["claude:0faf0bb2#L3747"]
spine_takeaway: "Trước khi chọn runtime, kiểm tính năng của đúng bản đang dùng; 'theo lý thuyết có' chưa đủ."
spine_takeaway_lines: ["claude:0faf0bb2#L3386"]
completeness: 7
---

# Đổi hướng: Multica + Claude Code đạt 5/5 tiêu chí sau khi Multica + AICoworker trượt

**Góc kể:** Dự án Bộ dựng công ty một người chạy bằng AI agent trên nền Multica, và đang thử xem agent có làm việc theo cột có bước duyệt được không. Người làm tưởng Multica phải chạy trên runtime OpenClaw, nhưng chat nhiều phiên trên bản OpenClaw đang dùng không chạy được, còn đổi sang Claude Code thì đạt 5/5 tiêu chí. Ai định ghép agent vào việc có bước duyệt nên biết runtime nào thật sự chạy trước khi đầu tư.
**Bối cảnh:** Sau khi spike với OpenClaw trượt, chủ yêu cầu thử Multica với Claude Code. Đây là hướng đi thay thế bỏ hẳn AICoworker.
**Chuyện gì xảy ra:** Spike với 5 tiêu chí: agent làm đúng vai trò, ghi comment và chuyển in_review trong 16 giây, tiếp nối session (resume_session=true), workflow Nháp → Sales review → In review → Done tự giao việc, và chat hai phiên giữ ngữ cảnh riêng. SEN-2 đi qua hai vòng 'Needs changes' và một lần agent dừng hỏi chủ về giá vì không tự bịa số liệu. Không agent nào tự chuyển done.
**Bài học:** Thay đổi runtime có thể cứu cả thử nghiệm: đổi từ OpenClaw sang Claude Code đạt được tất cả tiêu chí. Ghi rõ đánh đổi (mất bộ nhớ và SOUL, chạy bypassPermissions) cùng kết quả.
**Artefact:** Bảng 5/5 tiêu chí và ảnh chụp board Multica có SEN-2 ở cột in_review (che email và IP tailnet).
