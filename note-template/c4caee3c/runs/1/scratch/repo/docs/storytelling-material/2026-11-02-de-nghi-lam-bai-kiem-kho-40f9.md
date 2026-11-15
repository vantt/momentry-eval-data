---
id: 2026-11-02-de-nghi-lam-bai-kiem-kho-40f9
code: M-7VEC
aliases: [M-7VEC]
date: 2026-11-02
repo: repo
status: raw
signals: [so_truoc_so_sau, rang_buoc_thiet_ke]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L334", "claude:c4caee3c#L1044", "claude:c4caee3c#L1150", "claude:c4caee3c#L1264"]
hook: "Bộ kiểm tra dễ khiến lỗi dấu tiếng Việt bị che mất"
tension: tuong_ma_hoa_ra
sides: ["Baseline tưởng đã xử lý được dấu", "Câu hỏi trùng tên note nên che lỗi; bộ khó còn 0,27"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một công cụ tìm kiếm chạy cục bộ trên kho ghi chú Obsidian, đang cố đạt Hit@5 ít nhất 0,85 và gấp đôi baseline cho tiếng Việt. Người làm tin baseline đã xử lý được dấu, vì bộ đo cho 0,93, nhưng mỗi câu hỏi trùng tên note nên nhánh tiêu đề che lỗi: FTS5 không bỏ được âm tiết có hai dấu và chữ đ. Khi làm bộ đo tách tiêu đề khỏi câu hỏi, baseline rơi còn 0,27 và 0,40, và gói tiếng Việt đưa cả hai lên 1,00. Ai viết bộ đo tìm kiếm bằng ghi chú có tên trùng câu hỏi nên kiểm tra lại điểm của mình."
audience: dev làm công cụ tìm kiếm hoặc viết bộ đo cho tìm kiếm
spine_context: "Một công cụ tìm kiếm chạy cục bộ trên kho ghi chú Obsidian, đang làm bộ đo chất lượng cho phần tiếng Việt."
spine_context_lines: [profile]
spine_want: "Muốn Hit@5 ít nhất 0,85 và gấp đôi baseline ở phần tiếng Việt."
spine_want_lines: ["claude:c4caee3c#L315"]
spine_obstacle: "Baseline upstream đã đạt 0,93 và 0,87 trên bộ eval sinh, nên mục tiêu không đạt được."
spine_obstacle_lines: ["claude:c4caee3c#L315"]
spine_turn: "Tưởng baseline đã xử lý được dấu tiếng Việt; hoá ra điểm cao là do câu hỏi trùng tên note, nhánh tiêu đề che lỗi FTS5 không bỏ được âm tiết có hai dấu và chữ đ."
spine_turn_lines: ["claude:c4caee3c#L1034"]
spine_action: "Làm bộ eval khó hơn, tách tiêu đề khỏi câu hỏi và thêm ca khó về dấu, thay vì hạ ngưỡng."
spine_action_lines: ["claude:c4caee3c#L334", "claude:c4caee3c#L1044"]
spine_outcome: "Baseline vi-unaccented còn 0,27 và vi-dd còn 0,40; sau gói tiếng Việt cả hai đạt 1,00."
spine_outcome_lines: ["claude:c4caee3c#L1034", "claude:c4caee3c#L1150"]
spine_takeaway: "Bộ đo cần tách tiêu đề khỏi câu hỏi và có ca khó về dấu, nếu không điểm cao có thể che lỗi."
spine_takeaway_lines: ["claude:c4caee3c#L1034"]
completeness: 7
---

# Đề nghị làm bài kiểm khó hơn để baseline không đạt

**Góc kể:** Một công cụ tìm kiếm chạy cục bộ trên kho ghi chú Obsidian, đang cố đạt Hit@5 ít nhất 0,85 và gấp đôi baseline cho tiếng Việt. Người làm tin baseline đã xử lý được dấu, vì bộ đo cho 0,93, nhưng mỗi câu hỏi trùng tên note nên nhánh tiêu đề che lỗi: FTS5 không bỏ được âm tiết có hai dấu và chữ đ. Khi làm bộ đo tách tiêu đề khỏi câu hỏi, baseline rơi còn 0,27 và 0,40, và gói tiếng Việt đưa cả hai lên 1,00. Ai viết bộ đo tìm kiếm bằng ghi chú có tên trùng câu hỏi nên kiểm tra lại điểm của mình.
**Bối cảnh:** Mục tiêu G3 yêu cầu Hit@5 ít nhất 0,85 và gấp đôi baseline. Trên bộ eval sinh, baseline upstream đã đạt 0,93 và 0,87, nên mục tiêu không thể đạt.
**Chuyện gì xảy ra:** Chủ dự án chọn làm bộ eval khó hơn thay vì hạ ngưỡng. Nguyên nhân: mỗi câu tìm trùng tên note, nên nhánh tiêu đề tìm được dù FTS5 không bỏ dấu. Đo trực tiếp cho thấy unicode61 chỉ bỏ dấu được âm tiết có một dấu, không bỏ được âm tiết có hai dấu như ế, ữ, ợ, ặ, cũng không bỏ được đ. Bộ mới đưa baseline xuống 0,27 và 0,40. Sau gói tiếng Việt, cả hai đạt 1,00.
**Bài học:** Bộ đo có thể che điểm yếu khi tiêu đề trùng câu trả lời. Muốn đo đúng, bộ đo phải tách tiêu đề khỏi câu hỏi và có các ca khó về dấu.
**Artefact:** Bảng Hit@5 baseline theo hạng mục trước và sau khi làm khó hơn (chỉ có tên hạng mục).
