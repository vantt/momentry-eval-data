---
id: 2026-10-29-chuan-dong-goi-paperclip-goi-duoc
date: 2026-10-29
repo: repo
status: raw
signals: [artefact nhìn được, khác]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L3836", "claude:0faf0bb2#L3844", "claude:0faf0bb2#L3876", "claude:0faf0bb2#L3889", "claude:0faf0bb2#L3927"]
hook: "Paperclip gói được cả công ty, Multica chỉ gói được skill"
tension: none
sides: []
strength: 0
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Chuẩn đóng gói: Paperclip gói được cả công ty, Multica chỉ gói skill

**Bối cảnh:** Mục tiêu là đóng gói một công ty OPC để deploy lại được. Mình đối chiếu ba hệ thống với chuẩn Agent Companies v1 và Agent Skills.
**Chuyện gì xảy ra:** Paperclip xuất và nhập cả công ty theo cấu trúc COMPANY.md, TEAM.md, AGENTS.md, PROJECT.md, TASK.md, SKILL.md, có chế độ rename, skip, replace. AICoworker đóng gói được một agent dạng .agent kèm kiểm tra secret. Multica chỉ đóng gói skill, không export được workflow, agent hay squad. Chuẩn hiện không định nghĩa workflow nhiều bước.
**Bài học:** Trước khi thiết kế định dạng riêng, kiểm chuẩn mở đã có và phần nào còn thiếu. Ở đây thiếu đúng phần workflow.
**Artefact:** Bảng ba hệ thống, cột 'đóng gói được' và 'thiếu'.
