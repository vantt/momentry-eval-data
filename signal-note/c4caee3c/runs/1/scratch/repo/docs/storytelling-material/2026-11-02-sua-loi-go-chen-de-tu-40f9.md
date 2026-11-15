---
id: 2026-11-02-sua-loi-go-chen-de-tu-40f9
code: M-FBQB
aliases: [M-FBQB]
date: 2026-11-02
repo: repo
status: raw
signals: [khac, nguyen_nhan_bat_ngo]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L1458", "claude:c4caee3c#L1478"]
hook: "Bộ sửa lỗi gõ làm hỏng chính từ điển đồng nghĩa: 0,80 xuống 0,73"
tension: giup_ma_hai
sides: ["Sửa lỗi gõ cho người dùng", "Từ đúng bị đổi thành từ gần đó"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Gói Obsidian Hybrid Search tìm ghi chú trong kho Obsidian theo nghĩa và theo từ, và người làm đang gộp nhánh từ điển đồng nghĩa tiếng Việt vào master. Khi gộp, vi-synonym tụt từ 0,80 xuống 0,73 vì bộ sửa lỗi gõ chạy trước đã viết lại từ mà từ điển cần, nên từ điển không còn khớp. Sau khi cho từ điển khớp cả dạng người dùng gõ, điểm trở lại 0,80 và nDCG@5 tổng lên 0,909. Ai ghép một bước sửa đầu vào trước các bước khớp nên kiểm tra xem nó có đè lên các bước sau không."
audience: dev ghép nhiều bước xử lý truy vấn tìm kiếm
spine_context: "Gói npm Obsidian Hybrid Search tìm ghi chú trong kho Obsidian theo nghĩa và theo từ, cho người dùng Obsidian và agent AI. Người làm đang gộp các nhánh tính năng vào master."
spine_context_lines: [profile, "claude:c4caee3c#L1458"]
spine_want: "Gộp V18 (từ điển đồng nghĩa và viết tắt) vào master khi vi-synonym đạt ngưỡng 0,80."
spine_want_lines: ["claude:c4caee3c#L1458"]
spine_obstacle: Nhánh V18 xung đột ở 4 file khi gộp vào master.
spine_obstacle_lines: ["claude:c4caee3c#L1458"]
spine_turn: "Gộp tưởng là không ảnh hưởng gì tới từ điển; hoá ra bộ sửa lỗi gõ đã viết lại từ trước khi từ điển kịp khớp, nên vi-synonym tụt từ 0,80 xuống 0,73."
spine_turn_lines: ["claude:c4caee3c#L1458", "claude:c4caee3c#L1470"]
spine_action: Cho từ điển khớp cả dạng người dùng gõ gốc và dạng đã sửa; coi từ người dùng viết theo dạng từ điển là từ đã biết.
spine_action_lines: ["claude:c4caee3c#L1470"]
spine_outcome: "vi-synonym trở lại 0,80, vi-abbr đạt 1,00, nDCG@5 tổng từ 0,856 lên 0,909."
spine_outcome_lines: ["claude:c4caee3c#L1470", "claude:c4caee3c#L1478"]
spine_takeaway: "Khi chèn bước viết lại đầu vào, kiểm tra xem nó có đè lên các bước khớp sau không, và giữ cả dạng gốc để khớp."
spine_takeaway_lines: ["claude:c4caee3c#L1470"]
completeness: 7
---

# Sửa lỗi gõ chèn đè từ điển đồng nghĩa: vi-synonym tụt 0,80 xuống 0,73

**Góc kể:** Gói Obsidian Hybrid Search tìm ghi chú trong kho Obsidian theo nghĩa và theo từ, và người làm đang gộp nhánh từ điển đồng nghĩa tiếng Việt vào master. Khi gộp, vi-synonym tụt từ 0,80 xuống 0,73 vì bộ sửa lỗi gõ chạy trước đã viết lại từ mà từ điển cần, nên từ điển không còn khớp. Sau khi cho từ điển khớp cả dạng người dùng gõ, điểm trở lại 0,80 và nDCG@5 tổng lên 0,909. Ai ghép một bước sửa đầu vào trước các bước khớp nên kiểm tra xem nó có đè lên các bước sau không.
**Bối cảnh:** Sau khi merge nhánh gõ sai và nhánh từ điển, hạng mục đồng nghĩa tụt.
**Chuyện gì xảy ra:** Bộ sửa lỗi một ký tự đã viết lại từ mà từ điển đồng nghĩa cần, ví dụ một từ tiếng Anh bị đổi thành một từ gần đó trong vault. Nhánh từ điển giờ khớp cả dạng người dùng gõ, và từ người dùng viết theo dạng từ điển được coi là từ đã biết. Hạng mục trở lại 0,80.
**Bài học:** Khi chèn một bước viết lại đầu vào, kiểm tra xem nó có đè lên các bước khớp sau nó không.
**Artefact:** Bảng Hit@5 của vi-synonym trước và sau.
