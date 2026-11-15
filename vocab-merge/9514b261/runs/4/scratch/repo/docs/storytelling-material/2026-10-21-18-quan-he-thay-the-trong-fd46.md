---
id: 2026-10-21-18-quan-he-thay-the-trong-fd46
code: M-2JBB
aliases: [M-2JBB]
date: 2026-10-21
repo: repo
status: raw
signals: [số trước sau, nguyên nhân bất ngờ]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L1116", "claude:9514b261#L1121", "claude:9514b261#L1220", "claude:9514b261#L1230", "claude:9514b261#L1237"]
hook: "18 quan hệ thay thế trong log, chỉ 8 có relation thật"
tension: tuong_ma_hoa_ra
sides: ["log ghi 18 quyết định thay thế", "chỉ 8 có relation, 5 trong 7 cặp chỉ thay một phần"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# 18 quan hệ thay thế trong log nhưng chỉ 8 có relation, và 5 trong 7 cặp ghi được chỉ thay một phần

**Bối cảnh:** Đề xuất đòi một reducer tính tập quyết định hiệu lực. Agent cần biết dữ liệu hiện có đủ để reducer dựa vào không.
**Chuyện gì xảy ra:** Trong events có 36 quyết định D-ADR và 18 quan hệ supersedes, nhưng chỉ 8 có relation kiểu supersedes. Khi đối chiếu index, 7 cặp ghi được và 5 trong số đó chỉ thay một phần. Ít nhất 4 quyết định thay thế chỉ nói trong câu chữ, không có quan hệ. Một đích thay thế còn là mã băm tài liệu, không phải quyết định.
**Bài học:** Đếm quan hệ đã ghi trong dữ liệu trước khi thiết kế một reducer dựa trên chúng.
**Artefact:** Bảng đếm: quan hệ có ghi, thiếu, chỉ thay một phần.
