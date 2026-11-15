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
angle: "Obsidian Hybrid Search là công cụ tìm ghi chú Obsidian, và nhóm đang làm gói tiếng Việt cho nó với mục tiêu đạt gấp đôi baseline. Baseline upstream đạt 0,93 nên có vẻ tìm tiếng Việt đã ổn, nhưng corpus thử quá dễ: tiêu đề note trùng đúng câu tìm nên che mất lỗi không bỏ được dấu. Khi làm khó corpus, baseline rớt còn 0,27, và sau gói tiếng Việt đạt 1,00. Dev làm công cụ tìm kiếm hoặc tin vào số đo benchmark nên nghe chuyện này."
audience: dev làm công cụ tìm kiếm và benchmark
spine_context: "Obsidian Hybrid Search là công cụ tìm ghi chú Obsidian, kết hợp tìm theo nghĩa, toàn văn, tiêu đề, thẻ và liên kết; đang làm gói tiếng Việt cho nó."
spine_context_lines: [profile]
spine_want: "Đạt Hit@5 tối thiểu 0,85 và gấp ít nhất 2 lần baseline ở tiếng Việt."
spine_want_lines: ["claude:c4caee3c#L315"]
spine_obstacle: "Baseline upstream đã đạt 0,93 trên corpus sinh, nên điều kiện gấp đôi không thể đạt."
spine_obstacle_lines: ["claude:c4caee3c#L315"]
spine_turn: "Tưởng 0,93 nghĩa là tìm tiếng Việt không dấu đã tốt; hoá ra tiêu đề note trùng đúng câu tìm nên che mất lỗi FTS5 không bỏ được dấu."
spine_turn_lines: ["claude:c4caee3c#L1034"]
spine_action: "Người dùng chọn làm corpus khó hơn thay vì hạ ngưỡng; dựng lại fixture với tiêu đề chỉ đánh số, không lộ câu tìm."
spine_action_lines: ["claude:c4caee3c#L334", "claude:c4caee3c#L1034"]
spine_outcome: "Upstream: vi-unaccented từ 0,93 xuống 0,27, vi-dd từ 0,87 xuống 0,40. Sau gói tiếng Việt, cả hai lên 1,00."
spine_outcome_lines: ["claude:c4caee3c#L315", "claude:c4caee3c#L1034", "claude:c4caee3c#L1150"]
spine_takeaway: Benchmark có tiêu đề lộ câu tìm sẽ che lỗi tìm; đo lại với nhiều kiểu gõ và đúng tokenizer của hệ thống.
spine_takeaway_lines: ["claude:c4caee3c#L1034"]
completeness: 7
---

# Corpus tiếng Việt quá dễ: baseline 0,93 không đo được gì

**Góc kể:** Obsidian Hybrid Search là công cụ tìm ghi chú Obsidian, và nhóm đang làm gói tiếng Việt cho nó với mục tiêu đạt gấp đôi baseline. Baseline upstream đạt 0,93 nên có vẻ tìm tiếng Việt đã ổn, nhưng corpus thử quá dễ: tiêu đề note trùng đúng câu tìm nên che mất lỗi không bỏ được dấu. Khi làm khó corpus, baseline rớt còn 0,27, và sau gói tiếng Việt đạt 1,00. Dev làm công cụ tìm kiếm hoặc tin vào số đo benchmark nên nghe chuyện này.
**Bối cảnh:** Mục tiêu G3 yêu cầu Hit@5 từ 0,85 và gấp đôi baseline. Baseline upstream đã đạt 0,93 trên corpus sinh nên điều kiện gấp đôi không thể đạt.
**Chuyện gì xảy ra:** Chẩn đoán: tiêu đề note trùng đúng cụm câu tìm, nên nhánh tiêu đề và nhánh vector tìm ra note dù FTS5 không bỏ được dấu. Đo unicode61 trực tiếp: chỉ bỏ được syllable có một dấu, không bỏ được syllable hai dấu hay chữ đ. Người dùng chọn làm corpus khó hơn thay vì hạ ngưỡng. Hit@5 không dấu từ 0,93 xuống 0,27, dd từ 0,87 xuống 0,40. Gói tiếng Việt sau đó đưa không dấu lên 1,00.
**Bài học:** Benchmark có tiêu đề lộ câu tìm sẽ che mất lỗi tìm; đo lại với các kiểu gõ khác và đúng tokenizer của hệ thống.
**Artefact:** Bảng Hit@5 trước và sau theo hạng mục.
