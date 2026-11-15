---
id: 2026-11-02-eval-vault-that-tong-tang-0
date: 2026-11-02
repo: repo
status: raw
signals: [số trước sau, người duyệt thứ máy soạn, đảo quyết định có lý do]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L3653", "claude:c4caee3c#L3680", "claude:c4caee3c#L3682", "claude:c4caee3c#L3797"]
hook: "Vault thật tăng tổng từ 0,600 lên 0,698, nhưng cổng hạng mục vẫn đỏ"
tension: hop_ma_tan
sides: ["Điểm tổng tăng gần 0,10", "Hai hạng mục tụt, vi-iy mất 0,26 vì một câu rơi khỏi top 5"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một gói npm tìm kiếm ghi chú Obsidian theo nghĩa và từ khoá đang đo chất lượng trên vault thật của người làm. Tổng điểm tăng từ 0,600 lên 0,698, nhưng cổng theo từng hạng mục vẫn đỏ: có hạng mục tụt 0,260 chỉ vì một câu rơi khỏi top 5. Với bộ 2–6 câu mỗi hạng mục, một câu là đủ làm đổi cả điểm, nên cổng hạng mục nhạy hơn mức đáng tin. Ai đo chất lượng tìm kiếm bằng bộ mẫu nhỏ nên để ý điều này."
audience: dev làm công cụ tìm kiếm hoặc đo chất lượng bằng bộ câu hỏi nhỏ
spine_context: "Một gói npm tìm kiếm ghi chú Obsidian theo nghĩa và từ khoá, đang đo chất lượng trên vault thật."
spine_context_lines: [profile, "claude:c4caee3c#L11"]
spine_want: Muốn xác nhận gói tiếng Việt cải thiện tìm kiếm trên vault thật.
spine_want_lines: ["claude:c4caee3c#L3653"]
spine_obstacle: Tổng điểm tăng nhưng cổng theo từng hạng mục vẫn đỏ.
spine_obstacle_lines: ["claude:c4caee3c#L3653"]
spine_turn: "Tưởng cổng theo hạng mục là thước đo đáng tin; hoá ra với 2–6 câu mỗi hạng mục, một câu rơi làm điểm hạng mục đổi mạnh."
spine_turn_lines: ["claude:c4caee3c#L3653", "claude:c4caee3c#L3680"]
spine_action: Chốt dùng gói vi cho bộ cài; khởi chạy V15b thêm chế độ chi tiết cho cổng.
spine_action_lines: ["claude:c4caee3c#L3787", "claude:c4caee3c#L3797"]
spine_outcome: "Tổng nDCG@5 tăng từ 0,600 lên 0,698; cổng theo hạng mục vẫn đỏ, V15b đang chạy."
spine_outcome_lines: ["claude:c4caee3c#L3653", "claude:c4caee3c#L3797"]
spine_takeaway: Bộ nhỏ theo hạng mục quá nhạy; nên tính theo tổng hoặc không dùng cổng hạng mục cho bộ 2–6 câu.
spine_takeaway_lines: ["claude:c4caee3c#L3680"]
completeness: 7
---

# Eval vault thật: tổng tăng 0,600 lên 0,698 nhưng cổng hạng mục đỏ, người dùng quyết

**Góc kể:** Một gói npm tìm kiếm ghi chú Obsidian theo nghĩa và từ khoá đang đo chất lượng trên vault thật của người làm. Tổng điểm tăng từ 0,600 lên 0,698, nhưng cổng theo từng hạng mục vẫn đỏ: có hạng mục tụt 0,260 chỉ vì một câu rơi khỏi top 5. Với bộ 2–6 câu mỗi hạng mục, một câu là đủ làm đổi cả điểm, nên cổng hạng mục nhạy hơn mức đáng tin. Ai đo chất lượng tìm kiếm bằng bộ mẫu nhỏ nên để ý điều này.
**Bối cảnh:** 61 câu trên vault thật. Hạng mục chỉ có 2 đến 6 câu nên một câu rơi làm điểm hạng mục đổi mạnh.
**Chuyện gì xảy ra:** vi-iy tụt 0,26 vì một câu rơi khỏi top 5, vi-synonym tụt 0,167 vì vault chưa có lexicon. Người dùng chọn dùng gói vi cho bộ cài và yêu cầu thêm chế độ chi tiết V15b để điều tra từng hạng mục.
**Bài học:** Hạng mục có vài câu quá nhạy; đừng dùng cổng theo hạng mục cho bộ nhỏ, hoặc chỉ tính theo tổng.
**Artefact:** Bảng hạng mục trước và sau, không có câu hỏi.
