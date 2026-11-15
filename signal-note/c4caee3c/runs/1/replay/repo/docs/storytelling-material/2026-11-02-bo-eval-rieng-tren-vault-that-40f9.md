---
id: 2026-11-02-bo-eval-rieng-tren-vault-that-40f9
code: M-347G
aliases: [M-347G]
date: 2026-11-02
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L3615", "claude:c4caee3c#L3623", "claude:c4caee3c#L3645", "claude:c4caee3c#L3680", "claude:c4caee3c#L3682", "claude:c4caee3c#L3787", "claude:c4caee3c#L3797"]
hook: "Tổng điểm tăng 0,60 lên 0,70, nhưng một câu rớt làm hạng mục tụt 0,26"
tension: hop_ma_tan
sides: ["Điểm tổng tăng rõ rệt", "Cổng đỏ vì hạng mục chỉ 2 đến 6 câu"]
strength: 2
stakes: 2
hits: 1
runs: 1
unverified_facts: ["0,70"]
privacy: unchecked
links: []
threads: []
angle: none
spine_context: "Dự án Obsidian Hybrid Search: công cụ tìm kiếm local cho vault Obsidian, dùng cho người dùng Obsidian và agent AI. Người làm đang hoàn tất plan roadmap của fork."
spine_context_lines: [profile, "claude:c4caee3c#L11"]
spine_want: Hoàn tất các mục trong plan roadmap của fork.
spine_want_lines: ["claude:c4caee3c#L11"]
spine_action: "Merge nhánh đánh giá riêng trên vault thật vào master, rồi hỏi chủ phiên chọn gói tiếng Việt."
spine_action_lines: ["claude:c4caee3c#L3645", "claude:c4caee3c#L3682"]
completeness: 3
---

# Bộ eval riêng trên vault thật: tổng tăng, cổng theo hạng mục đỏ, và quy tắc không để dữ liệu rời máy

**Bối cảnh:** Người dùng chạy đánh giá trên 61 câu thật của mình, trên một nhánh riêng của repo dự án, và nhánh được đẩy lên remote.
**Chuyện gì xảy ra:** Tổng nDCG@5 tăng từ 0,600 lên 0,698 nhưng cổng theo hạng mục đỏ vì vi-iy tụt 0,26 khi chỉ một câu rơi khỏi top 5 (mỗi hạng mục chỉ 2 đến 6 câu). Người dùng chọn dùng gói tiếng Việt cho bộ cài và thêm chế độ chi tiết ghi ra file ngoài repo, có chặn đường dẫn trong repo. Lead cũng phải nhắc để câu hỏi và tên note không lên remote công khai.
**Bài học:** Với hạng mục chỉ vài câu, cổng theo hạng mục rất nhạy; đánh giá dữ liệu riêng cần có đường ra ngoài repo được kiểm soát.
**Artefact:** Bảng tổng hợp theo hạng mục (đã bỏ câu hỏi và đường dẫn).
