---
id: 2026-11-02-sua-thu-hang-snippet-14-15-40f9
code: M-95DP
aliases: [M-95DP]
date: 2026-11-02
repo: repo
status: raw
signals: [khac, nguyen_nhan_bat_ngo]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L2927", "claude:c4caee3c#L2951"]
hook: "Snippet từ 14/15 lên 15/15 mà không sửa dòng mã nào"
tension: it_ma_nhieu
sides: ["Tưởng phải sửa mã", "Chỉ cần merge tuỳ chọn khác là đạt"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án là một gói npm tìm ghi chú Obsidian theo nghĩa và từ khoá, và người làm đang gộp các nhánh cải thiện để phát hành. Một ca tiếng Việt không đạt cổng chất lượng vi-snippet vì ghi chú đích rơi xuống hạng 11. Người làm nghi lỗi nằm ở khôi phục dấu hay cách chấm lại, nhưng hoá ra nhánh đo chạy khi tuỳ chọn khôi phục dấu còn tắt. Gộp master đã bật tuỳ chọn đó, cổng đạt 15/15 mà không sửa dòng mã nào, và người làm nên kiểm cấu hình trước khi sửa thuật toán."
audience: dev dùng AI viết test và công cụ tìm kiếm
spine_context: "Một gói npm tìm ghi chú Obsidian theo nghĩa, từ khoá, tiêu đề, thẻ và liên kết; người làm đang gộp các nhánh cải thiện để phát hành."
spine_context_lines: [profile]
spine_want: Muốn cổng vi-snippet đạt 15/15 trước khi gộp nhánh.
spine_want_lines: ["claude:c4caee3c#L2919"]
spine_obstacle: "Ghi chú đích rơi xuống hạng 11 khi gộp kết quả, nên không đạt cổng vi-snippet."
spine_obstacle_lines: ["claude:c4caee3c#L2919"]
spine_turn: Tưởng lỗi nằm ở khôi phục dấu hoặc cách chấm lại; hoá ra nhánh đo còn chạy với tuỳ chọn khôi phục dấu tắt.
spine_turn_lines: ["claude:c4caee3c#L2919", "claude:c4caee3c#L2927"]
spine_action: "Gộp master vào nhánh, không sửa dòng mã nào."
spine_action_lines: ["claude:c4caee3c#L2927"]
spine_outcome: "Cổng vi-snippet đạt 15/15; nDCG@5 tổng 0,944; vi-alias giảm 0,016 nhưng còn trong ngưỡng 0,02."
spine_outcome_lines: ["claude:c4caee3c#L2919", "claude:c4caee3c#L2927"]
spine_takeaway: "Trước khi sửa thuật toán vì một ca lỗi, kiểm xem nhánh đo có đúng cấu hình mới nhất không."
spine_takeaway_lines: ["claude:c4caee3c#L2919"]
completeness: 7
---

# Sửa thứ hạng snippet 14/15 thành 15/15 mà không đổi dòng mã nào

**Góc kể:** Dự án là một gói npm tìm ghi chú Obsidian theo nghĩa và từ khoá, và người làm đang gộp các nhánh cải thiện để phát hành. Một ca tiếng Việt không đạt cổng chất lượng vi-snippet vì ghi chú đích rơi xuống hạng 11. Người làm nghi lỗi nằm ở khôi phục dấu hay cách chấm lại, nhưng hoá ra nhánh đo chạy khi tuỳ chọn khôi phục dấu còn tắt. Gộp master đã bật tuỳ chọn đó, cổng đạt 15/15 mà không sửa dòng mã nào, và người làm nên kiểm cấu hình trước khi sửa thuật toán.
**Bối cảnh:** Sau khi merge nhánh từ điển, cổng vi-snippet chỉ đạt 14/15 vì một câu rơi khỏi top 10. Lead đã giao một agent tìm cách sửa thứ hạng bằng cơ chế chung.
**Chuyện gì xảy ra:** Agent phát hiện không cần sửa mã: nhánh từ điển được tạo khi tuỳ chọn khôi phục dấu còn tắt, nên embedder nhận câu không dấu và note đích không vào nhánh vector. Khi merge tuỳ chọn đã bật mặc định, note đích lên hạng 1 và cổng đạt 15/15. Đổi lại vi-alias giảm 0,016 nhưng vẫn trong ngưỡng 0,02.
**Bài học:** Trước khi sửa thuật toán vì một ca lỗi, kiểm xem nhánh đang đo có đúng cấu hình mới nhất không; ca lỗi có thể đã được sửa bởi một thay đổi khác.
**Artefact:** Bảng nDCG@5 theo hạng mục giữa các nhánh (không kèm câu hỏi thật).
