---
id: 2026-11-02-tu-theo-upstream-roi-chuyen-sang-40f9
code: M-ZCWF
aliases: [M-ZCWF]
date: 2026-11-02
repo: repo
status: raw
signals: [dao_quyet_dinh]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L2155", "claude:c4caee3c#L2663", "claude:c4caee3c#L2685", "claude:c4caee3c#L2694"]
hook: "Chủ dự án thôi đuổi theo upstream, ghim tag bằng tay"
tension: chon_mot_mat_mot
sides: ["Tự động theo kịp upstream", "Bản dựng ổn định trên tag ghim"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Tự theo upstream rồi chuyển sang ghim tag bằng tay

**Bối cảnh:** Ban đầu CI tự đuổi theo upstream mỗi 6 giờ và tự dựng bản mới.
**Chuyện gì xảy ra:** Chủ dự án quyết định không tự đuổi nữa. Fork chỉ dựng trên tag được ghim trong một file. Lịch chạy định kỳ bị bỏ, đồng bộ master chỉ chạy khi có yêu cầu. Tiêu chí G1 trong PRD được sửa lại theo quyết định này, và secret cần cho đồng bộ tự động không còn cần thiết.
**Bài học:** Tự động theo upstream nghe hấp dẫn nhưng tăng gánh bảo trì. Khi người dùng cần kiểm soát thời điểm nâng cấp, ghim tag là đủ.
**Artefact:** Dòng PRD trước và sau khi đổi (không nhạy cảm).
