---
id: 2026-11-02-ten-rieng-hai-chu-bi-phuc-40f9
code: M-MKN7
aliases: [M-MKN7]
date: 2026-11-02
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo, khac]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L2733", "claude:c4caee3c#L2787", "claude:c4caee3c#L2789", "claude:c4caee3c#L2842"]
hook: "Một tên riêng hai chữ bị 'sửa' thành từ thường, điểm tụt"
tension: giup_ma_hai
sides: ["Phục hồi dấu để tìm tiếng Việt chuẩn hơn", "Tên riêng bị đổi thành từ thường, kéo điểm tìm kiếm xuống"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Obsidian Hybrid Search là công cụ tìm kiếm cho vault Obsidian chạy local, và người làm đang muốn tìm tiếng Việt đúng hơn kể cả khi gõ không dấu. Ban đầu có nghi ngờ rằng ngưỡng 50% của tính năng phục hồi dấu khiến tên riêng hai chữ như 'Hội An' bị đổi thành 'hội ăn'. Hoá ra ngưỡng vẫn đúng; lỗi nằm ở cách dựng câu gửi cho model nhúng, và sau khi sửa nDCG@5 tăng từ 0,932 lên 0,954. Ai xây tìm kiếm trên văn bản tiếng Việt có thể gặp đúng kiểu lỗi này."
audience: dev xây tìm kiếm hoặc công cụ có văn bản tiếng Việt
spine_context: "Obsidian Hybrid Search là công cụ tìm kiếm cho vault Obsidian chạy local, có plugin, MCP server cho agent và CLI. Người làm đang cải thiện tìm kiếm tiếng Việt."
spine_context_lines: [profile]
spine_want: "Muốn tìm đúng tiếng Việt, kể cả khi người dùng gõ không dấu, nhờ phục hồi dấu trước khi nhúng câu hỏi."
spine_want_lines: ["claude:c4caee3c#L2733"]
spine_obstacle: "Phục hồi dấu đổi chữ 'An' trong 'Hội An' thành 'ăn', nên câu gửi cho model thành 'hội ăn'."
spine_obstacle_lines: ["claude:c4caee3c#L2787"]
spine_turn: "Tưởng ngưỡng 50% phục hồi dấu là nguyên nhân; hoá ra ngưỡng đúng, lỗi nằm ở cách dựng câu gửi cho model nhúng."
spine_turn_lines: ["claude:c4caee3c#L2787"]
spine_action: Viết test cho 'Hội An' và chứng minh test đỏ trên mã cũ. Sau đó chỉ phục hồi chữ không dấu khi vault không bao giờ viết trần và độ tin cậy đủ.
spine_action_lines: ["claude:c4caee3c#L2787"]
spine_outcome: "nDCG@5 tổng tăng từ 0,932 lên 0,954, không hạng mục nào tụt. Tuỳ chọn restoreForEmbedding được bật mặc định."
spine_outcome_lines: ["claude:c4caee3c#L2789"]
spine_takeaway: "Khi lỗi nằm ở cách dựng đầu vào, đừng sửa ngưỡng. Viết test chứng minh lỗi trước khi sửa."
spine_takeaway_lines: ["claude:c4caee3c#L2787"]
completeness: 7
---

# Tên riêng hai chữ bị phục hồi dấu thành từ thường, kéo nDCG@5 xuống

**Góc kể:** Obsidian Hybrid Search là công cụ tìm kiếm cho vault Obsidian chạy local, và người làm đang muốn tìm tiếng Việt đúng hơn kể cả khi gõ không dấu. Ban đầu có nghi ngờ rằng ngưỡng 50% của tính năng phục hồi dấu khiến tên riêng hai chữ như 'Hội An' bị đổi thành 'hội ăn'. Hoá ra ngưỡng vẫn đúng; lỗi nằm ở cách dựng câu gửi cho model nhúng, và sau khi sửa nDCG@5 tăng từ 0,932 lên 0,954. Ai xây tìm kiếm trên văn bản tiếng Việt có thể gặp đúng kiểu lỗi này.
**Bối cảnh:** Khi bật restoreForEmbedding, một câu có một chữ có dấu trên hai chữ được coi là chưa có dấu, nên chữ không dấu bị phục hồi theo từ phổ biến hơn trong vault.
**Chuyện gì xảy ra:** Model eval phát hiện một tên riêng hai chữ bị đổi sang từ thường. Ngưỡng 50% của PRD không sai, lỗi nằm ở cách dựng câu gửi cho embedder. Agent viết test thất bại trên mã cũ trước, rồi sửa để chỉ phục hồi chữ không dấu khi vault không bao giờ viết nó trần và độ tin cậy đủ. nDCG@5 tổng tăng từ 0,932 lên 0,954, không hạng mục nào tụt, và tuỳ chọn được bật mặc định.
**Bài học:** Đừng sửa ngưỡng khi lỗi nằm ở chỗ dựng đầu vào. Viết test chứng minh lỗi trước khi sửa.
**Artefact:** Bảng nDCG@5 trước và sau cho hạng mục liên quan.
