---
id: 2026-11-02-phuc-hoi-dau-sai-voi-hoi
date: 2026-11-02
repo: repo
status: raw
signals: [Nguyên nhân bất ngờ, "Số trước, số sau"]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L2787", "claude:c4caee3c#L2789", "claude:c4caee3c#L2842"]
hook: "Ngưỡng đúng PRD, vậy mà 'Hội An' thành 'Hội ăn'"
tension: tuong_ma_hoa_ra
sides: ["Ai cũng nghĩ ngưỡng 50% sai", "Lỗi nằm ở câu gửi cho model nhúng"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Phục hồi dấu sai với 'Hội An': lỗi nằm ở cách dựng câu, không ở ngưỡng

**Bối cảnh:** Câu có dấu một phần: 1/2 âm tiết có dấu, tỉ lệ 0,5 không vượt ngưỡng '>' nên đi nhánh phục hồi.
**Chuyện gì xảy ra:** 'An' bị phục hồi thành 'ăn', từ hay gặp hơn trong vault. Ngưỡng 50% đúng PRD, lỗi là câu gửi cho model nhúng. Sửa: từ gõ có dấu giữ nguyên, từ không dấu chỉ được phục hồi khi vault không bao giờ viết trần và xác suất đủ cao. nDCG@5 tổng 0,932 → 0,954, bật mặc định.
**Bài học:** Trước khi đổi ngưỡng, kiểm xem lỗi có nằm ở điều kiện chọn nhánh không.
**Artefact:** Ví dụ 'Hội An' → 'hội ăn' (từ mẫu công khai, không có dữ liệu vault).
