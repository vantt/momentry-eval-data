---
id: 2026-11-02-phuc-hoi-dau-bien-mot-tu
date: 2026-11-02
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, số trước sau]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L2787", "claude:c4caee3c#L2789", "claude:c4caee3c#L2842"]
hook: "Sửa dấu tiếng Việt lại đổi từ đúng thành từ sai nghĩa"
tension: giup_ma_hai
sides: ["Phục hồi dấu để tìm kiếm chính xác hơn", "Từ không dấu bị đổi thành từ phổ biến khác, sai nghĩa"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án Obsidian Hybrid Search là gói npm tìm kiếm trong vault Obsidian, và người làm muốn tiếng Việt tìm đúng hơn, kể cả khi gõ không dấu. Giả thuyết ban đầu là ngưỡng 50% đang sai, vì câu \"Hội An\" chỉ có một nửa âm tiết có dấu nên bị phục hồi dấu thành \"Hội ăn\". Hoá ra ngưỡng đúng theo đặc tả, lỗi nằm ở cách dựng câu gửi model nhúng: từ đã gõ dấu phải giữ nguyên. Ai làm tìm kiếm tiếng Việt nên nhớ rằng đổi ngưỡng cho khớp test là sai hướng."
audience: dev làm tìm kiếm hoặc xử lý tiếng Việt
spine_context: "Dự án Obsidian Hybrid Search là gói npm tìm kiếm trong vault Obsidian theo nghĩa và từ khoá, dùng được cho người dùng Obsidian và AI agent."
spine_context_lines: [profile]
spine_want: "Muốn gói tiếng Việt tìm đúng hơn, kể cả khi người dùng gõ không dấu hoặc gõ một phần có dấu."
spine_want_lines: ["claude:c4caee3c#L2776"]
spine_obstacle: "Bước phục hồi dấu đổi chữ \"An\" thành \"ăn\" trong câu \"Hội An\", vì câu chỉ có một trên hai âm tiết có dấu nên không vượt ngưỡng."
spine_obstacle_lines: ["claude:c4caee3c#L2787"]
spine_turn: "Giả thuyết ban đầu là ngưỡng 50% sai; hoá ra ngưỡng đúng theo đặc tả, lỗi nằm ở cách dựng câu gửi model nhúng."
spine_turn_lines: ["claude:c4caee3c#L2787", "claude:c4caee3c#L2789"]
spine_action: "Viết test tái hiện lỗi trước khi sửa, rồi sửa cách dựng: từ đã gõ dấu giữ nguyên, từ không dấu chỉ được khôi phục khi vault không bao giờ viết trần và xác suất đủ ngưỡng."
spine_action_lines: ["claude:c4caee3c#L2787"]
spine_outcome: "nDCG@5 tổng tăng từ 0,932 lên 0,954, không hạng mục nào tụt, và tuỳ chọn được bật mặc định."
spine_outcome_lines: ["claude:c4caee3c#L2787", "claude:c4caee3c#L2789"]
spine_takeaway: "Ngưỡng đúng theo đặc tả vẫn có thể sai ở chỗ dựng câu. Hãy kiểm bằng test trước khi sửa, và đừng đổi ngưỡng cho khớp kết quả."
spine_takeaway_lines: ["claude:c4caee3c#L2787"]
completeness: 7
---

# Phục hồi dấu biến một từ không dấu thành từ khác trong câu có dấu một phần

**Góc kể:** Dự án Obsidian Hybrid Search là gói npm tìm kiếm trong vault Obsidian, và người làm muốn tiếng Việt tìm đúng hơn, kể cả khi gõ không dấu. Giả thuyết ban đầu là ngưỡng 50% đang sai, vì câu "Hội An" chỉ có một nửa âm tiết có dấu nên bị phục hồi dấu thành "Hội ăn". Hoá ra ngưỡng đúng theo đặc tả, lỗi nằm ở cách dựng câu gửi model nhúng: từ đã gõ dấu phải giữ nguyên. Ai làm tìm kiếm tiếng Việt nên nhớ rằng đổi ngưỡng cho khớp test là sai hướng.
**Bối cảnh:** Tuỳ chọn restoreForEmbedding gửi câu đã phục hồi dấu cho model nhúng. Ngưỡng tỷ lệ âm tiết có dấu dùng phép so sánh lớn hơn nghiêm ngặt.
**Chuyện gì xảy ra:** Với câu có một trên hai âm tiết có dấu (tỷ lệ 0,5), câu không được coi là có dấu nên đi nhánh phục hồi. Từ không dấu được đổi thành dạng phổ biến hơn trong vault, làm sai nghĩa. Sửa: từ đã gõ dấu không bao giờ đổi; từ không dấu chỉ được khôi phục khi vault không bao giờ viết trần và xác suất đủ ngưỡng. Sau sửa nDCG@5 tổng từ 0,932 lên 0,954, không hạng mục nào tụt, tuỳ chọn bật mặc định.
**Bài học:** Ngưỡng đúng theo spec vẫn có thể sai ở chỗ dựng câu; kiểm bằng test trước khi sửa, đừng đổi ngưỡng để khớp.
**Artefact:** Bảng bật và tắt restoreForEmbedding theo hạng mục.
