---
id: 2026-11-02-quy-trinh-kiem-tra-thu-cong
date: 2026-11-02
repo: repo
status: raw
signals: []
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L2155", "claude:c4caee3c#L2663", "claude:c4caee3c#L2685"]
hook: "Bỏ lịch tự đuổi theo upstream, ghim v0.17.2 và chỉ đồng bộ khi cần"
tension: giup_ma_hai
sides: ["Tự động đuổi theo upstream để luôn mới", "Ghim một tag, đồng bộ thủ công lại ổn định hơn"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Quy trình kiểm tra thủ công upstream thay cho tự động đuổi theo

**Bối cảnh:** Ban đầu fork tự chạy catchup mỗi 6 giờ để bám theo upstream.
**Chuyện gì xảy ra:** Người duyệt chọn chuyển sang ghim tag upstream trong một file và chỉ đồng bộ khi được yêu cầu. Lịch chạy được bỏ, tag v0.17.2 được ghim, và CI chỉ dựng trên tag đã ghim. Mục tiêu G1 trong PRD được sửa lại theo quyết định này.
**Bài học:** Tự động hoá việc theo dõi upstream có thể không cần thiết khi người duyệt muốn quyền quyết định từng bản.
**Artefact:** Nội dung file ghim gồm một dòng tag, không kèm thêm gì.
