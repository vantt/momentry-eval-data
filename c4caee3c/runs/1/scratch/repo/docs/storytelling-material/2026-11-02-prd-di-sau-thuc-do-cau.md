---
id: 2026-11-02-prd-di-sau-thuc-do-cau
date: 2026-11-02
repo: repo
status: raw
signals: [Đảo quyết định có lý do, Người duyệt thứ máy soạn]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L1255", "claude:c4caee3c#L2095", "claude:c4caee3c#L2129", "claude:c4caee3c#L2130"]
hook: "Bật thêm hai view cho câu có dấu làm điểm tụt 0,083"
tension: giup_ma_hai
sides: ["Thêm hai view tìm kiếm cho câu có dấu", "vi-semantic tụt 0,083 nDCG@5"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# PRD đi sau thực đo: câu có dấu không chạy hai view norm và fold

**Bối cảnh:** PRD 10.3 yêu cầu chạy cả hai view cho câu truy vấn có dấu.
**Chuyện gì xảy ra:** Thực đo: bật hai view cho câu có dấu làm vi-semantic tụt 0,083 nDCG@5. Người duyệt chọn giữ cách của gói và sửa PRD 10.3 cho khớp. View fold vẫn tự bật khi vault có chữ viết không dấu.
**Bài học:** Khi đo cho thấy spec sai, sửa spec và ghi lý do thay vì ép thực thi theo spec.
**Artefact:** Bảng vi-semantic trước và sau.
