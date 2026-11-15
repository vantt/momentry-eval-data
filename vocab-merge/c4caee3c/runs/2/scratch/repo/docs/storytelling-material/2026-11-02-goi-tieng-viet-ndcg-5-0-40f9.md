---
id: 2026-11-02-goi-tieng-viet-ndcg-5-0-40f9
code: M-GD81
aliases: [M-GD81]
date: 2026-11-02
repo: repo
status: raw
signals: [số trước sau, nguyên nhân bất ngờ]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L1138", "claude:c4caee3c#L1274", "claude:c4caee3c#L1283", "claude:c4caee3c#L1445", "claude:c4caee3c#L1470", "claude:c4caee3c#L1952", "claude:c4caee3c#L2187"]
hook: "Thêm lớp sửa gõ sai, lớp đó phá chính lớp từ đồng nghĩa trước"
tension: giup_ma_hai
sides: ["lớp sửa gõ sai giúp tìm tốt hơn", "nó viết lại từ đồng nghĩa, hạng 4 tụt xuống 7"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Gói tiếng Việt: nDCG@5 0,666 lên 0,932 qua nhiều lớp, và một lớp làm hỏng lớp trước

**Bối cảnh:** Gói được thêm từng lớp: chuẩn hoá, bỏ dấu, phục hồi dấu, Telex, sửa gõ sai, từ đồng nghĩa, viết tắt, alias.
**Chuyện gì xảy ra:** Lớp V13 đưa tổng từ 0,666 lên 0,813, Hit@1 của alias từ 0,60 lên 0,93, vi-unaccented từ 0,133 lên 0,951. Lớp sửa gõ sai viết lại các từ đã có trong từ điển đồng nghĩa, làm vi-synonym Hit@5 tụt xuống 0,73 (hạng 4 thành hạng 7). Sửa: lexicon đọc cả câu gốc lẫn câu đã sửa, và từ người dùng gõ theo dạng đồng nghĩa được coi là từ đã biết.
**Bài học:** Khi hai lớp cùng sửa một câu, lớp sau phải thấy được dạng gốc của lớp trước; đo lại toàn bộ hạng mục sau mỗi lần merge.
**Artefact:** Bảng nDCG@5 theo từng lớp, các hạng mục giữ nguyên.
