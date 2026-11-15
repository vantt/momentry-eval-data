---
id: 2026-11-02-prd-ghi-chay-ca-hai-view-40f9
code: M-6EAR
aliases: [M-6EAR]
date: 2026-11-02
repo: repo
status: raw
signals: [khac, dao_quyet_dinh]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L2095", "claude:c4caee3c#L2129", "claude:c4caee3c#L2160"]
hook: "PRD ghi một đằng, code làm một nẻo, và code mới đúng"
tension: tuong_ma_hoa_ra
sides: ["Tài liệu nói chạy cả hai view", "Bật cả hai làm điểm tụt 0,083"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# PRD ghi chạy cả hai view cho câu có dấu, code thì không; người dùng chọn giữ code và sửa PRD

**Bối cảnh:** PRD 10.3 yêu cầu luôn chạy hai view chuẩn hoá và bỏ dấu cho câu có dấu.
**Chuyện gì xảy ra:** Khi bật hai view cho câu có dấu, vi-semantic tụt 0,083 nDCG@5, nên V13 mặc định không chạy chúng; view bỏ dấu vẫn tự bật khi vault có chữ viết không dấu. Agent đưa lựa chọn cho người dùng và người dùng chọn giữ cách của code, rồi PRD được sửa cho khớp.
**Bài học:** Khi số đo cho thấy spec sai, đưa lựa chọn có số liệu cho người quyết và sửa spec theo quyết định, đừng để code và spec lệch nhau.
**Artefact:** Bảng so sánh vi-semantic với và không có hai view.
