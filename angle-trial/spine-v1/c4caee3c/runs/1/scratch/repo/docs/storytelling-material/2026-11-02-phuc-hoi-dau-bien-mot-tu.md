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
angle: "Obsidian Hybrid Search là công cụ tìm ghi chú Obsidian, và nhóm đang chỉnh một tuỳ chọn phục hồi dấu tiếng Việt trước khi gửi câu tìm kiếm cho model nhúng. Giả thuyết ban đầu là ngưỡng so sánh quá nghiêm đã khiến câu có một nửa số âm tiết có dấu bị xử lý sai. Hoá ra ngưỡng đúng theo spec, lỗi nằm ở cách dựng câu: một tên riêng không dấu bị đổi thành \"hội ăn\" vì từ đó phổ biến hơn trong ghi chú. Ai tự dựng câu tìm kiếm tiếng Việt nên kiểm chỗ này, vì một từ bị đổi có thể làm kết quả sai mà không báo lỗi."
audience: dev làm tìm kiếm tiếng Việt hoặc dựng câu cho model nhúng
spine_context: "Obsidian Hybrid Search là công cụ tìm kiếm cho ghi chú Obsidian, đang chỉnh tuỳ chọn phục hồi dấu tiếng Việt trước khi gửi câu tìm kiếm cho model nhúng."
spine_context_lines: [profile, "claude:c4caee3c#L2776"]
spine_want: Muốn bật restoreForEmbedding mặc định nếu kết quả eval cho thấy tốt hơn.
spine_want_lines: ["claude:c4caee3c#L2776"]
spine_obstacle: "Câu có dấu một phần, như có một trên hai âm tiết có dấu, bị đi nhánh phục hồi và làm sai từ không dấu."
spine_obstacle_lines: ["claude:c4caee3c#L2776"]
spine_turn: "Giả thuyết ban đầu là ngưỡng so sánh quá nghiêm; hoá ra ngưỡng đúng theo spec, lỗi nằm ở cách dựng câu."
spine_turn_lines: ["claude:c4caee3c#L2789"]
spine_action: "Sửa cách dựng câu: từ đã gõ dấu giữ nguyên, từ không dấu chỉ được khôi phục khi đủ điều kiện; rồi merge vào nhánh chính."
spine_action_lines: ["claude:c4caee3c#L2789", "claude:c4caee3c#L2790"]
spine_outcome: "nDCG@5 tổng tăng từ 0,932 lên 0,954, không hạng mục nào tụt, nên tuỳ chọn được bật mặc định."
spine_outcome_lines: ["claude:c4caee3c#L2789"]
spine_takeaway: "Ngưỡng đúng theo spec vẫn có thể sai ở chỗ dựng câu; kiểm bằng test trước khi sửa, đừng đổi ngưỡng để khớp."
spine_takeaway_lines: ["claude:c4caee3c#L2776"]
completeness: 7
---

# Phục hồi dấu biến một từ không dấu thành từ khác trong câu có dấu một phần

**Góc kể:** Obsidian Hybrid Search là công cụ tìm ghi chú Obsidian, và nhóm đang chỉnh một tuỳ chọn phục hồi dấu tiếng Việt trước khi gửi câu tìm kiếm cho model nhúng. Giả thuyết ban đầu là ngưỡng so sánh quá nghiêm đã khiến câu có một nửa số âm tiết có dấu bị xử lý sai. Hoá ra ngưỡng đúng theo spec, lỗi nằm ở cách dựng câu: một tên riêng không dấu bị đổi thành "hội ăn" vì từ đó phổ biến hơn trong ghi chú. Ai tự dựng câu tìm kiếm tiếng Việt nên kiểm chỗ này, vì một từ bị đổi có thể làm kết quả sai mà không báo lỗi.
**Bối cảnh:** Tuỳ chọn restoreForEmbedding gửi câu đã phục hồi dấu cho model nhúng. Ngưỡng tỷ lệ âm tiết có dấu dùng phép so sánh lớn hơn nghiêm ngặt.
**Chuyện gì xảy ra:** Với câu có một trên hai âm tiết có dấu (tỷ lệ 0,5), câu không được coi là có dấu nên đi nhánh phục hồi. Từ không dấu được đổi thành dạng phổ biến hơn trong vault, làm sai nghĩa. Sửa: từ đã gõ dấu không bao giờ đổi; từ không dấu chỉ được khôi phục khi vault không bao giờ viết trần và xác suất đủ ngưỡng. Sau sửa nDCG@5 tổng từ 0,932 lên 0,954, không hạng mục nào tụt, tuỳ chọn bật mặc định.
**Bài học:** Ngưỡng đúng theo spec vẫn có thể sai ở chỗ dựng câu; kiểm bằng test trước khi sửa, đừng đổi ngưỡng để khớp.
**Artefact:** Bảng bật và tắt restoreForEmbedding theo hạng mục.
