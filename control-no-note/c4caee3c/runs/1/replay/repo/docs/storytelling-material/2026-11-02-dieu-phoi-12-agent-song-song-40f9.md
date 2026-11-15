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
hook: "12 agent chạy song song, merge xung đột thì giao lại cho agent"
tension: gap_ma_phai_chon
sides: ["Merge sớm bản nhỏ, Hit@1 từ 0,60 lên 0,93", "Bản sau xung đột bốn file, phải huỷ merge"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án Obsidian Hybrid Search là công cụ tìm kiếm cho vault Obsidian chạy local, và người làm đang điều phối nhiều agent AI song song để hoàn tất một plan. Người làm tin rằng merge một thay đổi nhỏ sớm thì các nhánh sau sẽ tự giải xung đột. Hoá ra thay đổi đó làm test của nhánh khác hỏng, và khi V18 merge thì xung đột ở 4 file, kéo theo một lỗi làm tụt vi-synonym xuống 0,73. Ai điều phối nhiều agent cần biết merge sớm không miễn phí."
audience: dev điều phối nhiều agent AI làm việc song song trên cùng repo
spine_context: Dự án Obsidian Hybrid Search là công cụ tìm kiếm cho vault Obsidian chạy local; người làm đang điều phối nhiều agent AI song song để hoàn tất một plan.
spine_context_lines: [profile, "claude:c4caee3c#L11"]
spine_want: "Hoàn tất các việc trong plan, mỗi việc được merge vào master."
spine_want_lines: ["claude:c4caee3c#L11"]
spine_obstacle: "Nhiều nhánh cùng sửa một số file dùng chung, nên merge xung đột và test của nhánh khác hỏng."
spine_obstacle_lines: ["claude:c4caee3c#L1354", "claude:c4caee3c#L1368"]
spine_turn: "Tưởng merge một thay đổi nhỏ sớm là an toàn, các merge sau sẽ tự giải xung đột; hoá ra thay đổi đó làm test của nhánh khác hỏng, và một lỗi sau merge làm tụt vi-synonym xuống 0,73."
spine_turn_lines: ["claude:c4caee3c#L1284", "claude:c4caee3c#L1381", "claude:c4caee3c#L1470"]
spine_action: "Merge V19 ngay, rồi merge V17 và V18; khi V18 xung đột ở 4 file, huỷ merge và giao lại cho agent V18 giải trên nhánh của nó."
spine_action_lines: ["claude:c4caee3c#L1284", "claude:c4caee3c#L1458"]
spine_outcome: "V18 đạt vi-synonym Hit@5 0,80, vi-abbr 1,00, nDCG@5 tổng 0,909; 400 test xanh sau khi sửa."
spine_outcome_lines: ["claude:c4caee3c#L1424", "claude:c4caee3c#L1478"]
spine_takeaway: Thay đổi nhỏ vẫn có thể làm nhánh khác hỏng; sau mỗi merge cần chạy lại test của các nhánh còn lại.
spine_takeaway_lines: ["claude:c4caee3c#L1381", "claude:c4caee3c#L1470"]
completeness: 7
---

# Điều phối 12 agent song song: xung đột merge và giao lại cho agent tự giải

**Góc kể:** Dự án Obsidian Hybrid Search là công cụ tìm kiếm cho vault Obsidian chạy local, và người làm đang điều phối nhiều agent AI song song để hoàn tất một plan. Người làm tin rằng merge một thay đổi nhỏ sớm thì các nhánh sau sẽ tự giải xung đột. Hoá ra thay đổi đó làm test của nhánh khác hỏng, và khi V18 merge thì xung đột ở 4 file, kéo theo một lỗi làm tụt vi-synonym xuống 0,73. Ai điều phối nhiều agent cần biết merge sớm không miễn phí.
**Bối cảnh:** Các việc V17 đến V25 mỗi việc một worktree, nhưng nhiều việc cùng sửa query.ts, index.ts và README của gói.
**Chuyện gì xảy ra:** Merge V19 trước vì diff nhỏ, vi-alias Hit@1 tăng từ 0,60 lên 0,93. Sau đó V17 hỏng test vì thiếu trường mới. V18 xung đột ở bốn file, lead huỷ merge và giao chính agent V18 merge master vào nhánh của nó, rồi chạy lại eval. Khi người dùng hỏi 'push chưa', lead trả lời master đã bằng origin, phần còn lại thuộc agent đang chạy. Khi người dùng bảo bật agent làm việc không cần đợi, lead mở thêm các việc không phụ thuộc.
**Bài học:** Bắt agent merge master trước khi bàn giao. Merge từng nhánh nhỏ sớm để giảm xung đột.
