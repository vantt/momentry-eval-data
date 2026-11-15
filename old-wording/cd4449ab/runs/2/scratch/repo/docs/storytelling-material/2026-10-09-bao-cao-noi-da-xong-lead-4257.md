---
id: 2026-10-09-bao-cao-noi-da-xong-lead-4257
code: M-Q2RR
aliases: [M-Q2RR]
date: 2026-10-09
repo: repo
status: raw
signals: [khac, nguoi_duyet_may_soan]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest, outsider]
lines: ["omp:cd4449ab#L2024", "omp:cd4449ab#L2025", "omp:cd4449ab#L2026", "omp:cd4449ab#L2053", "omp:cd4449ab#L2079", "omp:cd4449ab#L2122"]
hook: "Agent báo đã xong, nhưng key repository vẫn còn sót"
tension: tuong_ma_hoa_ra
sides: ["báo cáo của agent nói đã xong", "lead kiểm lại thấy key repository và hàm chết còn đó"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án mcp-skill-hub đang làm wave 2 để đơn giản hoá, và một agent làm Phase 4 trong worktree riêng. Agent báo cáo đã bỏ key repository khỏi dữ liệu nguồn, nhưng lead phát hiện skill_add vẫn ghi key này cho skill mới. Khi một báo cáo nói đã sạch, hãy đối chiếu với code ở mọi đường ghi trước khi tin."
audience: dev dùng AI agent làm việc song song trên nhiều worktree
spine_context: Dự án mcp-skill-hub đang làm wave 2 để đơn giản hoá; một agent làm Phase 4 trong worktree riêng.
spine_context_lines: ["omp:cd4449ab#L6"]
spine_want: Lead muốn gộp checkpoint Phase 4 vào main.
spine_want_lines: ["omp:cd4449ab#L2025"]
spine_obstacle: "Lead thấy skill_add.go vẫn ghi key repository vào sources[] cho skill mới."
spine_obstacle_lines: ["omp:cd4449ab#L2025"]
spine_turn: "Báo cáo tưởng key repository đã được bỏ khỏi sources[]; hoá ra skill_add vẫn ghi nó."
spine_turn_lines: ["omp:cd4449ab#L2024", "omp:cd4449ab#L2025"]
spine_action: "Sửa skill_add.go để ghi repo, xoá provDoc không dùng, thêm test rồi commit d646117."
spine_action_lines: ["omp:cd4449ab#L2053", "omp:cd4449ab#L2077", "omp:cd4449ab#L2122"]
spine_outcome: "Commit d646117 với make check xanh (24 package ok, 0 lỗi); lead xác nhận."
spine_outcome_lines: ["omp:cd4449ab#L2122", "omp:cd4449ab#L2123"]
spine_takeaway: "Báo cáo 'đã xong' cần đối chiếu với code ở mọi đường ghi, không chỉ dựa vào test sẵn có."
spine_takeaway_lines: ["omp:cd4449ab#L2025"]
completeness: 7
---

# Báo cáo nói đã xong, lead bắt được key repository còn sót

**Góc kể:** Dự án mcp-skill-hub đang làm wave 2 để đơn giản hoá, và một agent làm Phase 4 trong worktree riêng. Agent báo cáo đã bỏ key repository khỏi dữ liệu nguồn, nhưng lead phát hiện skill_add vẫn ghi key này cho skill mới. Khi một báo cáo nói đã sạch, hãy đối chiếu với code ở mọi đường ghi trước khi tin.
**Bối cảnh:** Báo cáo vòng trước có một khẳng định sai: lead đọc code và thấy skill_add vẫn ghi key repository cho skill mới.
**Chuyện gì xảy ra:** Agent kiểm lại và thấy nhánh ghi repository vẫn còn, cùng một hàm provDoc không dùng. Sửa để ghi repo, xoá code chết và thêm test kiểm tra có repo, không có repository và content_digest. Test trust verdict vẫn giữ nguyên sau sửa.
**Bài học:** Khi báo cáo rằng đã sạch, hãy grep khoá cần loại bỏ trên mọi đường ghi trước khi viết, đừng chỉ tin vào test sẵn có.
**Artefact:** Kết quả grep repository trước và sau khi sửa.
**Góc người ngoài:** cách làm phổ biến là Hầu hết người dùng AI chỉ yêu cầu 'làm tiếp' và chấp nhận kết quả, ít khi yêu cầu bằng chứng từng bước; ở đây khác ở Agent biến mỗi ràng buộc (kiểm tra main, không đụng checkout khác) thành một bước kiểm tra lặp lại được và ghi kết quả vào báo cáo, nên người đọc có thể tự kiểm lại mà không cần tin lời agent.
