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
hook: "Multica trượt với AICoworker, đổi sang Claude Code thì đạt 5/5 tiêu chí"
tension: tuong_ma_hoa_ra
sides: ["Multica ghép AICoworker trượt, tưởng Multica chưa dùng được", "Đổi sang Claude Code đạt 5/5, comment và chuyển trạng thái trong 16 giây"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án là bộ dựng công ty một người chạy bằng AI agent, nền Multica, và người làm đang thử runtime thay thế. Người làm tưởng Multica cần runtime của OpenClaw (AICoworker) mới chạy được, nhưng spike với OpenClaw đã trượt. Khi đổi sang Claude Code, cùng bộ 5 tiêu chí đạt đủ 5/5: agent tự comment, tự chuyển in_review, và dừng hỏi chủ khi thiếu giá thay vì tự bịa. Người dùng agent nên quan tâm vì chỗ cần đổi có thể chỉ là runtime, không phải cả ý tưởng."
audience: dev dùng AI agent muốn giao việc nhưng vẫn giữ quyền duyệt
spine_context: "Bộ dựng công ty một người chạy bằng AI agent, nền là Multica; đang thử một runtime thay thế."
spine_context_lines: [profile, "claude:0faf0bb2#L3398"]
spine_want: Muốn biết Multica có chạy được với Claude Code không.
spine_want_lines: ["claude:0faf0bb2#L3398"]
spine_obstacle: AICoworker trên OpenClaw không chạy được với Multica; spike trước đó trượt.
spine_obstacle_lines: ["claude:0faf0bb2#L3394"]
spine_turn: Tưởng Multica cần runtime của OpenClaw; hoá ra Claude Code cũng chạy và đạt đủ 5/5 tiêu chí.
spine_turn_lines: ["claude:0faf0bb2#L3373", "claude:0faf0bb2#L3747"]
spine_action: Chạy spike Multica với Claude Code theo 5 tiêu chí.
spine_action_lines: ["claude:0faf0bb2#L3404", "claude:0faf0bb2#L3405"]
spine_outcome: Đạt 5/5; comment và chuyển in_review trong 16 giây; không agent nào tự chuyển done.
spine_outcome_lines: ["claude:0faf0bb2#L3747"]
spine_takeaway: "Khi một runtime trượt, thử đổi runtime trước khi bỏ cả hướng; chỉ dẫn không đủ để chặn agent tự done, cần kiểm ở phía server."
spine_takeaway_lines: ["claude:0faf0bb2#L3747"]
completeness: 7
---

# Đổi hướng: Multica + Claude Code đạt 5/5 tiêu chí sau khi Multica + AICoworker trượt

**Góc kể:** Dự án là bộ dựng công ty một người chạy bằng AI agent, nền Multica, và người làm đang thử runtime thay thế. Người làm tưởng Multica cần runtime của OpenClaw (AICoworker) mới chạy được, nhưng spike với OpenClaw đã trượt. Khi đổi sang Claude Code, cùng bộ 5 tiêu chí đạt đủ 5/5: agent tự comment, tự chuyển in_review, và dừng hỏi chủ khi thiếu giá thay vì tự bịa. Người dùng agent nên quan tâm vì chỗ cần đổi có thể chỉ là runtime, không phải cả ý tưởng.
**Bối cảnh:** Sau khi spike với OpenClaw trượt, chủ yêu cầu thử Multica với Claude Code. Đây là hướng đi thay thế bỏ hẳn AICoworker.
**Chuyện gì xảy ra:** Spike với 5 tiêu chí: agent làm đúng vai trò, ghi comment và chuyển in_review trong 16 giây, tiếp nối session (resume_session=true), workflow Nháp → Sales review → In review → Done tự giao việc, và chat hai phiên giữ ngữ cảnh riêng. SEN-2 đi qua hai vòng 'Needs changes' và một lần agent dừng hỏi chủ về giá vì không tự bịa số liệu. Không agent nào tự chuyển done.
**Bài học:** Thay đổi runtime có thể cứu cả thử nghiệm: đổi từ OpenClaw sang Claude Code đạt được tất cả tiêu chí. Ghi rõ đánh đổi (mất bộ nhớ và SOUL, chạy bypassPermissions) cùng kết quả.
**Artefact:** Bảng 5/5 tiêu chí và ảnh chụp board Multica có SEN-2 ở cột in_review (che email và IP tailnet).
