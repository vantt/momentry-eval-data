---
id: 2026-11-02-cau-co-dau-giu-view-tat-40f9
code: M-GYSS
aliases: [M-GYSS]
date: 2026-11-02
repo: repo
status: raw
signals: [dao_quyet_dinh, khac]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L1264", "claude:c4caee3c#L2095", "claude:c4caee3c#L2096", "claude:c4caee3c#L2129", "claude:c4caee3c#L2160"]
hook: "Giữ cách làm tắt, sửa PRD cho khớp thay vì sửa mã"
tension: chon_mot_mat_mot
sides: ["Làm đúng PRD 10.3", "Giữ view tắt và sửa PRD cho khớp"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Obsidian Hybrid Search là công cụ tìm ghi chú Obsidian trên máy, và người làm đang cố đưa nó đạt độ chính xác tốt cho tiếng Việt. Tài liệu thiết kế ghi rằng câu tìm có dấu phải chạy thêm hai bước chuẩn hoá. Khi đo, bật hai bước đó làm điểm xếp hạng của nhóm tìm theo ý nghĩa tụt 0,083, nên người làm tắt chúng cho câu có dấu rồi sửa lại tài liệu cho khớp. Ai viết spec cho công cụ có đo chất lượng nên thấy đây là bài học: đo đánh đổi trước khi làm đúng chữ trong tài liệu."
audience: dev làm tìm kiếm hoặc viết spec cho công cụ có đo chất lượng
spine_context: "Obsidian Hybrid Search là công cụ tìm ghi chú Obsidian trên máy, đang được làm để tìm tốt hơn với tiếng Việt."
spine_context_lines: [profile]
spine_want: Đạt mục tiêu G3 cho gói tiếng Việt.
spine_want_lines: ["claude:c4caee3c#L1264"]
spine_obstacle: "PRD 10.3 yêu cầu câu có dấu chạy cả view norm lẫn fold, nhưng bật hai view này làm vi-semantic tụt 0,083 nDCG@5."
spine_obstacle_lines: ["claude:c4caee3c#L2095"]
spine_turn: Tưởng làm đúng PRD 10.3 là đúng; hoá ra làm vậy làm hỏng nhóm vi-semantic.
spine_turn_lines: ["claude:c4caee3c#L1255", "claude:c4caee3c#L2095"]
spine_action: "V13 tắt view cho câu có dấu; người duyệt chọn giữ cách này, rồi PRD 10.3 được sửa cho khớp."
spine_action_lines: ["claude:c4caee3c#L1264", "claude:c4caee3c#L2096", "claude:c4caee3c#L2129"]
spine_outcome: "V13 đã commit 570e77b: vi-unaccented Hit@5 từ 0,27 lên 1,00, vi-dd từ 0,40 lên 1,00, vi-tone-precision MRR đạt 1,00, không hạng mục nào tụt."
spine_outcome_lines: ["claude:c4caee3c#L1264"]
spine_takeaway: "Trước khi làm đúng chữ trong tài liệu, hãy đo đánh đổi trên dữ liệu; rồi sửa tài liệu cho khớp quyết định thật."
spine_takeaway_lines: ["claude:c4caee3c#L2129"]
completeness: 7
---

# Câu có dấu: giữ view tắt và sửa PRD thay vì làm đúng PRD

**Góc kể:** Obsidian Hybrid Search là công cụ tìm ghi chú Obsidian trên máy, và người làm đang cố đưa nó đạt độ chính xác tốt cho tiếng Việt. Tài liệu thiết kế ghi rằng câu tìm có dấu phải chạy thêm hai bước chuẩn hoá. Khi đo, bật hai bước đó làm điểm xếp hạng của nhóm tìm theo ý nghĩa tụt 0,083, nên người làm tắt chúng cho câu có dấu rồi sửa lại tài liệu cho khớp. Ai viết spec cho công cụ có đo chất lượng nên thấy đây là bài học: đo đánh đổi trước khi làm đúng chữ trong tài liệu.
**Bối cảnh:** PRD 10.3 ghi câu có dấu vẫn chạy cả view norm lẫn fold. Agent đã tắt, vì bật lên thì vi-semantic tụt 0,083 nDCG@5.
**Chuyện gì xảy ra:** Lead đề xuất giữ cách của V13 và sửa PRD 10.3 cho khớp. Người dùng chọn đúng phương án này sau một câu hỏi lựa chọn. Hai tuỳ chọn accentedNorm và accentedFold vẫn còn để bật lại khi cần.
**Bài học:** Khi một thay đổi làm hỏng một hạng mục, đo đánh đổi rồi để người duyệt chọn. Sau đó sửa tài liệu cho khớp quyết định thật.
