---
id: 2026-11-02-doi-cach-theo-doi-upstream-tu-40f9
code: M-BEG6
aliases: [M-BEG6]
date: 2026-11-02
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L2155", "claude:c4caee3c#L2680", "claude:c4caee3c#L2685"]
hook: "Bỏ tự đuổi theo upstream, ghim tag thủ công"
tension: chon_mot_mat_mot
sides: ["Tự động theo kịp upstream", "Ghim tag để tự chủ, đổi lại phải làm tay"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đổi cách theo dõi upstream: từ tự động sang ghim tag thủ công

**Bối cảnh:** Catchup ban đầu chạy theo lịch 6 giờ và tự đuổi theo tag upstream mới.
**Chuyện gì xảy ra:** Người dùng quyết định không tự đuổi theo upstream. CI được đổi sang đọc một file ghim tag, bỏ lịch tự chạy, và chỉ đồng bộ master khi có yêu cầu. Mục G1 trong PRD được sửa theo.
**Bài học:** Khi ràng buộc vận hành đổi, đổi cả mục tiêu trong spec cùng lúc để spec không đòi điều không còn làm.
**Artefact:** Nội dung file ghim tag (chỉ tag, không kèm thông tin khác).
