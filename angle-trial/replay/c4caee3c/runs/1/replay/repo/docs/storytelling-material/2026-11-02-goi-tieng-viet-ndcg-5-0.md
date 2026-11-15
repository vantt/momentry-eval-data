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
angle: "Người làm tin rằng thêm lớp sửa gõ sai sẽ giúp tìm tốt hơn. Nhưng lớp này viết lại truy vấn trước khi lớp từ đồng nghĩa kịp đọc, nên một từ đồng nghĩa người dùng gõ bị đổi thành từ khác trong kho ghi chú, và ghi chú đúng tụt từ hạng 4 xuống hạng 7. Ai xếp nhiều lớp xử lý truy vấn cần kiểm tra lớp sau có thấy dạng gốc mà người dùng gõ hay không."
audience: dev làm tìm kiếm cho ghi chú tiếng Việt hoặc xếp nhiều lớp xử lý truy vấn
---

# Gói tiếng Việt: nDCG@5 0,666 lên 0,932 qua nhiều lớp, và một lớp làm hỏng lớp trước

**Góc kể:** Người làm tin rằng thêm lớp sửa gõ sai sẽ giúp tìm tốt hơn. Nhưng lớp này viết lại truy vấn trước khi lớp từ đồng nghĩa kịp đọc, nên một từ đồng nghĩa người dùng gõ bị đổi thành từ khác trong kho ghi chú, và ghi chú đúng tụt từ hạng 4 xuống hạng 7. Ai xếp nhiều lớp xử lý truy vấn cần kiểm tra lớp sau có thấy dạng gốc mà người dùng gõ hay không.
**Bối cảnh:** Gói được thêm từng lớp: chuẩn hoá, bỏ dấu, phục hồi dấu, Telex, sửa gõ sai, từ đồng nghĩa, viết tắt, alias.
**Chuyện gì xảy ra:** Lớp V13 đưa tổng từ 0,666 lên 0,813, Hit@1 của alias từ 0,60 lên 0,93, vi-unaccented từ 0,133 lên 0,951. Lớp sửa gõ sai viết lại các từ đã có trong từ điển đồng nghĩa, làm vi-synonym Hit@5 tụt xuống 0,73 (hạng 4 thành hạng 7). Sửa: lexicon đọc cả câu gốc lẫn câu đã sửa, và từ người dùng gõ theo dạng đồng nghĩa được coi là từ đã biết.
**Bài học:** Khi hai lớp cùng sửa một câu, lớp sau phải thấy được dạng gốc của lớp trước; đo lại toàn bộ hạng mục sau mỗi lần merge.
**Artefact:** Bảng nDCG@5 theo từng lớp, các hạng mục giữ nguyên.
