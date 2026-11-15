---
id: 2026-11-02-cham-mu-nguoi-cham-may-khong-40f9
code: M-GWJ2
aliases: [M-GWJ2]
date: 2026-11-02
repo: repo
status: raw
signals: [khac]
signal_note: Quy trình chấm mù tách đáp án khỏi người chấm máy để tránh thiên kiến khi so sánh hai bản.
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L1892", "claude:c4caee3c#L1959", "claude:c4caee3c#L1972"]
hook: "Chấm mù: agent chấm trước, giải mã đáp án sau"
tension: khac
sides: ["Agent là người chấm", "Không được nhìn đáp án trước khi chấm"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Chấm mù: người chấm máy không xem đáp án

**Bối cảnh:** Báo cáo review upstream so sánh cặp kết quả A và B, và cần biết cặp nào là bản nào.
**Chuyện gì xảy ra:** Script sinh cặp A/B và ghi đáp án vào file riêng. Agent chấm cặp mà không mở file đáp án, rồi mới giải mã. Với bản nâng v0.17.1 lên v0.17.2, upstream chỉ nâng phụ thuộc, không đổi mã nguồn, và cả 8 bản vá đều áp được trên hai tag. Mọi probe trên upstream trả 1, trên fork trả 0. Báo cáo cuối vẫn đang được viết khi phiên dừng.
**Bài học:** Tách đáp án khỏi bước chấm, và ghi rõ bước nào đã làm, bước nào còn dở.
**Artefact:** Mẫu mục báo cáo review (không có nội dung cặp).
