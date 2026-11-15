---
id: 2026-10-09-lead-vong-3-skill-add-van-4257
code: M-3KMS
aliases: [M-3KMS]
date: 2026-10-09
repo: repo
status: raw
signals: [nguoi_duyet_may_soan, dao_quyet_dinh]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L2025", "omp:cd4449ab#L2026", "omp:cd4449ab#L2053", "omp:cd4449ab#L2079", "omp:cd4449ab#L2086", "omp:cd4449ab#L2088", "omp:cd4449ab#L2110", "omp:cd4449ab#L2112", "omp:cd4449ab#L2122"]
hook: "Báo cáo ghi sạch, nhưng skill_add vẫn ghi repository"
tension: tuong_ma_hoa_ra
sides: ["báo cáo khẳng định đã chuyển sang repo", "code vẫn ghi trường repository cũ"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một dự án công cụ quản lý skill cho agent AI đang đơn giản hoá cách lưu metadata. Người làm báo cáo đã đổi trường nguồn từ repository sang repo, nhưng người duyệt đọc lại code thì thấy skill_add vẫn ghi key cũ. Ai viết báo cáo 'đã sửa' mà không kèm bằng chứng kiểm tra sẽ dễ có một câu sai lọt qua như vậy."
audience: dev làm công cụ cho AI agent và người review code
spine_context: "Một dự án công cụ quản lý skill cho agent AI (mcp-skill-hub), đang đơn giản hoá cách lưu metadata của skill theo từng phase."
spine_context_lines: ["omp:cd4449ab#L6"]
spine_want: "Muốn skill_add ghi .meta/skill.yaml với key repo, không còn repository hay content_digest."
spine_want_lines: ["omp:cd4449ab#L2025"]
spine_obstacle: "Người duyệt phát hiện skill_add vẫn ghi key repository vào sources[] dù báo cáo nói đã chuyển."
spine_obstacle_lines: ["omp:cd4449ab#L2025"]
spine_turn: "Tưởng báo cáo đã đúng: đã chuyển sang repo. Hoá ra code vẫn ghi key cũ, và báo cáo có một mệnh đề sai."
spine_turn_lines: ["omp:cd4449ab#L2024", "omp:cd4449ab#L2025"]
spine_action: "Đổi key sang repo, xoá provDoc không dùng, thêm test đọc .meta/skill.yaml sau confirm, rồi commit d646117."
spine_action_lines: ["omp:cd4449ab#L2110", "omp:cd4449ab#L2112"]
spine_outcome: "Người duyệt xác nhận d646117 đúng; make check xanh, 24 package đều ok."
spine_outcome_lines: ["omp:cd4449ab#L2122", "omp:cd4449ab#L2123"]
spine_takeaway: "Báo cáo 'đã sửa' nên kèm lệnh kiểm tra và kết quả, để người duyệt đối chiếu được ngay."
spine_takeaway_lines: ["omp:cd4449ab#L2025"]
completeness: 7
---

# Lead vòng 3: skill_add vẫn ghi repository

**Góc kể:** Một dự án công cụ quản lý skill cho agent AI đang đơn giản hoá cách lưu metadata. Người làm báo cáo đã đổi trường nguồn từ repository sang repo, nhưng người duyệt đọc lại code thì thấy skill_add vẫn ghi key cũ. Ai viết báo cáo 'đã sửa' mà không kèm bằng chứng kiểm tra sẽ dễ có một câu sai lọt qua như vậy.
**Bối cảnh:** Agent đã báo cáo xong việc sửa, nhưng code vẫn còn ghi key cũ.
**Chuyện gì xảy ra:** Lead kiểm tra và chỉ ra một mệnh đề trong báo cáo sai: skill_add vẫn ghi repository vào sources[]. Agent xoá provDoc không dùng, chuyển sang repo, rồi thêm test đọc .meta/skill.yaml sau confirm: có repo, không có repository, không có content_digest, trust verdict giữ nguyên. Test đầu tiên đỏ vì loader vẫn chỉ đọc repository.
**Bài học:** Báo cáo 'đã sửa' nên kèm lệnh grep đã chạy và kết quả; người duyệt bắt lỗi chính từ chỗ đó.
**Artefact:** Kết quả grep 'repository:' trước và sau, che nếu cần.
