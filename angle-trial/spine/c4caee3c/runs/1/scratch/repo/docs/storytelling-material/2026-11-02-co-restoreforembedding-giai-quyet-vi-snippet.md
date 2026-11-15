---
id: 2026-11-02-co-restoreforembedding-giai-quyet-vi-snippet
date: 2026-11-02
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, số trước sau]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L2919", "claude:c4caee3c#L2927", "claude:c4caee3c#L2951"]
hook: "Một cờ mặc định bật đưa note đích lên hạng 1, không sửa mã"
tension: it_ma_nhieu
sides: ["Không sửa dòng mã nào", "vi-snippet từ 14/15 lên 15/15, note đích lên hạng 1 với điểm 1,000"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Obsidian Hybrid Search là npm package tìm ghi chú Obsidian theo nghĩa và từ khoá, chạy local, và người làm đang đưa nhóm truy vấn tiếng Việt vi-snippet lên 15/15 trên cổng chất lượng. Người làm tin phải sửa thuật toán xếp hạng, nhưng khi gộp nhánh master thì một cờ mặc định (restoreForEmbedding) đã đưa đúng ghi chú lên hạng 1, không cần sửa mã. Người dùng tìm kiếm tiếng Việt nên quan tâm vì lỗi này nằm ở bước chọn ứng viên chứ không ở thuật toán. Bài học: kiểm nhánh nào đang thiếu ứng viên trước khi chỉnh thuật toán."
audience: dev làm tìm kiếm tiếng Việt cho ghi chú và tài liệu
spine_context: "Obsidian Hybrid Search là npm package tìm ghi chú Obsidian theo nghĩa và từ khoá, chạy local. Người làm đang đưa nhóm truy vấn tiếng Việt vi-snippet lên đạt 15/15 trên cổng chất lượng."
spine_context_lines: [profile]
spine_want: Muốn cổng vi-snippet đạt 15/15 mà không làm xấu các nhóm khác.
spine_want_lines: ["claude:c4caee3c#L2919"]
spine_obstacle: "Truy vấn vi-snippet-08 không đưa được ghi chú đích vào nhánh vector, vì bộ embedding nhận câu không dấu \"quen ngu\"."
spine_obstacle_lines: ["claude:c4caee3c#L2919"]
spine_turn: Tưởng phải sửa thuật toán xếp hạng hoặc trọng số; hoá ra một cờ mặc định đã bật khi gộp master là đủ.
spine_turn_lines: ["claude:c4caee3c#L2919", "claude:c4caee3c#L2927"]
spine_action: "Gộp master vào nhánh, không sửa dòng mã nào."
spine_action_lines: ["claude:c4caee3c#L2927", "claude:c4caee3c#L2928"]
spine_outcome: "vi-snippet đạt 15/15, nDCG@5 tổng 0,944; vi-alias giảm 0,016 nhưng còn trong ngưỡng 0,02. Nhánh chưa merge được vì file review đang bị agent khác sửa."
spine_outcome_lines: ["claude:c4caee3c#L2927", "claude:c4caee3c#L2929"]
spine_takeaway: "Trước khi sửa thuật toán, kiểm nhánh nào đang thiếu ứng viên; một cờ đúng có thể là đủ."
spine_takeaway_lines: ["claude:c4caee3c#L2919"]
completeness: 7
---

# Cờ restoreForEmbedding giải quyết vi-snippet mà không cần sửa mã

**Góc kể:** Obsidian Hybrid Search là npm package tìm ghi chú Obsidian theo nghĩa và từ khoá, chạy local, và người làm đang đưa nhóm truy vấn tiếng Việt vi-snippet lên 15/15 trên cổng chất lượng. Người làm tin phải sửa thuật toán xếp hạng, nhưng khi gộp nhánh master thì một cờ mặc định (restoreForEmbedding) đã đưa đúng ghi chú lên hạng 1, không cần sửa mã. Người dùng tìm kiếm tiếng Việt nên quan tâm vì lỗi này nằm ở bước chọn ứng viên chứ không ở thuật toán. Bài học: kiểm nhánh nào đang thiếu ứng viên trước khi chỉnh thuật toán.
**Bối cảnh:** Một câu snippet không đưa note đích vào nhánh vector.
**Chuyện gì xảy ra:** Nguyên nhân: embedder nhận câu không dấu nên note đích không vào nhánh vector. Khi cờ mặc định bật, note đích lên hạng 1 với điểm 1,000, note kế tiếp 0,910. vi-snippet từ 14/15 lên 15/15. vi-alias giảm 0,016 nhưng vẫn trong ngưỡng cổng.
**Bài học:** Trước khi sửa thuật toán, kiểm nhánh nào đang thiếu ứng viên; một cờ đúng có thể là đủ.
**Artefact:** Đầu ra explain theo từng nhánh, đã che nội dung.
