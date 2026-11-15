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
hook: "Điểm tổng tăng 0,600 lên 0,698, nhưng có hạng mục tụt 0,260"
tension: hop_ma_tan
sides: ["Tổng điểm trên vault thật tăng rõ rệt", "Vài hạng mục tụt, một câu rơi khỏi top 5 là mất 0,260"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Obsidian Hybrid Search là công cụ tìm kiếm cho ghi chú Obsidian trên máy, và người làm đang muốn gói tiếng Việt giúp tìm tốt hơn trên vault thật. Tổng điểm nDCG@5 tăng từ 0,600 lên 0,698, nên có vẻ đáng bật gói. Nhưng khi xem từng hạng mục, vi-iy tụt 0,260 vì một câu rơi khỏi top 5, và ba hạng mục khác cũng tụt; người làm vẫn chọn dùng gói. Dev làm tìm kiếm nên biết: một con số tổng có thể che mất hạng mục bị hỏng."
audience: dev làm tìm kiếm hoặc đánh giá chất lượng retrieval
spine_context: Obsidian Hybrid Search là công cụ tìm kiếm cho ghi chú Obsidian trên máy; người làm đang thêm gói ngôn ngữ tiếng Việt (vi) để tìm tốt hơn.
spine_context_lines: [profile, "claude:c4caee3c#L11"]
spine_want: Muốn gói vi làm tìm kiếm trên vault thật tốt hơn.
spine_want_lines: ["claude:c4caee3c#L3680"]
spine_obstacle: "Tổng điểm tăng nhưng nhiều hạng mục tiếng Việt tụt, trong đó vi-iy tụt 0,260."
spine_obstacle_lines: ["claude:c4caee3c#L3680"]
spine_turn: Thấy tổng tăng nên chọn bật gói; hoá ra con số tổng che mất các hạng mục tụt.
spine_turn_lines: ["claude:c4caee3c#L3680", "claude:c4caee3c#L3787"]
spine_action: "Chốt dùng gói vi cho bộ cài và giao việc tìm, sửa các hạng mục tụt."
spine_action_lines: ["claude:c4caee3c#L3787", "claude:c4caee3c#L3822"]
spine_outcome: Phần ghi chi tiết từng câu đã xong; phần chạy trên máy người làm còn lại.
spine_outcome_lines: ["claude:c4caee3c#L3825"]
spine_takeaway: Đừng quyết định theo tổng; mỗi hạng mục chỉ 2–6 câu nên dao động lớn là chuyện thường.
spine_takeaway_lines: ["claude:c4caee3c#L3680"]
completeness: 7
---

# Eval trên vault thật: tổng tăng nhưng cổng hạng mục đỏ, người dùng chọn dùng gói

**Góc kể:** Obsidian Hybrid Search là công cụ tìm kiếm cho ghi chú Obsidian trên máy, và người làm đang muốn gói tiếng Việt giúp tìm tốt hơn trên vault thật. Tổng điểm nDCG@5 tăng từ 0,600 lên 0,698, nên có vẻ đáng bật gói. Nhưng khi xem từng hạng mục, vi-iy tụt 0,260 vì một câu rơi khỏi top 5, và ba hạng mục khác cũng tụt; người làm vẫn chọn dùng gói. Dev làm tìm kiếm nên biết: một con số tổng có thể che mất hạng mục bị hỏng.
**Bối cảnh:** Golden set 61 câu của người dùng nằm ngoài repo. Script chỉ in số tổng hợp, không in câu hỏi hay tên note.
**Chuyện gì xảy ra:** Tổng nDCG@5 trên vault thật tăng từ 0,600 lên 0,698, nhưng vài hạng mục có 2 đến 6 câu bị tụt, có hạng mục tụt 0,260 vì một câu rơi khỏi top 5. Người dùng quyết định dùng gói vi cho bộ cài. Công cụ chi tiết ghi từng câu ra một file ngoài repo và từ chối ghi nếu đường dẫn nằm trong repo.
**Bài học:** Đánh giá trên dữ liệu thật cần công cụ chi tiết nhưng ghi ra nơi riêng tư. Mẫu nhỏ cho biến động lớn, đừng quyết định theo một hạng mục.
**Artefact:** Bảng số tổng hợp theo hạng mục, không có câu hỏi.
