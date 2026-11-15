---
id: 2026-11-02-eval-tren-vault-that-tong-tang-40f9
code: M-49A8
aliases: [M-49A8]
date: 2026-11-02
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L3623", "claude:c4caee3c#L3645", "claude:c4caee3c#L3680", "claude:c4caee3c#L3682", "claude:c4caee3c#L3797", "claude:c4caee3c#L3809"]
hook: "Điểm tổng lên 0,600 → 0,698, nhưng có hạng mục tụt 0,260"
tension: hop_ma_tan
sides: ["Điểm tổng trên vault thật tăng từ 0,600 lên 0,698", "Có hạng mục tụt 0,260 vì một câu rơi khỏi top 5"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: none
spine_context: Obsidian Hybrid Search là công cụ tìm kiếm cho vault Obsidian chạy local; đang đánh giá chất lượng tìm kiếm trên vault thật của người dùng.
spine_context_lines: [profile]
spine_want: "Quyết định có dùng gói tiếng Việt (vi) cho bộ cài hay không, dựa trên bộ golden set 61 câu."
spine_want_lines: ["claude:c4caee3c#L3680"]
spine_obstacle: "Tổng nDCG@5 tăng từ 0,600 lên 0,698, nhưng một số hạng mục tụt, trong đó vi-iy giảm 0,260 do một câu rơi khỏi top 5."
spine_obstacle_lines: ["claude:c4caee3c#L3680"]
spine_action: Người dùng chọn dùng gói vi cho bộ cài; agent ghi quyết định vào plan và giao việc V15b (chế độ --private-detail).
spine_action_lines: ["claude:c4caee3c#L3682", "claude:c4caee3c#L3809"]
spine_outcome: V15b phần đầu đã xong và đẩy lên master (6cda0fc); phần chạy trên vault thật còn chờ người dùng chạy trên máy mình.
spine_outcome_lines: ["claude:c4caee3c#L3825"]
completeness: 5
---

# Eval trên vault thật: tổng tăng nhưng cổng hạng mục đỏ, người dùng chọn dùng gói

**Bối cảnh:** Golden set 61 câu của người dùng nằm ngoài repo. Script chỉ in số tổng hợp, không in câu hỏi hay tên note.
**Chuyện gì xảy ra:** Tổng nDCG@5 trên vault thật tăng từ 0,600 lên 0,698, nhưng vài hạng mục có 2 đến 6 câu bị tụt, có hạng mục tụt 0,260 vì một câu rơi khỏi top 5. Người dùng quyết định dùng gói vi cho bộ cài. Công cụ chi tiết ghi từng câu ra một file ngoài repo và từ chối ghi nếu đường dẫn nằm trong repo.
**Bài học:** Đánh giá trên dữ liệu thật cần công cụ chi tiết nhưng ghi ra nơi riêng tư. Mẫu nhỏ cho biến động lớn, đừng quyết định theo một hạng mục.
**Artefact:** Bảng số tổng hợp theo hạng mục, không có câu hỏi.
