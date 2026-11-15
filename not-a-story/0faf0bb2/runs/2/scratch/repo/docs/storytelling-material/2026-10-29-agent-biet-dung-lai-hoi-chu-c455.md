---
id: 2026-10-29-agent-biet-dung-lai-hoi-chu-c455
code: M-F570
aliases: [M-F570]
date: 2026-10-29
repo: repo
status: raw
signals: [rang_buoc_thiet_ke, artefact_nhin_duoc]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L3691", "claude:0faf0bb2#L3709", "claude:0faf0bb2#L3712"]
hook: "Agent bị trả bài hai lần vì thiếu giá, nhất quyết không bịa số"
tension: khac
sides: ["Có thể điền đại một con số để qua duyệt cho nhanh", "Agent dừng hỏi chủ giá 350.000đ và hạn 15/01 rồi mới điền, bài mới đạt"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: none
spine_context: "Bộ dựng công ty một người chạy bằng AI agent trên Multica, đang thử nghiệm workflow với agent Mai viết bài và Long duyệt."
spine_context_lines: [profile, "claude:0faf0bb2#L3691"]
spine_want: Thử nghiệm Multica cùng Claude Code.
spine_want_lines: ["claude:0faf0bb2#L3398"]
spine_obstacle: Bài thiếu giá và hạn ưu đãi nên Long trả lại hai vòng.
spine_obstacle_lines: ["claude:0faf0bb2#L3712"]
spine_action: Mai dừng lại hỏi chủ giá và hạn; chủ comment; Mai điền; Long duyệt đạt.
spine_action_lines: ["claude:0faf0bb2#L3691", "claude:0faf0bb2#L3712"]
spine_outcome: "SEN-2 đi tới in_review, giao cho chủ; không agent nào tự chuyển done."
spine_outcome_lines: ["claude:0faf0bb2#L3707", "claude:0faf0bb2#L3712"]
spine_takeaway: Ràng buộc không bịa số làm agent dừng hỏi người; vòng hỏi-đáp qua comment đủ để hoàn tất bước.
spine_takeaway_lines: ["claude:0faf0bb2#L3712"]
completeness: 6
---

# Agent biết dừng lại hỏi chủ thay vì tự bịa số liệu bán hàng

**Bối cảnh:** Trong workflow bài đăng Facebook, agent Mai được giao viết bài có giá và hạn chót ưu đãi, nhưng chủ chưa cung cấp các con số này.
**Chuyện gì xảy ra:** Long trả lại bài hai lần vì thiếu giá. Mai dừng lại và hỏi chủ giá (350.000đ) và hạn đặt trước (15/01), nói rõ không tự bịa số liệu bán hàng. Sau khi chủ comment, Mai điền vào và Long duyệt đạt, đưa issue sang in_review cho chủ.
**Bài học:** Ràng buộc 'không bịa số liệu' làm agent tạm dừng và hỏi người; vòng hỏi-đáp qua comment đủ để hoàn tất một bước workflow.
**Artefact:** Ảnh chụp chuỗi comment SEN-2 (che tên khách và email).
