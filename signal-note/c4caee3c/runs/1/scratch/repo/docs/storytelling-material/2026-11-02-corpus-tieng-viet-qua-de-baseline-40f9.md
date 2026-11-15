---
id: 2026-11-02-corpus-tieng-viet-qua-de-baseline-40f9
code: M-Z81P
aliases: [M-Z81P]
date: 2026-11-02
repo: repo
status: raw
signals: [khac, nguyen_nhan_bat_ngo]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L315", "claude:c4caee3c#L334", "claude:c4caee3c#L1044", "claude:c4caee3c#L1150", "claude:c4caee3c#L2187"]
hook: "Baseline 0,93 đẹp mà không đo được gì, làm khó lại còn 0,27"
tension: tuong_ma_hoa_ra
sides: ["Điểm 0,93 trông rất tốt", "Corpus quá dễ, thật ra chỉ 0,27"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án là Obsidian Hybrid Search, một gói npm giúp tìm ghi chú Obsidian theo nghĩa và từ khoá, và người làm đang đưa gói tiếng Việt vượt baseline của upstream. Ban đầu baseline đạt 0,93 nên điều kiện G3 tưởng là không thể đạt. Hoá ra corpus quá dễ: mỗi cụm truy vấn cũng là tiêu đề note nên vẫn tìm được dù FTS5 không bỏ dấu. Sau khi làm khó corpus, baseline xuống 0,27 và 0,40, còn gói đạt 1,00; ai đo chất lượng tìm kiếm nên kiểm xem bài test có để lộ đáp án không."
audience: dev đo chất lượng tìm kiếm hoặc làm công cụ đa ngôn ngữ
spine_context: Dự án Obsidian Hybrid Search là gói npm tìm ghi chú trong vault Obsidian theo nghĩa và từ khoá; người làm đang đưa gói tiếng Việt vượt baseline của upstream.
spine_context_lines: [profile, "claude:c4caee3c#L315"]
spine_want: "Đạt Hit@5 ≥ 0,85 và gấp đôi baseline upstream (G3)."
spine_want_lines: ["claude:c4caee3c#L315"]
spine_obstacle: "Baseline upstream đã đạt 0,93 và 0,87 trên corpus sinh, nên điều kiện G3 tưởng là không thể đạt."
spine_obstacle_lines: ["claude:c4caee3c#L315"]
spine_turn: "Tưởng điểm 0,93 là baseline tốt; hoá ra corpus quá dễ vì mỗi cụm truy vấn cũng là tiêu đề note, nên tìm được dù FTS5 không bỏ dấu."
spine_turn_lines: ["claude:c4caee3c#L315", "claude:c4caee3c#L1034"]
spine_action: "Theo lựa chọn của chủ phiên, làm khó corpus tiếng Việt thay vì hạ ngưỡng, rồi chạy lại eval với gói tiếng Việt."
spine_action_lines: ["claude:c4caee3c#L334", "claude:c4caee3c#L1034"]
spine_outcome: "Baseline upstream xuống 0,27 (vi-unaccented) và 0,40 (vi-dd); với gói, cả hai đạt 1,00."
spine_outcome_lines: ["claude:c4caee3c#L1044", "claude:c4caee3c#L1150"]
spine_takeaway: "Khi baseline gần trần, kiểm xem bài đo có đang đo đúng thứ và tiêu đề có làm lộ đáp án không."
spine_takeaway_lines: ["claude:c4caee3c#L1034"]
completeness: 7
---

# Corpus tiếng Việt quá dễ: baseline 0,93 không đo được gì, nên làm khó corpus chứ không hạ ngưỡng

**Góc kể:** Dự án là Obsidian Hybrid Search, một gói npm giúp tìm ghi chú Obsidian theo nghĩa và từ khoá, và người làm đang đưa gói tiếng Việt vượt baseline của upstream. Ban đầu baseline đạt 0,93 nên điều kiện G3 tưởng là không thể đạt. Hoá ra corpus quá dễ: mỗi cụm truy vấn cũng là tiêu đề note nên vẫn tìm được dù FTS5 không bỏ dấu. Sau khi làm khó corpus, baseline xuống 0,27 và 0,40, còn gói đạt 1,00; ai đo chất lượng tìm kiếm nên kiểm xem bài test có để lộ đáp án không.
**Bối cảnh:** Mục tiêu G3 yêu cầu Hit@5 ≥ 0,85 và gấp đôi baseline của upstream, nhưng upstream chưa có gói đã đạt 0,93 (không dấu) và 0,87 (dd) trên corpus sinh.
**Chuyện gì xảy ra:** Agent đi tìm nguyên nhân và thấy mỗi cụm từ truy vấn cũng là tiêu đề note, nên nhánh tiêu đề và nhánh vector tìm ra note dù FTS5 không bỏ dấu được. Chỉ tiêu đề và bố cục làm baseline trông tốt. Người dùng chọn làm corpus khó hơn thay vì hạ ngưỡng. Baseline mới rơi xuống 0,27 và 0,40; sau khi có gói, cả hai đạt 1,00.
**Bài học:** Khi baseline đã gần trần, bài kiểm đang đo sai thứ; làm khó bộ đo trước khi đụng tới ngưỡng, và kiểm xem tiêu đề có làm lộ đáp án không.
**Artefact:** Bảng Hit@5 trước và sau khi làm khó corpus, theo từng hạng mục.
