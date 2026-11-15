---
id: 2026-11-02-corpus-tieng-viet-qua-de-baseline
date: 2026-11-02
repo: repo
status: raw
signals: [số trước sau, đảo quyết định có lý do]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L315", "claude:c4caee3c#L1044", "claude:c4caee3c#L1150", "claude:c4caee3c#L1264"]
hook: "Baseline 0,93 tưởng tốt, thật ra bộ test quá dễ để đo gì"
tension: tuong_ma_hoa_ra
sides: ["Điểm 0,93 trông như hệ thống tìm tốt", "Tiêu đề trùng câu hỏi nên không đo được gì; làm khó thì còn 0,27"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Obsidian Hybrid Search là công cụ tìm ghi chú Obsidian theo nghĩa và theo từ, và người làm đang muốn gói tiếng Việt của nó tìm tốt gấp đôi baseline. Ban đầu baseline 0,93 có vẻ là mức đã rất cao nên điều kiện gấp đôi tưởng không thể đạt. Hoá ra bộ test tiếng Việt quá dễ: tiêu đề mỗi ghi chú trùng đúng câu tìm, nên 0,93 không đo được gì, và khi bỏ dấu điểm rơi xuống 0,27. Ai làm benchmark tìm kiếm nên kiểm tra xem bộ test có đang tự lộ đáp án không."
audience: dev làm công cụ tìm kiếm hoặc benchmark cho tài liệu cá nhân
spine_context: Obsidian Hybrid Search là công cụ tìm ghi chú Obsidian theo nghĩa và theo từ; người làm đang đưa gói tiếng Việt vào để cải thiện chất lượng tìm.
spine_context_lines: [profile, "claude:c4caee3c#L11"]
spine_want: "Hit@5 đạt tối thiểu 0,85 và gấp tối thiểu 2 lần baseline."
spine_want_lines: ["claude:c4caee3c#L315"]
spine_obstacle: "Baseline upstream đã đạt 0,93 trên corpus sinh, nên điều kiện gấp đôi không thể đạt."
spine_obstacle_lines: ["claude:c4caee3c#L315"]
spine_turn: "Tưởng 0,93 là mức tìm tốt thật; hoá ra tiêu đề mỗi ghi chú trùng đúng câu tìm, nên bộ test quá dễ và điểm 0,93 không đo được gì."
spine_turn_lines: ["claude:c4caee3c#L315", "claude:c4caee3c#L1034"]
spine_action: Chọn làm corpus khó hơn thay vì hạ ngưỡng; đánh số tiêu đề và đo lại với kiểu gõ không dấu.
spine_action_lines: ["claude:c4caee3c#L334", "claude:c4caee3c#L1034"]
spine_outcome: "vi-unaccented Hit@5 từ 0,93 xuống 0,27, vi-dd từ 0,87 xuống 0,40; sau khi có gói tiếng Việt, cả hai lên 1,00."
spine_outcome_lines: ["claude:c4caee3c#L1034", "claude:c4caee3c#L1150"]
spine_takeaway: Benchmark có tiêu đề lộ câu tìm sẽ che mất lỗi tìm; hãy đo với kiểu gõ khác và đúng tokenizer của hệ thống.
spine_takeaway_lines: ["claude:c4caee3c#L1034"]
completeness: 7
---

# Corpus tiếng Việt quá dễ: baseline 0,93 không đo được gì

**Góc kể:** Obsidian Hybrid Search là công cụ tìm ghi chú Obsidian theo nghĩa và theo từ, và người làm đang muốn gói tiếng Việt của nó tìm tốt gấp đôi baseline. Ban đầu baseline 0,93 có vẻ là mức đã rất cao nên điều kiện gấp đôi tưởng không thể đạt. Hoá ra bộ test tiếng Việt quá dễ: tiêu đề mỗi ghi chú trùng đúng câu tìm, nên 0,93 không đo được gì, và khi bỏ dấu điểm rơi xuống 0,27. Ai làm benchmark tìm kiếm nên kiểm tra xem bộ test có đang tự lộ đáp án không.
**Bối cảnh:** Mục tiêu G3 yêu cầu Hit@5 từ 0,85 và gấp đôi baseline. Baseline upstream đã đạt 0,93 trên corpus sinh nên điều kiện gấp đôi không thể đạt.
**Chuyện gì xảy ra:** Chẩn đoán: tiêu đề note trùng đúng cụm câu tìm, nên nhánh tiêu đề và nhánh vector tìm ra note dù FTS5 không bỏ được dấu. Đo unicode61 trực tiếp: chỉ bỏ được syllable có một dấu, không bỏ được syllable hai dấu hay chữ đ. Người dùng chọn làm corpus khó hơn thay vì hạ ngưỡng. Hit@5 không dấu từ 0,93 xuống 0,27, dd từ 0,87 xuống 0,40. Gói tiếng Việt sau đó đưa không dấu lên 1,00.
**Bài học:** Benchmark có tiêu đề lộ câu tìm sẽ che mất lỗi tìm; đo lại với các kiểu gõ khác và đúng tokenizer của hệ thống.
**Artefact:** Bảng Hit@5 trước và sau theo hạng mục.
