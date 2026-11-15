---
id: 2026-10-29-cot-workflow-mai-viet-long-tra-c455
code: M-4VWX
aliases: [M-4VWX]
date: 2026-10-29
repo: repo
status: raw
signals: [nguoi_duyet_may_soan, artefact_nhin_duoc]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L3622", "claude:0faf0bb2#L3629", "claude:0faf0bb2#L3671", "claude:0faf0bb2#L3691", "claude:0faf0bb2#L3707", "claude:0faf0bb2#L3709", "claude:0faf0bb2#L3712"]
hook: "Bị trả lại hai lần vì thiếu giá, agent dừng hỏi thay vì bịa"
tension: khac
sides: ["Bị ép sửa hai vòng cho xong", "Agent để trống và hỏi chủ chứ không tự điền giá"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Người làm đang dựng một bộ agent AI trên Multica tự host, để agent nhận việc qua issue và đi qua các cột duyệt trước khi chủ chốt. Bài đăng SEN-2 do Mai viết đã sang cột duyệt, nhưng Long trả lại về todo vì thiếu giá, và Mai dừng lại chờ chủ thay vì tự điền. Với dev làm workflow agent, đáng nhớ là bước chuyển cột chưa có nghĩa là xong, và chỗ thiếu số liệu nên để người điền."
audience: dev xây workflow cho agent AI
spine_context: "Người làm đang dựng một bộ agent AI trên Multica tự host, cho một công ty một người. Agent nhận việc qua issue và đi qua các cột workflow có chủ duyệt."
spine_context_lines: [profile, "claude:0faf0bb2#L3398"]
spine_want: Muốn thử xem workflow theo cột với agent Mai (viết) và Long (duyệt) có chạy đúng không.
spine_want_lines: ["claude:0faf0bb2#L3398"]
spine_obstacle: "Long trả SEN-2 về todo và giao lại cho Mai, nên bài chưa qua được vòng duyệt."
spine_obstacle_lines: ["claude:0faf0bb2#L3629"]
spine_turn: Tưởng bài nháp chuyển sang cột duyệt là gần xong; hoá ra Long trả lại về todo.
spine_turn_lines: ["claude:0faf0bb2#L3622", "claude:0faf0bb2#L3629"]
spine_action: "Mai dừng lại và chờ chủ bổ sung thông tin; chủ comment giá 350.000đ, ưu đãi và hạn đặt trước."
spine_action_lines: ["claude:0faf0bb2#L3691"]
spine_outcome: SEN-2 đi tới in_review và giao cho chủ; Long duyệt đạt sau khi Mai điền đủ thông tin.
spine_outcome_lines: ["claude:0faf0bb2#L3702", "claude:0faf0bb2#L3712"]
spine_takeaway: "Chuyển cột chưa phải là xong: cột duyệt có thể đẩy ngược lại, và thiếu số liệu thì nên để agent hỏi người chứ không tự điền."
spine_takeaway_lines: ["claude:0faf0bb2#L3712"]
completeness: 7
---

# Cột workflow: Mai viết, Long trả lại hai vòng, Mai dừng lại hỏi chủ thay vì bịa giá

**Góc kể:** Người làm đang dựng một bộ agent AI trên Multica tự host, để agent nhận việc qua issue và đi qua các cột duyệt trước khi chủ chốt. Bài đăng SEN-2 do Mai viết đã sang cột duyệt, nhưng Long trả lại về todo vì thiếu giá, và Mai dừng lại chờ chủ thay vì tự điền. Với dev làm workflow agent, đáng nhớ là bước chuyển cột chưa có nghĩa là xong, và chỗ thiếu số liệu nên để người điền.
**Bối cảnh:** Workflow 'Bài đăng FB' gồm Nháp (Mai), Sales review (Long), In review (chủ) và Done; SEN-2 được tạo mà không chỉ định người.
**Chuyện gì xảy ra:** Mai viết xong thì SEN-2 tự giao cho Long. Long trả lại hai lần vì thiếu giá; Mai sửa nhưng để chỗ trống, rồi dừng và hỏi chủ giá và hạn chót thay vì tự điền. Sau khi chủ comment, Long duyệt và thẻ sang in_review cho chủ. Monitor hết giờ 15 phút trước khi chủ trả lời.
**Bài học:** Trong chuỗi agent viết và agent duyệt, cho agent quyền hỏi người để tránh bịa số liệu.
**Artefact:** Ảnh board workflow (chưa chụp); che tên khách và số liệu thật nếu có.
