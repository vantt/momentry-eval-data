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
hook: "Multica + AICoworker trượt, đổi sang Claude Code thì đạt 5/5 tiêu chí"
tension: khac
sides: ["Tổ hợp ban đầu trượt vì phiên bản", "Đổi runtime sang Claude Code, đạt 5/5, comment xong trong 16 giây"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đổi hướng: Multica + Claude Code đạt 5/5 tiêu chí sau khi Multica + AICoworker trượt

**Bối cảnh:** Sau khi spike với OpenClaw trượt, chủ yêu cầu thử Multica với Claude Code. Đây là hướng đi thay thế bỏ hẳn AICoworker.
**Chuyện gì xảy ra:** Spike với 5 tiêu chí: agent làm đúng vai trò, ghi comment và chuyển in_review trong 16 giây, tiếp nối session (resume_session=true), workflow Nháp → Sales review → In review → Done tự giao việc, và chat hai phiên giữ ngữ cảnh riêng. SEN-2 đi qua hai vòng 'Needs changes' và một lần agent dừng hỏi chủ về giá vì không tự bịa số liệu. Không agent nào tự chuyển done.
**Bài học:** Thay đổi runtime có thể cứu cả thử nghiệm: đổi từ OpenClaw sang Claude Code đạt được tất cả tiêu chí. Ghi rõ đánh đổi (mất bộ nhớ và SOUL, chạy bypassPermissions) cùng kết quả.
**Artefact:** Bảng 5/5 tiêu chí và ảnh chụp board Multica có SEN-2 ở cột in_review (che email và IP tailnet).
