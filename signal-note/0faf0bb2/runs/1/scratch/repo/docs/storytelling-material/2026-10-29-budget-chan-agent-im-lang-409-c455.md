---
id: 2026-10-29-budget-chan-agent-im-lang-409-c455
code: M-X6CR
aliases: [M-X6CR]
date: 2026-10-29
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo, so_truoc_so_sau]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L1137", "claude:0faf0bb2#L1138", "claude:0faf0bb2#L1141", "claude:0faf0bb2#L1160", "claude:0faf0bb2#L1170", "claude:0faf0bb2#L1174", "claude:0faf0bb2#L1175", "claude:0faf0bb2#L1183", "claude:0faf0bb2#L1185"]
hook: "Chủ comment mà agent không dậy: budget chặn im lặng, không báo gì"
tension: cam_ma_van_lot
sides: ["Chủ comment để đánh thức agent", "Budget chặn bằng 409, giao diện không hiện thông báo nào"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Bộ dựng công ty một người chạy bằng đội agent AI, và sau khi đổi model, chủ comment vào issue để đánh thức agent làm lại việc. Chủ tưởng comment sẽ tạo run mới, nhưng budget đã chặn wake vì model không có giá tin cậy, và không có thông báo nào. Ai bật budget cho model chưa có bảng giá nên kiểm tra trước, nếu không agent sẽ đứng im mà không ai biết."
audience: dev xây hệ thống agent AI có budget
spine_context: "Bộ dựng công ty một người chạy bằng đội agent AI, nơi agent nhận việc qua issue và chủ duyệt các bước quan trọng."
spine_context_lines: [profile]
spine_want: Chủ comment vào issue để đánh thức agent làm lại việc sau khi đổi model.
spine_want_lines: ["claude:0faf0bb2#L1137", "claude:0faf0bb2#L1138"]
spine_obstacle: Comment không tạo run mới; lệnh wake trả 409 vì usage ghi nhận không có giá tin cậy.
spine_obstacle_lines: ["claude:0faf0bb2#L1160", "claude:0faf0bb2#L1170"]
spine_turn: Tưởng comment của chủ sẽ đánh thức agent; hoá ra budget chặn wake và không có thông báo nào.
spine_turn_lines: ["claude:0faf0bb2#L1137", "claude:0faf0bb2#L1160", "claude:0faf0bb2#L1170"]
spine_action: "Đặt budget của ba agent về 0, rồi resume agent và theo dõi run."
spine_action_lines: ["claude:0faf0bb2#L1174", "claude:0faf0bb2#L1184"]
spine_outcome: "Trạng thái agent chuyển từ paused (budget) sang running, run mới đang chạy."
spine_outcome_lines: ["claude:0faf0bb2#L1175", "claude:0faf0bb2#L1185"]
spine_takeaway: Bật budget cho model không có bảng giá có thể chặn agent mà không báo; kiểm tra giá trước khi bật budget.
spine_takeaway_lines: ["claude:0faf0bb2#L1170", "claude:0faf0bb2#L1175"]
completeness: 7
---

# Budget chặn agent im lặng: 409 'no reliable price' khiến comment của chủ không đánh thức được agent

**Góc kể:** Bộ dựng công ty một người chạy bằng đội agent AI, và sau khi đổi model, chủ comment vào issue để đánh thức agent làm lại việc. Chủ tưởng comment sẽ tạo run mới, nhưng budget đã chặn wake vì model không có giá tin cậy, và không có thông báo nào. Ai bật budget cho model chưa có bảng giá nên kiểm tra trước, nếu không agent sẽ đứng im mà không ai biết.
**Bối cảnh:** Sau khi agent Mai làm xong bản nháp, chủ comment để đánh thức lại agent nhưng không có run mới nào.
**Chuyện gì xảy ra:** Wake trả 409 vì model thuê bao không có giá nên hệ thống không tính được usage. Mình đặt budget của ba agent về 0, resume Mai, và trạng thái chuyển từ paused (budget) sang running trong khoảng 20 giây. Hệ thống chặn không có thông báo nào trên giao diện.
**Bài học:** Bật budget cho model không có bảng giá sẽ chặn agent mà không báo; kiểm tra giá trước khi bật budget.
**Artefact:** Bảng trạng thái agent trước và sau khi resume (paused budget, running).
