---
id: 2026-10-29-gr8r-dep-nhung-khong-license-de-c455
code: M-XXPR
aliases: [M-XXPR]
date: 2026-10-29
repo: repo
status: raw
signals: [dao_quyet_dinh, so_truoc_so_sau]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L413", "claude:0faf0bb2#L417", "claude:0faf0bb2#L435", "claude:0faf0bb2#L437", "claude:0faf0bb2#L3302"]
hook: "Đề xuất viết lại bị hỏi 'sao phải tốn công', và mình rút lại"
tension: tuong_ma_hoa_ra
sides: ["Tưởng không có thứ nào đủ gần, phải viết lại", "Paperclip MIT, 108k sao, đã làm gần đúng vision"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án là bộ dựng công ty một người chạy bằng đội agent AI, và người làm muốn có UI quản lý task giống gr8r. Vì gr8r không có license nên họ định viết UI mới, vì nghĩ không có gì đủ gần. Tìm kỹ thì có dự án MIT khoảng 108k sao làm đúng việc cần, và web của Kaneo đã có tiếng Việt, nối API thật, đáng làm nền hơn. Ai phải chọn nền UI trước khi viết lại nên đọc chuyện này."
audience: dev dùng AI đang chọn nền UI hoặc cân nhắc viết lại
spine_context: Bộ dựng công ty một người chạy bằng đội agent AI; đang chọn UI để quản lý project và task.
spine_context_lines: [profile, "claude:0faf0bb2#L257"]
spine_want: "Muốn có UI quản lý project/task/comment giống gr8r, chi phí thấp, chạy trên Cloudflare."
spine_want_lines: ["claude:0faf0bb2#L257"]
spine_obstacle: "gr8r không có license nên không copy code được, và chỉ là bản demo frontend."
spine_obstacle_lines: ["claude:0faf0bb2#L417"]
spine_turn: Tưởng phải viết UI mới vì gr8r không dùng được và không có nền nào đủ gần; hoá ra có dự án MIT khoảng 108k sao làm đúng việc đang cần.
spine_turn_lines: ["claude:0faf0bb2#L417", "claude:0faf0bb2#L435", "claude:0faf0bb2#L437"]
spine_action: "Tìm các dự án sẵn có có license dùng được, rồi kiểm tra từng ứng viên."
spine_action_lines: ["claude:0faf0bb2#L419", "claude:0faf0bb2#L432", "claude:0faf0bb2#L438"]
spine_outcome: Đề xuất lấy web của Kaneo làm nền và mượn màn hình từ Circle; Kaneo đã có tiếng Việt và nối API thật.
spine_outcome_lines: ["claude:0faf0bb2#L3290"]
spine_takeaway: "Trước khi đề xuất viết lại, tìm xem có dự án sẵn dùng được không; thiết kế đẹp không thay được license."
spine_takeaway_lines: ["claude:0faf0bb2#L3302"]
completeness: 7
---

# gr8r đẹp nhưng không license; đề xuất viết lại bị chủ hỏi lại và Paperclip được tìm thấy

**Góc kể:** Dự án là bộ dựng công ty một người chạy bằng đội agent AI, và người làm muốn có UI quản lý task giống gr8r. Vì gr8r không có license nên họ định viết UI mới, vì nghĩ không có gì đủ gần. Tìm kỹ thì có dự án MIT khoảng 108k sao làm đúng việc cần, và web của Kaneo đã có tiếng Việt, nối API thật, đáng làm nền hơn. Ai phải chọn nền UI trước khi viết lại nên đọc chuyện này.
**Bối cảnh:** Mình đề xuất viết lại UI vì gr8r không có license và chỉ là bản demo frontend.
**Chuyện gì xảy ra:** Chủ hỏi tại sao phải viết lại vì tốn công. Tìm lại thì Paperclip có giấy phép MIT, khoảng 108k sao, làm gần đúng vision, và mình rút lại đề xuất. Đánh giá sau cùng: gr8r thắng về thiết kế nhưng thua về license, backend, i18n và hệ sinh thái component.
**Bài học:** Trước khi đề xuất viết lại, tìm xem có dự án sẵn dùng được không; chất lượng thiết kế không thay được license.
**Artefact:** Bảng so sánh gr8r, Circle và Kaneo.
