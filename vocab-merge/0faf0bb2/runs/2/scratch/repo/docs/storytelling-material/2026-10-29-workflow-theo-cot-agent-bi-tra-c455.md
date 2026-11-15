---
id: 2026-10-29-workflow-theo-cot-agent-bi-tra-c455
code: M-1AR9
aliases: [M-1AR9]
date: 2026-10-29
repo: repo
status: raw
signals: [vòng lặp người với máy, artefact]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L3622", "claude:0faf0bb2#L3629", "claude:0faf0bb2#L3671", "claude:0faf0bb2#L3691", "claude:0faf0bb2#L3712", "claude:0faf0bb2#L3747"]
hook: "Agent bị trả lại hai lần, rồi hỏi chủ thay vì bịa số"
tension: khac
sides: ["Bị trả lại hai lần vì thiếu giá", "Agent dừng hỏi chủ, không tự bịa số hay tự đóng"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Workflow theo cột: agent bị trả lại hai lần, hỏi chủ thay vì bịa số, không tự đóng

**Bối cảnh:** Spike Multica với Claude Code, workflow Nháp, Sales review, In review, Done.
**Chuyện gì xảy ra:** Issue không chỉ định người vẫn tự giao cho agent soạn. Khi chuyển cột, issue tự giao cho agent duyệt. Agent duyệt trả lại lần đầu vì thiếu giá. Lần hai, agent soạn để trống và bị trả lại tiếp. Agent dừng lại và hỏi chủ về giá và hạn chót, không tự bịa số liệu. Chủ điền thông tin, agent duyệt chuyển sang in_review và giao cho chủ. Không agent nào tự chuyển done. Ghi ngược vào Multica mất 16 giây.
**Bài học:** Cho agent quyền dừng và hỏi người thì kết quả tốt hơn là bịa số liệu. Bước done nên giữ cho người.
**Artefact:** Board workflow với các cột và lịch sử chuyển cột. Đã che tên và id.
