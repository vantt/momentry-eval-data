---
id: 2026-10-09-bao-cao-noi-xong-code-van-4257
code: M-7RDJ
aliases: [M-7RDJ]
date: 2026-10-09
repo: repo
status: raw
signals: [khac]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest, outsider]
lines: ["omp:cd4449ab#L1712", "omp:cd4449ab#L2025", "omp:cd4449ab#L2053", "omp:cd4449ab#L2110"]
hook: "Báo cáo nói xong, nhưng code vẫn ghi key cũ 'repository'"
tension: tuong_ma_hoa_ra
sides: ["Báo cáo nói đã chuyển sang key mới", "Code vẫn ghi 'repository', chủ phải tự bắt"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án mcp-skill-hub đang làm đợt 2, và một worktree đang làm Phase 4 đổi cách ghi skill sang key mới 'repo'. Báo cáo nói mọi chỗ ghi đã chuyển xong, nhưng skill_add vẫn ghi 'repository' cho skill mới: báo cáo sai, code chưa đổi. Ai nhận báo cáo AI cần biết câu 'đã xong' phải được đối chiếu với code, không chỉ tin tóm tắt."
audience: dev dùng AI để viết và review code
spine_context: "Dự án mcp-skill-hub, worktree C đang làm Phase 4 của đợt 2: đổi cách ghi skill sang key mới."
spine_context_lines: ["omp:cd4449ab#L6"]
spine_want: Muốn Phase 4 đạt chuẩn để lead merge vào main trước khi làm Phase 3.
spine_want_lines: ["omp:cd4449ab#L2025"]
spine_obstacle: "Báo cáo nói mọi chỗ ghi đã chuyển, nhưng skill_add vẫn ghi 'repository' cho skill mới."
spine_obstacle_lines: ["omp:cd4449ab#L2025"]
spine_turn: "Tưởng báo cáo đã đúng; hoá ra skill_add vẫn ghi key cũ, nên câu 'đã xong' sai."
spine_turn_lines: ["omp:cd4449ab#L2024", "omp:cd4449ab#L2025"]
spine_action: "Sửa skill_add ghi 'repo', xoá đường dẫn provDoc không dùng, thêm test kiểm tra không còn 'repository'."
spine_action_lines: ["omp:cd4449ab#L2053", "omp:cd4449ab#L2110"]
spine_outcome: "Commit d646117, 3 file, +126/−48 dòng."
spine_outcome_lines: ["omp:cd4449ab#L2112"]
spine_takeaway: "Câu 'đã xong' trong báo cáo AI cần được đối chiếu với code, kèm lệnh kiểm chứng."
spine_takeaway_lines: ["omp:cd4449ab#L2025"]
completeness: 7
---

# Báo cáo nói xong, code vẫn ghi key cũ 'repository'

**Góc kể:** Dự án mcp-skill-hub đang làm đợt 2, và một worktree đang làm Phase 4 đổi cách ghi skill sang key mới 'repo'. Báo cáo nói mọi chỗ ghi đã chuyển xong, nhưng skill_add vẫn ghi 'repository' cho skill mới: báo cáo sai, code chưa đổi. Ai nhận báo cáo AI cần biết câu 'đã xong' phải được đối chiếu với code, không chỉ tin tóm tắt.
**Bối cảnh:** Báo cáo phase 4 ghi mọi writer đã chuyển sang repo, nhưng skill_add vẫn ghi key cũ.
**Chuyện gì xảy ra:** Chủ phát hiện skill_add vẫn ghi 'repository' vào sources[] (L2025). Agent sửa sang 'repo', xoá đường dẫn provDoc không dùng và thêm test kiểm tra không còn 'repository' và 'content_digest' (L2110).
**Bài học:** Câu 'đã xong' trong báo cáo cần kèm lệnh grep kiểm chứng, không chỉ tóm tắt.
**Artefact:** Kết quả grep trước và sau sửa; che đường dẫn.
**Góc người ngoài:** cách làm phổ biến là Người dùng thường đọc báo cáo rồi tin, hoặc chỉ mở code khi có lỗi lộ ra khi chạy; ở đây khác ở Báo cáo có bảng, hash và dấu 'đã kiểm chứng', nhưng code vẫn còn key cũ. Người review bắt được bằng cách đối chiếu trực tiếp. Người đọc muốn biết cách làm việc này để tự kiểm báo cáo AI.
