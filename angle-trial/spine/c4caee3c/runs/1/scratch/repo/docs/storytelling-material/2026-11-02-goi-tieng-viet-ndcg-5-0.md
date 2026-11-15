---
id: 2026-11-02-goi-tieng-viet-ndcg-5-0
date: 2026-11-02
repo: repo
status: raw
signals: [số trước sau, nguyên nhân bất ngờ]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L1138", "claude:c4caee3c#L1274", "claude:c4caee3c#L1283", "claude:c4caee3c#L1445", "claude:c4caee3c#L1470", "claude:c4caee3c#L1952", "claude:c4caee3c#L2187"]
hook: "Lớp sửa gõ sai làm hỏng lớp từ đồng nghĩa: hạng 4 thành hạng 7"
tension: hop_ma_tan
sides: ["Thêm lớp sửa gõ sai để tìm tốt hơn", "Nó viết lại từ đồng nghĩa, vi-synonym tụt hạng 4 xuống 7"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một nhóm đang làm bản fork của Obsidian Hybrid Search, công cụ tìm ghi chú Obsidian theo nghĩa, và thêm gói tiếng Việt để tìm đúng cả khi gõ không dấu, gõ sai hay dùng từ đồng nghĩa. Họ tin lớp sửa gõ sai chỉ làm kết quả tốt hơn, nhưng sau khi merge, lớp này đã viết lại các từ trong từ điển đồng nghĩa, kéo vi-synonym từ hạng 4 xuống hạng 7. Ai xếp nhiều lớp xử lý văn bản lên cùng một câu hỏi đều có thể gặp đúng lỗi này, vì lớp sau che mất dạng gốc mà lớp trước cần."
audience: dev xây công cụ tìm kiếm hoặc xử lý ngôn ngữ nhiều lớp
spine_context: "Một nhóm làm bản fork của Obsidian Hybrid Search, công cụ tìm ghi chú Obsidian theo nghĩa, và đang thêm gói tiếng Việt để tìm đúng khi gõ không dấu, gõ sai hay dùng từ đồng nghĩa."
spine_context_lines: [profile, "claude:c4caee3c#L11"]
spine_want: "Muốn hoàn tất plan roadmap fork, trong đó gói tiếng Việt phải đạt các mục tiêu G3."
spine_want_lines: ["claude:c4caee3c#L11", "claude:c4caee3c#L1150"]
spine_obstacle: "Các lớp xử lý cùng sửa một câu, nên lớp sau có thể che mất dạng gốc mà lớp trước cần."
spine_obstacle_lines: ["claude:c4caee3c#L1470"]
spine_turn: "Tưởng lớp sửa gõ sai chỉ làm kết quả tốt hơn; hoá ra nó viết lại các từ trong từ điển đồng nghĩa, kéo vi-synonym từ hạng 4 xuống hạng 7."
spine_turn_lines: ["claude:c4caee3c#L1458", "claude:c4caee3c#L1470"]
spine_action: Lexicon đọc cả câu gốc lẫn câu đã sửa; từ người dùng gõ theo dạng đồng nghĩa được coi là từ đã biết; thêm test.
spine_action_lines: ["claude:c4caee3c#L1470"]
spine_outcome: "vi-synonym Hit@5 lên 0,80, vi-abbr đạt 1,00, nDCG@5 tổng lên 0,909, không hạng mục nào tụt."
spine_outcome_lines: ["claude:c4caee3c#L1478"]
spine_takeaway: "Khi hai lớp cùng sửa một câu, lớp sau phải thấy dạng gốc của lớp trước; đo lại toàn bộ hạng mục sau mỗi lần merge."
spine_takeaway_lines: ["claude:c4caee3c#L1470"]
completeness: 7
---

# Gói tiếng Việt: nDCG@5 0,666 lên 0,932 qua nhiều lớp, và một lớp làm hỏng lớp trước

**Góc kể:** Một nhóm đang làm bản fork của Obsidian Hybrid Search, công cụ tìm ghi chú Obsidian theo nghĩa, và thêm gói tiếng Việt để tìm đúng cả khi gõ không dấu, gõ sai hay dùng từ đồng nghĩa. Họ tin lớp sửa gõ sai chỉ làm kết quả tốt hơn, nhưng sau khi merge, lớp này đã viết lại các từ trong từ điển đồng nghĩa, kéo vi-synonym từ hạng 4 xuống hạng 7. Ai xếp nhiều lớp xử lý văn bản lên cùng một câu hỏi đều có thể gặp đúng lỗi này, vì lớp sau che mất dạng gốc mà lớp trước cần.
**Bối cảnh:** Gói được thêm từng lớp: chuẩn hoá, bỏ dấu, phục hồi dấu, Telex, sửa gõ sai, từ đồng nghĩa, viết tắt, alias.
**Chuyện gì xảy ra:** Lớp V13 đưa tổng từ 0,666 lên 0,813, Hit@1 của alias từ 0,60 lên 0,93, vi-unaccented từ 0,133 lên 0,951. Lớp sửa gõ sai viết lại các từ đã có trong từ điển đồng nghĩa, làm vi-synonym Hit@5 tụt xuống 0,73 (hạng 4 thành hạng 7). Sửa: lexicon đọc cả câu gốc lẫn câu đã sửa, và từ người dùng gõ theo dạng đồng nghĩa được coi là từ đã biết.
**Bài học:** Khi hai lớp cùng sửa một câu, lớp sau phải thấy được dạng gốc của lớp trước; đo lại toàn bộ hạng mục sau mỗi lần merge.
**Artefact:** Bảng nDCG@5 theo từng lớp, các hạng mục giữ nguyên.
