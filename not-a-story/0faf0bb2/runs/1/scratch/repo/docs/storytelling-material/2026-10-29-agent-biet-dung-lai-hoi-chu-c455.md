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
sides: ["Bị trả bài hai lần, có thể điền số cho xong", "Dừng lại hỏi chủ giá 350.000đ thay vì tự bịa"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: none
spine_context: "Một bộ dựng công ty một người vận hành bằng AI agent trên nền Multica, đang thử luồng giao việc qua issue có cổng duyệt."
spine_context_lines: [profile, "claude:0faf0bb2#L3398"]
spine_want: Muốn một bài đăng có giá và hạn ưu đãi đi hết luồng tới bước chờ chủ duyệt.
spine_want_lines: ["claude:0faf0bb2#L3707"]
spine_obstacle: "Chủ chưa đưa giá và hạn đặt trước, nên bài không có số để viết."
spine_obstacle_lines: ["claude:0faf0bb2#L3691"]
spine_action: "Agent viết bài dừng lại, hỏi chủ qua comment thay vì tự điền số liệu."
spine_action_lines: ["claude:0faf0bb2#L3696"]
spine_outcome: "Chủ comment giá 350.000đ và hạn 15/01; issue vào in_review, giao cho chủ."
spine_outcome_lines: ["claude:0faf0bb2#L3691", "claude:0faf0bb2#L3707"]
spine_takeaway: Ràng buộc không bịa số liệu khiến agent tạm dừng và hỏi người; vòng hỏi-đáp qua comment đủ để hoàn tất bước.
spine_takeaway_lines: ["claude:0faf0bb2#L3712"]
completeness: 6
---

# Agent biết dừng lại hỏi chủ thay vì tự bịa số liệu bán hàng

**Bối cảnh:** Trong workflow bài đăng Facebook, agent Mai được giao viết bài có giá và hạn chót ưu đãi, nhưng chủ chưa cung cấp các con số này.
**Chuyện gì xảy ra:** Long trả lại bài hai lần vì thiếu giá. Mai dừng lại và hỏi chủ giá (350.000đ) và hạn đặt trước (15/01), nói rõ không tự bịa số liệu bán hàng. Sau khi chủ comment, Mai điền vào và Long duyệt đạt, đưa issue sang in_review cho chủ.
**Bài học:** Ràng buộc 'không bịa số liệu' làm agent tạm dừng và hỏi người; vòng hỏi-đáp qua comment đủ để hoàn tất một bước workflow.
**Artefact:** Ảnh chụp chuỗi comment SEN-2 (che tên khách và email).
