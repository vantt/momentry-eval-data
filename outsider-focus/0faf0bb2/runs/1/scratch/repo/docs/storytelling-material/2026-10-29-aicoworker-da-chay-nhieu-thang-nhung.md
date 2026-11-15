---
id: 2026-10-29-aicoworker-da-chay-nhieu-thang-nhung
date: 2026-10-29
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, khác]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L2226", "claude:0faf0bb2#L2234", "claude:0faf0bb2#L2254"]
hook: "AICoworker chạy nhiều tháng, nhiều cơ chế tự học, agent main chưa có MEMORY.md"
tension: tuong_ma_hoa_ra
sides: ["Có bộ nhớ, skill-creator, self-patch, advisor", "Agent main chưa có nổi một file MEMORY.md"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# AICoworker đã chạy nhiều tháng nhưng agent main chưa có MEMORY.md nào

**Bối cảnh:** Người dùng nhận xét AICoworker là loại tự cải tiến. Mình kiểm tra các cơ chế bộ nhớ và skill-creator xem có thật không.
**Chuyện gì xảy ra:** AICoworker có nhiều cơ chế tự cải tiến gồm bộ nhớ, skill-creator, đúc kết workflow, advisor, self-patch. Nhưng workspace-main của agent main chưa có file MEMORY.md nào, tức là chưa tích lũy bộ nhớ dài hạn. Các cơ chế này chủ yếu bắt đầu từ chat, không có tín hiệu kết quả hay cổng duyệt.
**Bài học:** Có cơ chế tự cải tiến chưa có nghĩa là đang được dùng. Kiểm dấu vết thật, như file bộ nhớ có tồn tại không, trước khi kết luận.
**Artefact:** Cây thư mục workspace-main với các file danh tính, và việc thiếu MEMORY.md.
