---
id: 2026-11-02-loi-phuc-hoi-dau-hoi-an
date: 2026-11-02
repo: repo
status: raw
signals: []
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L2787", "claude:c4caee3c#L2789", "claude:c4caee3c#L2842", "claude:c4caee3c#L2919", "claude:c4caee3c#L2927"]
hook: "Máy 'phục hồi dấu' biến Hội An thành 'hội ăn'"
tension: giup_ma_hai
sides: ["Tính năng sinh ra để phục hồi dấu tiếng Việt", "Nó biến địa danh Hội An thành 'hội ăn'"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Lỗi phục hồi dấu 'Hội An' thành 'hội ăn' và vì sao bật mặc định

**Bối cảnh:** Tuỳ chọn restoreForEmbedding đưa câu đã phục hồi dấu cho model nhúng. Câu có một nửa syllable có dấu không được coi là câu có dấu.
**Chuyện gì xảy ra:** Với Hội An, Hội giữ nguyên nhưng An bị phục hồi thành ăn, vì ăn phổ biến hơn trong vault. Agent chứng minh bằng test mới thất bại trên mã cũ, rồi sửa: từ đã gõ dấu không bao giờ đổi, và từ không dấu chỉ được phục hồi khi vault không bao giờ viết trần và độ tin cậy đủ cao. Sau sửa, nDCG@5 tổng tăng từ 0,932 lên 0,954 khi bật. Cùng lúc, vi-snippet từ 14/15 lên 15/15 chỉ vì tuỳ chọn này đã bật mặc định, không cần sửa xếp hạng.
**Bài học:** Một lỗi tưởng là lỗi xếp hạng có thể thật ra là lỗi dựng câu truy vấn; hãy xem lại đầu vào trước khi chỉnh thuật toán.
**Artefact:** Cặp câu Hội An trước và sau khi phục hồi, kèm bảng nDCG theo hạng mục.
