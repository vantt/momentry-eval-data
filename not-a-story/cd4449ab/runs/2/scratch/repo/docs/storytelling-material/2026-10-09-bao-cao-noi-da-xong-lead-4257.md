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
hook: "Agent báo đã xong, nhưng key cũ vẫn còn sót"
tension: tuong_ma_hoa_ra
sides: ["Báo cáo của agent nói đã sửa xong", "Lead kiểm lại vẫn thấy nhánh ghi key cũ và hàm chết"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một dự án skill hub cho AI agent đang gom việc đơn giản hoá thành nhiều phase, và phase 4 phải qua review trước khi merge. Báo cáo của agent nói đã xong, nhưng khi lead đọc lại, skill_add vẫn ghi key repository vào danh sách nguồn của skill mới, và một khẳng định trong báo cáo là sai. Điều đáng nghe là báo 'đã sạch' chỉ đáng tin khi đã grep khoá đó trên mọi đường ghi."
audience: dev dùng AI agent và muốn biết cách kiểm chứng báo cáo của agent
spine_context: "Một dự án skill hub cho AI agent, đang tách việc đơn giản hoá thành nhiều phase; phase 4 phải qua review trước khi merge."
spine_context_lines: ["omp:cd4449ab#L6"]
spine_want: Muốn phase 4 qua được review và merge vào main.
spine_want_lines: ["omp:cd4449ab#L1462"]
spine_obstacle: Lead chạy thử trên bản sao hub thật và thấy lỗi; báo cáo cũng có một khẳng định sai.
spine_obstacle_lines: ["omp:cd4449ab#L1462", "omp:cd4449ab#L2025"]
spine_turn: "Báo cáo nói đã xong, tưởng không còn ghi key cũ; hoá ra skill_add vẫn ghi key repository vào sources[] của skill mới."
spine_turn_lines: ["omp:cd4449ab#L2024", "omp:cd4449ab#L2025"]
spine_action: "Đổi sang ghi key repo, xoá helper không dùng, thêm test kiểm tra .meta/skill.yaml có repo và không có repository hay content_digest."
spine_action_lines: ["omp:cd4449ab#L2053", "omp:cd4449ab#L2077"]
spine_outcome: "make check xanh ở 24 package, commit d646117; lead xác nhận, trust verdict giữ nguyên."
spine_outcome_lines: ["omp:cd4449ab#L2122", "omp:cd4449ab#L2123"]
spine_takeaway: "Khi báo cáo đã sạch, grep khoá cần bỏ trên mọi đường ghi trước khi viết, đừng chỉ dựa vào test có sẵn."
spine_takeaway_lines: ["omp:cd4449ab#L2025", "omp:cd4449ab#L2029"]
completeness: 7
---

# Báo cáo nói đã xong, lead bắt được key repository còn sót

**Góc kể:** Một dự án skill hub cho AI agent đang gom việc đơn giản hoá thành nhiều phase, và phase 4 phải qua review trước khi merge. Báo cáo của agent nói đã xong, nhưng khi lead đọc lại, skill_add vẫn ghi key repository vào danh sách nguồn của skill mới, và một khẳng định trong báo cáo là sai. Điều đáng nghe là báo 'đã sạch' chỉ đáng tin khi đã grep khoá đó trên mọi đường ghi.
**Bối cảnh:** Báo cáo vòng trước có một khẳng định sai: lead đọc code và thấy skill_add vẫn ghi key repository cho skill mới.
**Chuyện gì xảy ra:** Agent kiểm lại và thấy nhánh ghi repository vẫn còn, cùng một hàm provDoc không dùng. Sửa để ghi repo, xoá code chết và thêm test kiểm tra có repo, không có repository và content_digest. Test trust verdict vẫn giữ nguyên sau sửa.
**Bài học:** Khi báo cáo rằng đã sạch, hãy grep khoá cần loại bỏ trên mọi đường ghi trước khi viết, đừng chỉ tin vào test sẵn có.
**Artefact:** Kết quả grep repository trước và sau khi sửa.
**Góc người ngoài:** cách làm phổ biến là Hầu hết người dùng AI chỉ yêu cầu 'làm tiếp' và chấp nhận kết quả, ít khi yêu cầu bằng chứng từng bước; ở đây khác ở Agent biến mỗi ràng buộc (kiểm tra main, không đụng checkout khác) thành một bước kiểm tra lặp lại được và ghi kết quả vào báo cáo, nên người đọc có thể tự kiểm lại mà không cần tin lời agent.
