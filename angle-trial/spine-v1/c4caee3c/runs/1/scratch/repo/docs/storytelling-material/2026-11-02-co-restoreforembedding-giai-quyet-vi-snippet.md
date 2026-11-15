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
angle: "Obsidian Hybrid Search là công cụ tìm ghi chú Obsidian, và nhóm đang chuẩn bị bản phát hành có cổng chất lượng. Một câu tìm kiếm tiếng Việt không đưa được note đúng vào nhánh vector, nên nhóm tin phải sửa thuật toán xếp hạng. Hoá ra một cờ mặc định đã bật khi gộp nhánh master, và note đúng lên hạng 1 mà không cần sửa mã. Ai đang gỡ lỗi tìm kiếm nên kiểm nhánh nào thiếu ứng viên trước khi sửa thuật toán."
audience: dev làm tìm kiếm tiếng Việt hoặc RAG
spine_context: "Obsidian Hybrid Search là công cụ tìm ghi chú Obsidian, và nhóm đang chuẩn bị bản phát hành có cổng chất lượng."
spine_context_lines: [profile, "claude:c4caee3c#L2927"]
spine_want: Muốn cổng vi-snippet đạt 15/15 trước khi phát hành.
spine_want_lines: ["claude:c4caee3c#L2927"]
spine_obstacle: Một câu snippet tiếng Việt không đưa được note đích vào nhánh vector.
spine_obstacle_lines: ["claude:c4caee3c#L2919"]
spine_turn: Tưởng cần sửa thuật toán xếp hạng; hoá ra một cờ mặc định (restoreForEmbedding) đã bật khi gộp master và đủ để sửa.
spine_turn_lines: ["claude:c4caee3c#L2919", "claude:c4caee3c#L2927"]
spine_action: "Gộp master vào nhánh, không sửa dòng mã nào."
spine_action_lines: ["claude:c4caee3c#L2927"]
spine_outcome: "vi-snippet đạt 15/15, nDCG@5 tổng 0,944; vi-alias giảm 0,016 nhưng vẫn trong ngưỡng 0,02; nhánh chưa merge vì còn thay đổi chưa commit."
spine_outcome_lines: ["claude:c4caee3c#L2919", "claude:c4caee3c#L2927", "claude:c4caee3c#L2951"]
spine_takeaway: "Trước khi sửa thuật toán, kiểm nhánh nào đang thiếu ứng viên; một cờ đúng có thể là đủ."
spine_takeaway_lines: ["claude:c4caee3c#L2919"]
completeness: 7
---

# Cờ restoreForEmbedding giải quyết vi-snippet mà không cần sửa mã

**Góc kể:** Obsidian Hybrid Search là công cụ tìm ghi chú Obsidian, và nhóm đang chuẩn bị bản phát hành có cổng chất lượng. Một câu tìm kiếm tiếng Việt không đưa được note đúng vào nhánh vector, nên nhóm tin phải sửa thuật toán xếp hạng. Hoá ra một cờ mặc định đã bật khi gộp nhánh master, và note đúng lên hạng 1 mà không cần sửa mã. Ai đang gỡ lỗi tìm kiếm nên kiểm nhánh nào thiếu ứng viên trước khi sửa thuật toán.
**Bối cảnh:** Một câu snippet không đưa note đích vào nhánh vector.
**Chuyện gì xảy ra:** Nguyên nhân: embedder nhận câu không dấu nên note đích không vào nhánh vector. Khi cờ mặc định bật, note đích lên hạng 1 với điểm 1,000, note kế tiếp 0,910. vi-snippet từ 14/15 lên 15/15. vi-alias giảm 0,016 nhưng vẫn trong ngưỡng cổng.
**Bài học:** Trước khi sửa thuật toán, kiểm nhánh nào đang thiếu ứng viên; một cờ đúng có thể là đủ.
**Artefact:** Đầu ra explain theo từng nhánh, đã che nội dung.
