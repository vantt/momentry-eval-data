---
id: 2026-11-02-co-restoreforembedding-giai-quyet-vi-snippet-40f9
code: M-44JV
aliases: [M-44JV]
date: 2026-11-02
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, số trước sau]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L2919", "claude:c4caee3c#L2927", "claude:c4caee3c#L2951"]
hook: "Một cờ bật mặc định đưa vi-snippet từ 14/15 lên 15/15, không sửa mã"
tension: it_ma_nhieu
sides: ["không sửa dòng mã nào", "note đích lên hạng 1, vi-snippet đạt 15/15"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Cờ restoreForEmbedding giải quyết vi-snippet mà không cần sửa mã

**Bối cảnh:** Một câu snippet không đưa note đích vào nhánh vector.
**Chuyện gì xảy ra:** Nguyên nhân: embedder nhận câu không dấu nên note đích không vào nhánh vector. Khi cờ mặc định bật, note đích lên hạng 1 với điểm 1,000, note kế tiếp 0,910. vi-snippet từ 14/15 lên 15/15. vi-alias giảm 0,016 nhưng vẫn trong ngưỡng cổng.
**Bài học:** Trước khi sửa thuật toán, kiểm nhánh nào đang thiếu ứng viên; một cờ đúng có thể là đủ.
**Artefact:** Đầu ra explain theo từng nhánh, đã che nội dung.
