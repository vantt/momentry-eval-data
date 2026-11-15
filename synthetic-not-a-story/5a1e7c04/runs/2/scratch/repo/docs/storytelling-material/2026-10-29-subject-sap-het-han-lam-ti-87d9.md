---
id: 2026-10-29-subject-sap-het-han-lam-ti-87d9
code: M-XZX0
aliases: [M-XZX0]
date: 2026-10-29
repo: repo
status: raw
signals: [khac, dao_quyet_dinh, nguyen_nhan_bat_ngo]
source: "chat Claude, claude:5a1e7c04"
sessions: ["claude:5a1e7c04"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:5a1e7c04#L26", "claude:5a1e7c04#L27", "claude:5a1e7c04#L28", "claude:5a1e7c04#L29", "claude:5a1e7c04#L30", "claude:5a1e7c04#L31", "claude:5a1e7c04#L32", "claude:5a1e7c04#L33"]
hook: "Subject 'sắp hết hạn' tăng mở 9 điểm, nhưng hủy đăng ký tăng gấp 5"
tension: giup_ma_hai
sides: ["Dùng deadline giả để tăng tỉ lệ mở từ 40% lên 50%", "Hủy đăng ký từ 0,2% lên 1,0% (~190 người), 2 khiếu nại spam, click không đổi"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Người làm marketing cho serum vitamin C đang chuẩn bị email ra mắt. Họ muốn dùng lại kiểu subject 'sắp hết hạn' vì hai email trước làm tỉ lệ mở tăng khoảng 9 điểm, và tin rằng đó là điểm cộng. Hoá ra cái giá là hủy đăng ký tăng khoảng 5 lần, 2 khiếu nại spam, và một khách nói thẳng 'hôm qua bạn vẫn nói còn 3 tiếng'. Ai dùng deadline trong email nên đo cả hủy đăng ký và khiếu nại, không chỉ tỉ lệ mở."
audience: người làm email marketing dùng AI để viết subject
spine_context: "Người làm marketing cho serum vitamin C đang chuẩn bị tuần ra mắt, email ra mắt gửi vào tối mai."
spine_context_lines: ["claude:5a1e7c04#L1"]
spine_want: "Muốn email ra mắt được mở nhiều hơn, nên định dùng lại kiểu subject đã làm tỉ lệ mở tăng."
spine_want_lines: ["claude:5a1e7c04#L26"]
spine_obstacle: Email 3 nói 'còn 3 tiếng' nhưng pre-order vẫn mở.
spine_obstacle_lines: ["claude:5a1e7c04#L29"]
spine_turn: Tưởng subject kiểu hết hạn là cách tăng tỉ lệ mở an toàn; hoá ra hủy đăng ký tăng khoảng 5 lần và có 2 khiếu nại spam.
spine_turn_lines: ["claude:5a1e7c04#L26", "claude:5a1e7c04#L29"]
spine_action: "Chọn subject không có deadline giả cho email ra mắt và thêm luật vào email-rules.md: chỉ dùng deadline khi có thật, và đo cả hủy đăng ký lẫn khiếu nại."
spine_action_lines: ["claude:5a1e7c04#L32", "claude:5a1e7c04#L33"]
spine_outcome: "Email ra mắt dùng 'Brightness, bottled. Now live.'; luật đã được ghi vào file. Chưa có số liệu kết quả của email ra mắt."
spine_outcome_lines: ["claude:5a1e7c04#L32", "claude:5a1e7c04#L34"]
spine_takeaway: "Đừng tối ưu chỉ theo tỉ lệ mở: deadline giả có thể tăng lượt mở nhưng làm tăng hủy đăng ký và khiếu nại."
spine_takeaway_lines: ["claude:5a1e7c04#L29", "claude:5a1e7c04#L30"]
completeness: 7
---

# Subject 'sắp hết hạn' làm tỉ lệ mở tăng, nhưng hủy đăng ký tăng 5 lần và bị khiếu nại

**Góc kể:** Người làm marketing cho serum vitamin C đang chuẩn bị email ra mắt. Họ muốn dùng lại kiểu subject 'sắp hết hạn' vì hai email trước làm tỉ lệ mở tăng khoảng 9 điểm, và tin rằng đó là điểm cộng. Hoá ra cái giá là hủy đăng ký tăng khoảng 5 lần, 2 khiếu nại spam, và một khách nói thẳng 'hôm qua bạn vẫn nói còn 3 tiếng'. Ai dùng deadline trong email nên đo cả hủy đăng ký và khiếu nại, không chỉ tỉ lệ mở.
**Bối cảnh:** Hai email trước dùng subject kiểu 'Last chance' và 'Final call' theo gợi ý của agent. Người dùng muốn dùng lại phong cách này cho email ra mắt.
**Chuyện gì xảy ra:** Tỉ lệ mở tăng khoảng 9 điểm, từ khoảng 40% lên 50%. Nhưng tỉ lệ hủy đăng ký tăng từ khoảng 0,2% lên 1,0%, ước tính khoảng 190 người trên danh sách 9.800. Có 2 khiếu nại spam, trong khi các email trước không có. Tỉ lệ click gần như không đổi (3,4% và 3,0% so với 3,1% và 2,9%). Email 3 nói 'còn 3 tiếng' nhưng pre-order vẫn mở. Inbox nhận 6 phản hồi, trong đó có một người viết rằng hôm qua vẫn nói còn 3 tiếng. Quyết định: dùng subject không có deadline giả, và thêm luật vào email-rules. Luật là không dùng deadline trừ khi có thật, và kiểm tra hủy đăng ký cùng khiếu nại song song với tỉ lệ mở.
**Bài học:** Đừng tối ưu chỉ theo tỉ lệ mở. Deadline giả làm tăng lượt mở nhưng làm mất niềm tin, tăng hủy đăng ký và khiếu nại spam.
**Artefact:** Bảng so sánh tỉ lệ mở, click, hủy đăng ký và spam trước và sau. Che tên email và danh sách người nhận.
**Góc người ngoài:** cách làm phổ biến là Bảo vệ gợi ý cũ, hoặc chỉ đổi âm thầm mà không giải thích vì sao sai; ở đây khác ở Nhận sai ngắn gọn, không biện hộ, và đưa phương án thay thế cụ thể. Người đọc muốn thấy cách phản hồi khi AI đưa ra gợi ý sai.
