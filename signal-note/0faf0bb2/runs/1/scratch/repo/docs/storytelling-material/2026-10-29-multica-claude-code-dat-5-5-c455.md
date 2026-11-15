---
id: 2026-10-29-multica-claude-code-dat-5-5-c455
code: M-5C6Q
aliases: [M-5C6Q]
date: 2026-10-29
repo: repo
status: raw
signals: [dao_quyet_dinh, so_truoc_so_sau]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L3404", "claude:0faf0bb2#L3412", "claude:0faf0bb2#L3420", "claude:0faf0bb2#L3444", "claude:0faf0bb2#L3485", "claude:0faf0bb2#L3556", "claude:0faf0bb2#L3747"]
hook: "Lần trước trượt, lần này Multica đạt 5/5 và xong trong 16 giây"
tension: tuong_ma_hoa_ra
sides: ["Lần trước kết luận là trượt", "Chạy lại đạt 5/5, nhưng agent chạy bypassPermissions không sandbox"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: none
spine_context: "Bộ dựng công ty một người chạy bằng đội agent AI trên nền Multica tự host, đang thử chạy agent bằng Claude Code."
spine_context_lines: [profile, "claude:0faf0bb2#L3398"]
spine_want: "Chạy thử Multica với Claude Code để kiểm năm tiêu chí: đúng vai trò, ghi ngược vào Multica, nối tiếp session, workflow theo cột, chat nhiều phiên."
spine_want_lines: ["claude:0faf0bb2#L3398", "claude:0faf0bb2#L3404"]
spine_obstacle: "Lần thử trước với runtime OpenClaw bị trượt, không chạy được với bản đang dùng."
spine_obstacle_lines: ["claude:0faf0bb2#L3394"]
spine_action: "Kiểm Claude Code trên máy, tải CLI Multica v0.7.1 và xác minh checksum, dựng stack rồi đăng nhập CLI."
spine_action_lines: ["claude:0faf0bb2#L3405", "claude:0faf0bb2#L3420", "claude:0faf0bb2#L3423", "claude:0faf0bb2#L3429"]
spine_outcome: "Đạt 5/5 tiêu chí; agent comment và chuyển in_review trong 16 giây, không tự chuyển done."
spine_outcome_lines: ["claude:0faf0bb2#L3747"]
completeness: 5
---

# Multica + Claude Code đạt 5/5 tiêu chí: đảo kết quả trượt của lần trước

**Bối cảnh:** Sau khi spike OpenClaw trượt, thử lại Multica với Claude Code CLI 2.1.312 trên cùng máy.
**Chuyện gì xảy ra:** SEN-1 của agent Mai: viết 2 câu, comment và chuyển in_review trong khoảng 16 giây. Lượt chạy sau có resume_session=true, hai phiên chat cho hai khách không lẫn ngữ cảnh, và không agent nào tự chuyển done. Điểm rủi ro: agent chạy với bypassPermissions và không có sandbox.
**Bài học:** Khi một runtime trượt, thử runtime khác cùng điều phối để tách lỗi tích hợp khỏi lỗi ý tưởng.
**Artefact:** Bảng năm tiêu chí đạt hoặc trượt.
