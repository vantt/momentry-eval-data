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
lines: ["claude:c4caee3c#L1281", "claude:c4caee3c#L2095", "claude:c4caee3c#L2129", "claude:c4caee3c#L2160"]
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
angle: "Obsidian Hybrid Search là công cụ tìm kiếm cho vault Obsidian, và đang cố hoàn tất roadmap trong khi giữ tài liệu đặc tả khớp với code. PRD ghi phải chạy cả hai view chuẩn hoá cho câu có dấu, nhưng số đo cho thấy làm vậy khiến vi-semantic tụt 0,083 nDCG@5. Người nghe nên để ý vì khi spec và số đo mâu thuẫn, cách đúng là đưa số liệu cho người quyết rồi sửa spec, đừng để hai bên lệch nhau."
audience: dev viết spec cho công cụ tìm kiếm tiếng Việt
spine_context: "Obsidian Hybrid Search là công cụ tìm kiếm cho vault Obsidian theo nghĩa và từ khoá, đang hoàn tất roadmap plan."
spine_context_lines: [profile, "claude:c4caee3c#L11"]
spine_want: "Hoàn tất plan roadmap, và để PRD khớp với code."
spine_want_lines: ["claude:c4caee3c#L11"]
spine_obstacle: "Bật cả hai view chuẩn hoá cho câu có dấu làm vi-semantic tụt 0,083 nDCG@5."
spine_obstacle_lines: ["claude:c4caee3c#L1264", "claude:c4caee3c#L2095"]
spine_turn: "PRD 10.3 ghi phải chạy cả hai view cho câu có dấu; số đo cho thấy làm vậy làm kém đi, nên code mặc định tắt và PRD phải đổi theo."
spine_turn_lines: ["claude:c4caee3c#L2095", "claude:c4caee3c#L2129"]
spine_action: "Đưa lựa chọn có số liệu cho người dùng; người dùng chọn giữ cách của V13, rồi PRD 10.3 được sửa cho khớp."
spine_action_lines: ["claude:c4caee3c#L2095", "claude:c4caee3c#L2096", "claude:c4caee3c#L2129"]
spine_outcome: "PRD và code khớp nhau, sửa trong commit abce8d2."
spine_outcome_lines: ["claude:c4caee3c#L2155", "claude:c4caee3c#L2160"]
spine_takeaway: "Khi số đo cho thấy spec sai, đưa lựa chọn có số liệu cho người quyết và sửa spec theo quyết định, đừng để code và spec lệch nhau."
spine_takeaway_lines: ["claude:c4caee3c#L1264", "claude:c4caee3c#L2095"]
completeness: 7
---

# PRD ghi chạy cả hai view cho câu có dấu, code thì không; người dùng chọn giữ code và sửa PRD

**Góc kể:** Obsidian Hybrid Search là công cụ tìm kiếm cho vault Obsidian, và đang cố hoàn tất roadmap trong khi giữ tài liệu đặc tả khớp với code. PRD ghi phải chạy cả hai view chuẩn hoá cho câu có dấu, nhưng số đo cho thấy làm vậy khiến vi-semantic tụt 0,083 nDCG@5. Người nghe nên để ý vì khi spec và số đo mâu thuẫn, cách đúng là đưa số liệu cho người quyết rồi sửa spec, đừng để hai bên lệch nhau.
**Bối cảnh:** PRD 10.3 yêu cầu luôn chạy hai view chuẩn hoá và bỏ dấu cho câu có dấu.
**Chuyện gì xảy ra:** Khi bật hai view cho câu có dấu, vi-semantic tụt 0,083 nDCG@5, nên V13 mặc định không chạy chúng; view bỏ dấu vẫn tự bật khi vault có chữ viết không dấu. Agent đưa lựa chọn cho người dùng và người dùng chọn giữ cách của code, rồi PRD được sửa cho khớp.
**Bài học:** Khi số đo cho thấy spec sai, đưa lựa chọn có số liệu cho người quyết và sửa spec theo quyết định, đừng để code và spec lệch nhau.
**Artefact:** Bảng so sánh vi-semantic với và không có hai view.
