---
id: 2026-11-02-eval-vault-that-cho-thay-goi
date: 2026-11-02
repo: repo
status: raw
signals: ["Số trước, số sau", Người duyệt thứ máy soạn]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L3623", "claude:c4caee3c#L3645", "claude:c4caee3c#L3680", "claude:c4caee3c#L3682", "claude:c4caee3c#L3809"]
hook: "Tổng điểm tăng 0,600 lên 0,698 nhưng 4 hạng mục tụt"
tension: hop_ma_tan
sides: ["Gói tiếng Việt kéo điểm tổng tăng gần 0,1", "Hạng mục vi-iy tụt 0,260 chỉ vì một câu rơi top 5"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Eval vault thật cho thấy gói tiếng Việt tụt ở vài hạng mục dù tổng tăng

**Bối cảnh:** Golden set 61 câu viết bởi người dùng trên vault thật, đặt ngoài repo; đo bằng quality-gate --private.
**Chuyện gì xảy ra:** Tổng nDCG@5 tăng từ 0,600 lên 0,698 với gói vi, nhưng cổng theo hạng mục hỏng: vi-iy giảm 0,260 (một câu rơi khỏi top 5), vi-accented −0,052, vi-compound −0,041, vi-synonym −0,167 vì vault chưa có lexicon. Mỗi hạng mục chỉ 2–6 câu. Người dùng quyết dùng gói vi cho bộ cài, và thêm việc V15b: chế độ --private-detail ghi từng câu ra file ngoài repo, có guard chặn ghi trong repo.
**Bài học:** Cổng theo hạng mục với 2–6 câu mỗi nhóm rất nhiễu; tổng và chi tiết từng câu cần đọc cùng nhau trước khi quyết.
**Artefact:** Bảng nDCG@5 theo hạng mục trên vault (che toàn bộ câu hỏi và tên note).
