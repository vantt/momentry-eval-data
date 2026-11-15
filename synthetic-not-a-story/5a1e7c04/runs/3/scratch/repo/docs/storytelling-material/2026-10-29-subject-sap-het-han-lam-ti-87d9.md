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
hook: "Subject 'còn 3 tiếng' tăng mở 9 điểm, hủy tăng gấp 5"
tension: giup_ma_hai
sides: ["Subject giả hạn chót kéo tỉ lệ mở từ 40% lên 50%", "Hủy đăng ký tăng 5 lần, có khiếu nại spam, click không đổi"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Subject 'sắp hết hạn' làm tỉ lệ mở tăng, nhưng hủy đăng ký tăng 5 lần và bị khiếu nại

**Bối cảnh:** Hai email trước dùng subject kiểu 'Last chance' và 'Final call' theo gợi ý của agent. Người dùng muốn dùng lại phong cách này cho email ra mắt.
**Chuyện gì xảy ra:** Tỉ lệ mở tăng khoảng 9 điểm, từ khoảng 40% lên 50%. Nhưng tỉ lệ hủy đăng ký tăng từ khoảng 0,2% lên 1,0%, ước tính khoảng 190 người trên danh sách 9.800. Có 2 khiếu nại spam, trong khi các email trước không có. Tỉ lệ click gần như không đổi (3,4% và 3,0% so với 3,1% và 2,9%). Email 3 nói 'còn 3 tiếng' nhưng pre-order vẫn mở. Inbox nhận 6 phản hồi, trong đó có một người viết rằng hôm qua vẫn nói còn 3 tiếng. Quyết định: dùng subject không có deadline giả, và thêm luật vào email-rules. Luật là không dùng deadline trừ khi có thật, và kiểm tra hủy đăng ký cùng khiếu nại song song với tỉ lệ mở.
**Bài học:** Đừng tối ưu chỉ theo tỉ lệ mở. Deadline giả làm tăng lượt mở nhưng làm mất niềm tin, tăng hủy đăng ký và khiếu nại spam.
**Artefact:** Bảng so sánh tỉ lệ mở, click, hủy đăng ký và spam trước và sau. Che tên email và danh sách người nhận.
**Góc người ngoài:** cách làm phổ biến là Bảo vệ gợi ý cũ, hoặc chỉ đổi âm thầm mà không giải thích vì sao sai; ở đây khác ở Nhận sai ngắn gọn, không biện hộ, và đưa phương án thay thế cụ thể. Người đọc muốn thấy cách phản hồi khi AI đưa ra gợi ý sai.
