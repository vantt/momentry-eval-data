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
angle: "Obsidian Hybrid Search là công cụ tìm kiếm ghi chú Obsidian, và nhóm đang đo xem gói tiếng Việt có giúp tìm kiếm trên vault thật không. Cổng chất lượng theo từng nhóm câu hỏi được dùng để soát từng nhóm, nhưng với 61 câu chia thành 2–6 câu mỗi nhóm, một câu rơi khỏi top 5 làm vi-iy tụt 0,26 dù điểm tổng tăng từ 0,600 lên 0,698. Ai đánh giá bộ câu hỏi nhỏ cần biết điểm tổng có thể che mất nhóm nào đang tụt."
audience: dev làm công cụ tìm kiếm và đánh giá chất lượng cho ghi chú
spine_context: "Obsidian Hybrid Search là công cụ tìm kiếm ghi chú Obsidian, đang đánh giá chất lượng tìm kiếm tiếng Việt trên vault thật."
spine_context_lines: [profile]
spine_want: Đo xem gói tiếng Việt có cải thiện tìm kiếm trên vault thật không.
spine_want_lines: ["claude:c4caee3c#L3653"]
spine_obstacle: Điểm tổng tăng nhưng cổng theo hạng mục vẫn đỏ; mỗi hạng mục chỉ 2–6 câu nên một câu rơi làm điểm đổi mạnh.
spine_obstacle_lines: ["claude:c4caee3c#L3680"]
spine_turn: "Cổng theo hạng mục là để soát từng nhóm câu hỏi; hoá ra với bộ nhỏ, vi-iy tụt 0,26 chỉ vì một câu rơi khỏi top 5."
spine_turn_lines: ["claude:c4caee3c#L3680"]
spine_action: Người dùng chốt dùng gói vi cho bộ cài; đã khởi chạy chế độ chi tiết V15b để xem từng hạng mục.
spine_action_lines: ["claude:c4caee3c#L3787", "claude:c4caee3c#L3797"]
spine_outcome: "Tổng nDCG@5 tăng từ 0,600 lên 0,698, nhưng cổng hạng mục vẫn đỏ; vi-synonym tụt 0,167 vì vault chưa có lexicon."
spine_outcome_lines: ["claude:c4caee3c#L3680", "claude:c4caee3c#L3787"]
spine_takeaway: "Với bộ vài câu mỗi nhóm, cổng theo nhóm quá nhạy; nên xem điểm tổng trước, hoặc tăng số câu trước khi dùng cổng theo nhóm."
spine_takeaway_lines: ["claude:c4caee3c#L3680"]
completeness: 7
---

# Eval vault thật: tổng tăng 0,600 lên 0,698 nhưng cổng hạng mục đỏ, người dùng quyết

**Góc kể:** Obsidian Hybrid Search là công cụ tìm kiếm ghi chú Obsidian, và nhóm đang đo xem gói tiếng Việt có giúp tìm kiếm trên vault thật không. Cổng chất lượng theo từng nhóm câu hỏi được dùng để soát từng nhóm, nhưng với 61 câu chia thành 2–6 câu mỗi nhóm, một câu rơi khỏi top 5 làm vi-iy tụt 0,26 dù điểm tổng tăng từ 0,600 lên 0,698. Ai đánh giá bộ câu hỏi nhỏ cần biết điểm tổng có thể che mất nhóm nào đang tụt.
**Bối cảnh:** 61 câu trên vault thật. Hạng mục chỉ có 2 đến 6 câu nên một câu rơi làm điểm hạng mục đổi mạnh.
**Chuyện gì xảy ra:** vi-iy tụt 0,26 vì một câu rơi khỏi top 5, vi-synonym tụt 0,167 vì vault chưa có lexicon. Người dùng chọn dùng gói vi cho bộ cài và yêu cầu thêm chế độ chi tiết V15b để điều tra từng hạng mục.
**Bài học:** Hạng mục có vài câu quá nhạy; đừng dùng cổng theo hạng mục cho bộ nhỏ, hoặc chỉ tính theo tổng.
**Artefact:** Bảng hạng mục trước và sau, không có câu hỏi.
