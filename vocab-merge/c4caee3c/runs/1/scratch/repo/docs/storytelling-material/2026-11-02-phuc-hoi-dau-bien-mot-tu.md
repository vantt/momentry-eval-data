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
---

# Phục hồi dấu biến một từ không dấu thành từ khác trong câu có dấu một phần

**Bối cảnh:** Tuỳ chọn restoreForEmbedding gửi câu đã phục hồi dấu cho model nhúng. Ngưỡng tỷ lệ âm tiết có dấu dùng phép so sánh lớn hơn nghiêm ngặt.
**Chuyện gì xảy ra:** Với câu có một trên hai âm tiết có dấu (tỷ lệ 0,5), câu không được coi là có dấu nên đi nhánh phục hồi. Từ không dấu được đổi thành dạng phổ biến hơn trong vault, làm sai nghĩa. Sửa: từ đã gõ dấu không bao giờ đổi; từ không dấu chỉ được khôi phục khi vault không bao giờ viết trần và xác suất đủ ngưỡng. Sau sửa nDCG@5 tổng từ 0,932 lên 0,954, không hạng mục nào tụt, tuỳ chọn bật mặc định.
**Bài học:** Ngưỡng đúng theo spec vẫn có thể sai ở chỗ dựng câu; kiểm bằng test trước khi sửa, đừng đổi ngưỡng để khớp.
**Artefact:** Bảng bật và tắt restoreForEmbedding theo hạng mục.
