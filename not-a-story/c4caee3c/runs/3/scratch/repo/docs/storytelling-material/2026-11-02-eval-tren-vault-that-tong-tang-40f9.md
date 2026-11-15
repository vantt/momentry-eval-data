---
id: 2026-11-02-eval-tren-vault-that-tong-tang-40f9
code: M-49A8
aliases: [M-49A8]
date: 2026-11-02
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L3623", "claude:c4caee3c#L3645", "claude:c4caee3c#L3680", "claude:c4caee3c#L3682", "claude:c4caee3c#L3797", "claude:c4caee3c#L3809"]
hook: "Tổng điểm tăng 0,600 lên 0,698, nhưng có hạng mục tụt 0,260"
tension: chon_mot_mat_mot
sides: ["Tổng nDCG@5 trên vault thật tăng rõ", "Một câu rơi khỏi top 5 kéo hạng mục tụt 0,260"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Eval trên vault thật: tổng tăng nhưng cổng hạng mục đỏ, người dùng chọn dùng gói

**Bối cảnh:** Golden set 61 câu của người dùng nằm ngoài repo. Script chỉ in số tổng hợp, không in câu hỏi hay tên note.
**Chuyện gì xảy ra:** Tổng nDCG@5 trên vault thật tăng từ 0,600 lên 0,698, nhưng vài hạng mục có 2 đến 6 câu bị tụt, có hạng mục tụt 0,260 vì một câu rơi khỏi top 5. Người dùng quyết định dùng gói vi cho bộ cài. Công cụ chi tiết ghi từng câu ra một file ngoài repo và từ chối ghi nếu đường dẫn nằm trong repo.
**Bài học:** Đánh giá trên dữ liệu thật cần công cụ chi tiết nhưng ghi ra nơi riêng tư. Mẫu nhỏ cho biến động lớn, đừng quyết định theo một hạng mục.
**Artefact:** Bảng số tổng hợp theo hạng mục, không có câu hỏi.
