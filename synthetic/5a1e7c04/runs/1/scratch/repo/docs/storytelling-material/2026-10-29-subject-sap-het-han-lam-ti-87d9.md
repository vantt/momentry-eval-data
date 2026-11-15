---
id: 2026-10-29-subject-sap-het-han-lam-ti-87d9
code: M-XZX0
aliases: [M-XZX0]
date: 2026-10-29
repo: repo
status: raw
signals: [số trước-sau, đảo quyết định, nguyên nhân bất ngờ]
source: "chat Claude, claude:5a1e7c04"
sessions: ["claude:5a1e7c04"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:5a1e7c04#L26", "claude:5a1e7c04#L27", "claude:5a1e7c04#L28", "claude:5a1e7c04#L29", "claude:5a1e7c04#L30", "claude:5a1e7c04#L31", "claude:5a1e7c04#L32", "claude:5a1e7c04#L33"]
hook: "Email 'còn 3 tiếng' tăng 9 điểm lượt mở, hủy đăng ký tăng gấp 5"
tension: giup_ma_hai
sides: ["lượt mở tăng từ 40% lên 50%", "hủy đăng ký tăng từ 0,2% lên 1,0%, có 2 khiếu nại spam"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một đội đang chuẩn bị tuần ra mắt serum vitamin C, email ra mắt gửi vào tối hôm sau. Họ tin rằng subject kiểu 'còn 3 tiếng' làm tỉ lệ mở tăng là dấu hiệu tốt, và định dùng lại cho email ra mắt. Tỉ lệ mở đúng là tăng khoảng 9 điểm, nhưng hủy đăng ký tăng gần 5 lần, có khiếu nại spam, và một khách viết rằng hôm qua vẫn nghe còn 3 tiếng. Ai dùng AI để tối ưu chỉ số email nên xem kỹ chuyện này."
audience: người làm email marketing và dev dùng AI để tối ưu chỉ số
spine_context: "Một đội chuẩn bị tuần ra mắt serum vitamin C, email ra mắt gửi vào tối hôm sau."
spine_context_lines: ["claude:5a1e7c04#L1"]
spine_want: Muốn dùng lại kiểu subject gây gấp gáp đã làm tỉ lệ mở tăng ở hai email trước.
spine_want_lines: ["claude:5a1e7c04#L26"]
spine_obstacle: "Email 3 nói 'Last chance' nhưng pre-order vẫn mở, và khách bắt đầu nhận ra."
spine_obstacle_lines: ["claude:5a1e7c04#L29", "claude:5a1e7c04#L30"]
spine_turn: "Tưởng tỉ lệ mở tăng là dấu hiệu tốt; hoá ra hủy đăng ký tăng gần 5 lần và có khiếu nại spam, còn tỉ lệ click gần như không đổi."
spine_turn_lines: ["claude:5a1e7c04#L26", "claude:5a1e7c04#L29"]
spine_action: "Chọn subject không có deadline giả và thêm luật vào email-rules: chỉ dùng deadline khi có thật, và theo dõi hủy đăng ký cùng khiếu nại song song với tỉ lệ mở."
spine_action_lines: ["claude:5a1e7c04#L31", "claude:5a1e7c04#L32", "claude:5a1e7c04#L34"]
spine_takeaway: Đừng tối ưu chỉ theo tỉ lệ mở; deadline giả tăng lượt mở nhưng làm mất niềm tin.
spine_takeaway_lines: ["claude:5a1e7c04#L29", "claude:5a1e7c04#L31"]
completeness: 6
---

# Subject 'sắp hết hạn' làm tỉ lệ mở tăng, nhưng hủy đăng ký tăng 5 lần và bị khiếu nại

**Góc kể:** Một đội đang chuẩn bị tuần ra mắt serum vitamin C, email ra mắt gửi vào tối hôm sau. Họ tin rằng subject kiểu 'còn 3 tiếng' làm tỉ lệ mở tăng là dấu hiệu tốt, và định dùng lại cho email ra mắt. Tỉ lệ mở đúng là tăng khoảng 9 điểm, nhưng hủy đăng ký tăng gần 5 lần, có khiếu nại spam, và một khách viết rằng hôm qua vẫn nghe còn 3 tiếng. Ai dùng AI để tối ưu chỉ số email nên xem kỹ chuyện này.
**Bối cảnh:** Hai email trước dùng subject kiểu 'Last chance' và 'Final call' theo gợi ý của agent. Người dùng muốn dùng lại phong cách này cho email ra mắt.
**Chuyện gì xảy ra:** Tỉ lệ mở tăng khoảng 9 điểm, từ khoảng 40% lên 50%. Nhưng tỉ lệ hủy đăng ký tăng từ khoảng 0,2% lên 1,0%, ước tính khoảng 190 người trên danh sách 9.800. Có 2 khiếu nại spam, trong khi các email trước không có. Tỉ lệ click gần như không đổi (3,4% và 3,0% so với 3,1% và 2,9%). Email 3 nói 'còn 3 tiếng' nhưng pre-order vẫn mở. Inbox nhận 6 phản hồi, trong đó có một người viết rằng hôm qua vẫn nói còn 3 tiếng. Quyết định: dùng subject không có deadline giả, và thêm luật vào email-rules. Luật là không dùng deadline trừ khi có thật, và kiểm tra hủy đăng ký cùng khiếu nại song song với tỉ lệ mở.
**Bài học:** Đừng tối ưu chỉ theo tỉ lệ mở. Deadline giả làm tăng lượt mở nhưng làm mất niềm tin, tăng hủy đăng ký và khiếu nại spam.
**Artefact:** Bảng so sánh tỉ lệ mở, click, hủy đăng ký và spam trước và sau. Che tên email và danh sách người nhận.
**Góc người ngoài:** cách làm phổ biến là Bảo vệ gợi ý cũ, hoặc chỉ đổi âm thầm mà không giải thích vì sao sai; ở đây khác ở Nhận sai ngắn gọn, không biện hộ, và đưa phương án thay thế cụ thể. Người đọc muốn thấy cách phản hồi khi AI đưa ra gợi ý sai.
