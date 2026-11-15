---
id: 2026-11-02-dieu-phoi-12-agent-song-song-40f9
code: M-6TBM
aliases: [M-6TBM]
date: 2026-11-02
repo: repo
status: raw
signals: [rang_buoc_thiet_ke, khac, nguoi_duyet_may_soan]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L1283", "claude:c4caee3c#L1285", "claude:c4caee3c#L1354", "claude:c4caee3c#L1368", "claude:c4caee3c#L1426", "claude:c4caee3c#L1434", "claude:c4caee3c#L1445", "claude:c4caee3c#L1458", "claude:c4caee3c#L2054", "claude:c4caee3c#L3055"]
hook: "12 agent chạy song song: một merge hỏng test, một xung đột bốn file"
tension: gap_ma_phai_chon
sides: ["Merge nhanh các nhánh để tiến độ không dừng", "Xung đột bốn file buộc huỷ merge và giao agent tự giải"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án là công cụ tìm kiếm cho vault Obsidian, và người làm đang gộp nhiều nhánh tính năng tiếng Việt vào bản fork bằng nhiều agent chạy song song. Sau khi gộp nhánh sửa gõ sai, từ đồng nghĩa tụt Hit@5 từ 0,80 xuống 0,73 vì bộ sửa gõ chạy trước từ điển, nên từ người dùng gõ không còn khớp. Người làm sửa để từ điển xét cả câu gốc, và Hit@5 về 0,80. Người làm công cụ có bước xử lý nối tiếp nên cần chạy eval sau khi gộp, không chỉ test."
audience: dev làm công cụ tìm kiếm hoặc pipeline xử lý truy vấn nhiều bước
spine_context: "Dự án là công cụ tìm kiếm cho vault Obsidian, đang được gộp thành bản fork có gói tiếng Việt, với nhiều agent chạy song song."
spine_context_lines: [profile, "claude:c4caee3c#L11"]
spine_want: "Hoàn tất roadmap của fork, gồm gói tiếng Việt và các nhánh tính năng."
spine_want_lines: ["claude:c4caee3c#L11"]
spine_obstacle: "Nhiều nhánh cùng sửa query.ts, index.ts và README nên khi gộp thường xung đột."
spine_obstacle_lines: ["claude:c4caee3c#L1354", "claude:c4caee3c#L1426"]
spine_turn: Tưởng gộp hai nhánh xong là ổn; hoá ra bộ sửa gõ sai chạy trước từ điển đồng nghĩa nên từ người dùng gõ bị đổi trước khi từ điển kịp thấy.
spine_turn_lines: ["claude:c4caee3c#L1470"]
spine_action: "Cho từ điển xét cả câu gốc chưa qua sửa gõ, cho bộ sửa gõ coi từ người dùng gõ là từ đã biết, thêm test rồi chạy lại eval."
spine_action_lines: ["claude:c4caee3c#L1470"]
spine_outcome: "vi-synonym Hit@5 về 0,80; nDCG@5 tổng lên 0,909."
spine_outcome_lines: ["claude:c4caee3c#L1478"]
spine_takeaway: "Sau khi gộp nhánh cần chạy eval chứ không chỉ test: lỗi thứ tự giữa hai bước xử lý chỉ lộ qua chất lượng tìm kiếm."
spine_takeaway_lines: ["claude:c4caee3c#L1470"]
completeness: 7
---

# Điều phối 12 agent song song: xung đột merge và giao lại cho agent tự giải

**Góc kể:** Dự án là công cụ tìm kiếm cho vault Obsidian, và người làm đang gộp nhiều nhánh tính năng tiếng Việt vào bản fork bằng nhiều agent chạy song song. Sau khi gộp nhánh sửa gõ sai, từ đồng nghĩa tụt Hit@5 từ 0,80 xuống 0,73 vì bộ sửa gõ chạy trước từ điển, nên từ người dùng gõ không còn khớp. Người làm sửa để từ điển xét cả câu gốc, và Hit@5 về 0,80. Người làm công cụ có bước xử lý nối tiếp nên cần chạy eval sau khi gộp, không chỉ test.
**Bối cảnh:** Các việc V17 đến V25 mỗi việc một worktree, nhưng nhiều việc cùng sửa query.ts, index.ts và README của gói.
**Chuyện gì xảy ra:** Merge V19 trước vì diff nhỏ, vi-alias Hit@1 tăng từ 0,60 lên 0,93. Sau đó V17 hỏng test vì thiếu trường mới. V18 xung đột ở bốn file, lead huỷ merge và giao chính agent V18 merge master vào nhánh của nó, rồi chạy lại eval. Khi người dùng hỏi 'push chưa', lead trả lời master đã bằng origin, phần còn lại thuộc agent đang chạy. Khi người dùng bảo bật agent làm việc không cần đợi, lead mở thêm các việc không phụ thuộc.
**Bài học:** Bắt agent merge master trước khi bàn giao. Merge từng nhánh nhỏ sớm để giảm xung đột.
