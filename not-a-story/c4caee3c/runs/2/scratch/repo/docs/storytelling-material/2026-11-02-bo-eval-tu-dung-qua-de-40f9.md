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
hook: "Baseline 0,93 làm mục tiêu bbất khả: họ làm khó đề thi"
tension: tuong_ma_hoa_ra
sides: ["Tưởng bộ đo đủ khó, mục tiêu gấp đôi sẽ đạt được", "Baseline đã 0,93 nên gấp đôi là không thể; hạ đề xuống 0,27"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Obsidian Hybrid Search là công cụ tìm kiếm chạy cục bộ trên vault Obsidian, và nhóm đang thêm gói tiếng Việt cho nó với mục tiêu Hit@5 ít nhất 0,85 và gấp đôi baseline. Baseline upstream đã đạt 0,93 trên bộ đo tự dựng, nên gấp đôi là không thể, tức bộ đo quá dễ vì mỗi câu tìm trùng tiêu đề note. Nhóm chọn làm khó bộ đo thay vì hạ ngưỡng; baseline xuống 0,27 và 0,40, và gói tiếng Việt đưa cả hai lên 1,00. Ai tự dựng bộ đo để đánh giá search đều có thể rơi vào cùng cái bẫy này."
audience: dev làm công cụ tìm kiếm và đánh giá chất lượng bằng bộ đo tự dựng
spine_context: "Nhóm đang thêm gói tiếng Việt cho Obsidian Hybrid Search, công cụ tìm kiếm chạy cục bộ trên vault Obsidian."
spine_context_lines: [profile]
spine_want: "Đạt mục tiêu G3: Hit@5 ít nhất 0,85 và gấp tối thiểu 2 lần baseline."
spine_want_lines: ["claude:c4caee3c#L315"]
spine_obstacle: "Baseline upstream đã đạt Hit@5 0,93 với vi-unaccented và 0,87 với vi-dd, nên mục tiêu gấp đôi không thể đạt."
spine_obstacle_lines: ["claude:c4caee3c#L315"]
spine_turn: "Tưởng bộ đo đủ khó để mục tiêu gấp đôi có ý nghĩa; hoá ra bộ đo quá dễ, vì mỗi câu tìm trùng tiêu đề note nên baseline đã cao sẵn."
spine_turn_lines: ["claude:c4caee3c#L315", "claude:c4caee3c#L1034"]
spine_action: "Làm khó bộ đo tiếng Việt thay vì hạ ngưỡng, rồi đo lại baseline trên bộ mới."
spine_action_lines: ["claude:c4caee3c#L334", "claude:c4caee3c#L1034"]
spine_outcome: "Baseline xuống 0,27 và 0,40; sau gói tiếng Việt cả hai đạt 1,00, nDCG@5 tổng tăng từ 0,666 lên 0,932 và không hạng mục nào tụt."
spine_outcome_lines: ["claude:c4caee3c#L1034", "claude:c4caee3c#L1150", "claude:c4caee3c#L2187"]
spine_takeaway: "Khi mục tiêu không đạt vì bộ đo quá dễ, sửa bộ đo trước khi hạ ngưỡng, rồi đo lại baseline trên bộ mới."
spine_takeaway_lines: ["claude:c4caee3c#L334", "claude:c4caee3c#L1034"]
completeness: 7
---

# Bộ eval tự dựng quá dễ: baseline 0,93 khiến mục tiêu không thể đạt, nên làm khó bộ đo

**Góc kể:** Obsidian Hybrid Search là công cụ tìm kiếm chạy cục bộ trên vault Obsidian, và nhóm đang thêm gói tiếng Việt cho nó với mục tiêu Hit@5 ít nhất 0,85 và gấp đôi baseline. Baseline upstream đã đạt 0,93 trên bộ đo tự dựng, nên gấp đôi là không thể, tức bộ đo quá dễ vì mỗi câu tìm trùng tiêu đề note. Nhóm chọn làm khó bộ đo thay vì hạ ngưỡng; baseline xuống 0,27 và 0,40, và gói tiếng Việt đưa cả hai lên 1,00. Ai tự dựng bộ đo để đánh giá search đều có thể rơi vào cùng cái bẫy này.
**Bối cảnh:** Corpus sinh có note trùng tiêu đề với câu tìm, nên vector và nhánh title tìm ra note dù FTS5 không bỏ dấu được.
**Chuyện gì xảy ra:** Baseline upstream đạt Hit@5 0,93 với vi-unaccented và 0,87 với vi-dd, nên điều kiện gấp đôi baseline không thể đạt. Người dùng chọn làm khó corpus chứ không hạ ngưỡng, và baseline xuống 0,27 và 0,40. Sau gói tiếng Việt, cả hai lên 1,00, và nDCG@5 tổng từ 0,666 lên 0,932 mà không hạng mục nào tụt.
**Bài học:** Khi mục tiêu không đạt được vì bộ đo quá dễ, sửa bộ đo trước khi nghĩ đến hạ ngưỡng, và đo lại baseline trên bộ mới.
**Artefact:** Bảng Hit@5 theo hạng mục trước và sau, không kèm câu hỏi.
