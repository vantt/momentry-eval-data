---
id: 2026-11-02-vault-that-tong-tang-nhung-hang-40f9
code: M-32CA
aliases: [M-32CA]
date: 2026-11-02
repo: repo
status: raw
signals: [so_truoc_so_sau, khac]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L3653", "claude:c4caee3c#L3680", "claude:c4caee3c#L3696"]
hook: "Điểm tổng tăng 0,600 lên 0,698, nhưng vi-iy rớt 0,260"
tension: tuong_ma_hoa_ra
sides: ["Tổng điểm tăng rõ rệt", "Nhiều hạng mục tụt, có hạng mục mất 0,260"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một công cụ tìm kiếm cục bộ cho kho ghi chú Obsidian đang được đo chất lượng trên vault thật của chủ dự án. Điểm tổng nDCG@5 tăng từ 0,600 lên 0,698 sau khi thêm gói tiếng Việt, tưởng là tin tốt. Nhưng khi xem từng hạng mục, vi-iy rớt 0,260 và vi-synonym rớt 0,167, vì bộ đo chỉ có 2 đến 6 câu mỗi nhóm. Với bộ đo nhỏ, điểm tổng có thể che mất những nhóm đang giảm mạnh."
audience: dev dùng AI hằng ngày và làm đo lường chất lượng tìm kiếm
spine_context: "Một công cụ tìm kiếm chạy cục bộ trên kho ghi chú Obsidian, đang làm bộ đo chất lượng tìm kiếm trên vault thật của chủ dự án."
spine_context_lines: [profile]
spine_want: Muốn biết gói tiếng Việt có làm tìm kiếm tốt hơn trên vault thật hay không.
spine_want_lines: ["claude:c4caee3c#L3504"]
spine_obstacle: "Tổng điểm tăng nhưng cổng theo hạng mục báo hỏng: vi-iy rớt 0,260, vi-synonym rớt 0,167."
spine_obstacle_lines: ["claude:c4caee3c#L3653", "claude:c4caee3c#L3682"]
spine_turn: "Tưởng tổng tăng là đủ để kết luận gói tiếng Việt tốt; hoá ra với bộ đo chỉ 2–6 câu mỗi hạng mục, tổng có thể tăng trong khi từng nhóm giảm mạnh."
spine_turn_lines: ["claude:c4caee3c#L3682"]
spine_action: Chủ dự án chọn dùng gói tiếng Việt và giao việc tìm nguyên nhân từng hạng mục.
spine_action_lines: ["claude:c4caee3c#L3682"]
spine_outcome: "Tổng nDCG@5 từ 0,600 lên 0,698; vi-iy −0,260, vi-accented −0,052, vi-compound −0,041, vi-synonym −0,167; lượt catchup sau đó hỏng."
spine_outcome_lines: ["claude:c4caee3c#L3682", "claude:c4caee3c#L3697"]
spine_takeaway: "Với bộ đo nhỏ, xem từng hạng mục trước khi kết luận dựa vào điểm tổng."
spine_takeaway_lines: ["claude:c4caee3c#L3682"]
completeness: 7
---

# Vault thật: tổng tăng nhưng hạng mục rơi

**Góc kể:** Một công cụ tìm kiếm cục bộ cho kho ghi chú Obsidian đang được đo chất lượng trên vault thật của chủ dự án. Điểm tổng nDCG@5 tăng từ 0,600 lên 0,698 sau khi thêm gói tiếng Việt, tưởng là tin tốt. Nhưng khi xem từng hạng mục, vi-iy rớt 0,260 và vi-synonym rớt 0,167, vì bộ đo chỉ có 2 đến 6 câu mỗi nhóm. Với bộ đo nhỏ, điểm tổng có thể che mất những nhóm đang giảm mạnh.
**Bối cảnh:** Chủ dự án chạy bộ 61 câu trên vault thật của mình, không chia sẻ nội dung ra ngoài.
**Chuyện gì xảy ra:** Tổng nDCG@5 tăng từ 0,600 lên 0,698. Nhưng cổng theo hạng mục báo hỏng: vi-iy giảm 0,260 vì một câu rơi khỏi top 5, vi-accented giảm 0,052, vi-compound giảm 0,041 vì đổi thứ hạng, vi-synonym giảm 0,167 vì vault chưa có lexicon. Mỗi hạng mục chỉ có 2 đến 6 câu. Chủ dự án chọn dùng gói tiếng Việt và giao việc tìm nguyên nhân từng hạng mục.
**Bài học:** Với bộ đo nhỏ, tổng có thể tăng trong khi từng nhóm giảm mạnh. Xem từng hạng mục trước khi kết luận.
**Artefact:** Bảng hạng mục trước và sau (không có câu hỏi, không có tên note).
