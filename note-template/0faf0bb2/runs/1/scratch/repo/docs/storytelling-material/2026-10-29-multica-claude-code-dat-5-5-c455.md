---
id: 2026-10-29-multica-claude-code-dat-5-5-c455
code: M-5C6Q
aliases: [M-5C6Q]
date: 2026-10-29
repo: repo
status: raw
signals: [nguoi_duyet_may_soan, artefact_nhin_duoc]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L3492", "claude:0faf0bb2#L3540", "claude:0faf0bb2#L3556", "claude:0faf0bb2#L3622", "claude:0faf0bb2#L3629", "claude:0faf0bb2#L3671", "claude:0faf0bb2#L3691", "claude:0faf0bb2#L3702", "claude:0faf0bb2#L3712", "claude:0faf0bb2#L3725", "claude:0faf0bb2#L3747"]
hook: "Agent bị trả lại hai lần, và nó hỏi chủ thay vì bịa giá"
tension: nguoi_dung_may_sai
sides: ["Agent thường điền đại một con số để cho xong việc", "Nó dừng lại hỏi chủ giá và hạn chót, qua cột chỉ 16 giây"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: none
spine_context: "fgOPC là bộ dựng công ty một người vận hành bằng AI agent, chạy trên Multica tự host, đang thử nghiệm với runtime Claude Code."
spine_context_lines: [profile]
spine_want: "Spike Multica với Claude Code để kiểm năm tiêu chí: đúng vai, ghi ngược, tiếp nối session, workflow theo cột, chat nhiều phiên."
spine_want_lines: ["claude:0faf0bb2#L3398"]
spine_action: "Tạo agent Mai (Marketing), giao SEN-1 cho Mai kèm yêu cầu viết nội dung và chuyển sang in_review."
spine_action_lines: ["claude:0faf0bb2#L3492", "claude:0faf0bb2#L3493"]
spine_outcome: Đạt 5/5 tiêu chí; từ lúc chạy tới in_review mất 16 giây; không agent nào tự chuyển done.
spine_outcome_lines: ["claude:0faf0bb2#L3747"]
spine_takeaway: "Ràng buộc 'không tự done' hiện chỉ nằm trong chỉ dẫn, server chưa ép."
spine_takeaway_lines: ["claude:0faf0bb2#L3747"]
completeness: 5
---

# Multica + Claude Code đạt 5/5: issue đi qua cột, agent hỏi chủ thay vì bịa số

**Bối cảnh:** Spike thứ hai với Claude Code làm runtime, kiểm năm tiêu chí: đúng vai, ghi ngược, tiếp nối session, workflow theo cột, chat nhiều phiên.
**Chuyện gì xảy ra:** Issue tạo không có người nhận được tự giao cho agent viết nội dung, rồi sang cột duyệt và tự giao cho agent khác. Từ lúc chạy tới in_review chỉ mất 16 giây. Người duyệt trả lại hai lần: lần đầu vì thiếu giá, agent sửa nhưng để chỗ trống; lần hai agent dừng và hỏi chủ giá cùng hạn chót thay vì tự điền. Sau khi chủ trả lời, issue đi tiếp tới chờ chủ duyệt. Hai phiên chat với cùng một agent giữ hai session riêng và không lẫn thông tin. Không agent nào tự chuyển done, nhưng điều này mới nằm trong chỉ dẫn, server chưa ép.
**Bài học:** Workflow theo cột chạy được khi mỗi cột có người xử lý và chỉ dẫn rõ. Ràng buộc 'không tự done' phải nằm ở server, không chỉ trong prompt.
**Artefact:** Ảnh bảng workflow theo cột với issue đang chờ chủ duyệt. Che địa chỉ nội bộ và tên người.
