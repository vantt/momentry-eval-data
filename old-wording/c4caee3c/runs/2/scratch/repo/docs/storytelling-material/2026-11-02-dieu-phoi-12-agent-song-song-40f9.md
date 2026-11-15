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
hook: "Điều phối 12 agent song song: một xung đột, lead giao agent tự giải"
tension: hop_ma_tan
sides: ["12 agent chạy song song cho nhanh", "Xung đột bốn file, phải huỷ merge để agent tự giải"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Điều phối 12 agent song song: xung đột merge và giao lại cho agent tự giải

**Bối cảnh:** Các việc V17 đến V25 mỗi việc một worktree, nhưng nhiều việc cùng sửa query.ts, index.ts và README của gói.
**Chuyện gì xảy ra:** Merge V19 trước vì diff nhỏ, vi-alias Hit@1 tăng từ 0,60 lên 0,93. Sau đó V17 hỏng test vì thiếu trường mới. V18 xung đột ở bốn file, lead huỷ merge và giao chính agent V18 merge master vào nhánh của nó, rồi chạy lại eval. Khi người dùng hỏi 'push chưa', lead trả lời master đã bằng origin, phần còn lại thuộc agent đang chạy. Khi người dùng bảo bật agent làm việc không cần đợi, lead mở thêm các việc không phụ thuộc.
**Bài học:** Bắt agent merge master trước khi bàn giao. Merge từng nhánh nhỏ sớm để giảm xung đột.
