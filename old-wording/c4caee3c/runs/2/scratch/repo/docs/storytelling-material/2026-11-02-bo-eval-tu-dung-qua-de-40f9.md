---
id: 2026-11-02-bo-eval-tu-dung-qua-de-40f9
code: M-6M4F
aliases: [M-6M4F]
date: 2026-11-02
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L315", "claude:c4caee3c#L334", "claude:c4caee3c#L1044", "claude:c4caee3c#L1150", "claude:c4caee3c#L1264", "claude:c4caee3c#L2187"]
hook: "Bộ đo dễ quá nên mục tiêu bất khả thi: baseline đã 0,93"
tension: tuong_ma_hoa_ra
sides: ["Baseline 0,93 tưởng là tốt, nên mục tiêu gấp đôi là bất khả thi", "Làm khó bộ đo xuống 0,27 thì gói tiếng Việt mới đạt 1,00"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Obsidian Hybrid Search là công cụ tìm kiếm cho vault Obsidian chạy local, và người làm đang thêm gói tiếng Việt cho nó. Ban đầu bộ eval tự dựng được tin là đủ khó, nhưng baseline upstream đã đạt Hit@5 0,93, khiến mục tiêu gấp đôi không thể đạt. Thay vì hạ ngưỡng, người làm làm khó corpus: baseline rơi xuống 0,27 và 0,40, rồi gói tiếng Việt đưa cả hai lên 1,00. Ai đặt ngưỡng cho bộ đo tìm kiếm nên kiểm tra baseline trước."
audience: dev xây bộ đo hoặc đặt ngưỡng chất lượng cho công cụ tìm kiếm
spine_context: Obsidian Hybrid Search là công cụ tìm kiếm cho vault Obsidian chạy local; người làm đang thêm gói tiếng Việt cho nó.
spine_context_lines: [profile, "claude:c4caee3c#L11"]
spine_want: "Đạt Hit@5 ≥ 0,85 và gấp tối thiểu 2 lần baseline upstream (điều kiện G3)."
spine_want_lines: ["claude:c4caee3c#L315"]
spine_obstacle: "Baseline upstream đã đạt Hit@5 0,93 (vi-unaccented) và 0,87 (vi-dd), nên điều kiện gấp đôi không thể đạt."
spine_obstacle_lines: ["claude:c4caee3c#L315"]
spine_turn: "Bộ eval tự dựng được tin là đủ khó để đo gói; hoá ra baseline đã đạt 0,93, nên bộ đo quá dễ."
spine_turn_lines: ["claude:c4caee3c#L315"]
spine_action: Người dùng chọn làm khó corpus thay vì hạ ngưỡng; người làm dựng lại corpus khó hơn.
spine_action_lines: ["claude:c4caee3c#L334", "claude:c4caee3c#L1044"]
spine_outcome: "Baseline rơi xuống 0,27 và 0,40; sau gói tiếng Việt cả hai đạt 1,00, và nDCG@5 tổng tăng từ 0,666 lên 0,932."
spine_outcome_lines: ["claude:c4caee3c#L1150", "claude:c4caee3c#L2187"]
spine_takeaway: "Khi mục tiêu không đạt vì bộ đo quá dễ, sửa bộ đo trước khi hạ ngưỡng, rồi đo lại baseline trên bộ mới."
spine_takeaway_lines: ["claude:c4caee3c#L334"]
completeness: 7
---

# Bộ eval tự dựng quá dễ: baseline 0,93 khiến mục tiêu không thể đạt, nên làm khó bộ đo

**Góc kể:** Obsidian Hybrid Search là công cụ tìm kiếm cho vault Obsidian chạy local, và người làm đang thêm gói tiếng Việt cho nó. Ban đầu bộ eval tự dựng được tin là đủ khó, nhưng baseline upstream đã đạt Hit@5 0,93, khiến mục tiêu gấp đôi không thể đạt. Thay vì hạ ngưỡng, người làm làm khó corpus: baseline rơi xuống 0,27 và 0,40, rồi gói tiếng Việt đưa cả hai lên 1,00. Ai đặt ngưỡng cho bộ đo tìm kiếm nên kiểm tra baseline trước.
**Bối cảnh:** Corpus sinh có note trùng tiêu đề với câu tìm, nên vector và nhánh title tìm ra note dù FTS5 không bỏ dấu được.
**Chuyện gì xảy ra:** Baseline upstream đạt Hit@5 0,93 với vi-unaccented và 0,87 với vi-dd, nên điều kiện gấp đôi baseline không thể đạt. Người dùng chọn làm khó corpus chứ không hạ ngưỡng, và baseline xuống 0,27 và 0,40. Sau gói tiếng Việt, cả hai lên 1,00, và nDCG@5 tổng từ 0,666 lên 0,932 mà không hạng mục nào tụt.
**Bài học:** Khi mục tiêu không đạt được vì bộ đo quá dễ, sửa bộ đo trước khi nghĩ đến hạ ngưỡng, và đo lại baseline trên bộ mới.
**Artefact:** Bảng Hit@5 theo hạng mục trước và sau, không kèm câu hỏi.
