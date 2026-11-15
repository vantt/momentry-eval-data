---
id: 2026-10-29-ba-he-thong-ba-cach-dong-c455
code: M-76XF
aliases: [M-76XF]
date: 2026-10-29
repo: repo
status: raw
signals: [số, ràng buộc định hình thiết kế]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L3836", "claude:0faf0bb2#L3844", "claude:0faf0bb2#L3877", "claude:0faf0bb2#L3889", "claude:0faf0bb2#L3927"]
hook: "Ba hệ thống, ba kiểu đóng gói: cả công ty, một agent, hoặc chỉ skill"
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

# Ba hệ thống, ba cách đóng gói: Paperclip gói cả công ty, AICoworker gói một agent, Multica chỉ gói skill

**Bối cảnh:** Nghiên cứu cách đóng gói một công ty OPC để có thể deploy lại.
**Chuyện gì xảy ra:** Paperclip export và import theo chuẩn Agent Companies v1, gồm COMPANY.md, TEAM.md, AGENTS.md, PROJECT.md, TASK.md và SKILL.md. Khi trùng tên có các chế độ rename, skip và replace. AICoworker đóng gói .agent cho một agent, có quét secret, và khi cập nhật thì giữ các file người dùng đã sửa. Multica chỉ import skill từ GitHub hoặc zip, còn workflow, agent và squad không export được. Chuẩn mở không định nghĩa cách mô tả workflow.
**Bài học:** Trước khi thiết kế định dạng, kiểm tra xem chuẩn đã định nghĩa phần nào. Workflow gần như chưa ai chuẩn hoá.
**Artefact:** Bảng ba hàng: đóng gói được gì và thiếu gì.
