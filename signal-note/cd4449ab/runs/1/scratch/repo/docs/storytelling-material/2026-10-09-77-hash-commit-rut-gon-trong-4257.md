---
id: 2026-10-09-77-hash-commit-rut-gon-trong-4257
code: M-M0B1
aliases: [M-M0B1]
date: 2026-10-09
repo: repo
status: raw
signals: [khac, artefact_nhin_duoc]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [harvest]
lines: ["omp:cd4449ab#L2414", "omp:cd4449ab#L2416", "omp:cd4449ab#L2438", "omp:cd4449ab#L2440", "omp:cd4449ab#L2456", "omp:cd4449ab#L2458", "omp:cd4449ab#L2459", "omp:cd4449ab#L2461", "omp:cd4449ab#L2489", "omp:cd4449ab#L2491", "omp:cd4449ab#L2492", "omp:cd4449ab#L2513", "omp:cd4449ab#L2515", "omp:cd4449ab#L2516", "omp:cd4449ab#L2518", "omp:cd4449ab#L2519", "omp:cd4449ab#L2521", "omp:cd4449ab#L2522", "omp:cd4449ab#L2524", "omp:cd4449ab#L2525", "omp:cd4449ab#L2527"]
hook: "77 hash rút gọn, một lệnh git đổi hết thành 40 ký tự"
tension: it_ma_nhieu
sides: ["77 hash viết tắt dễ trỏ sai", "một lệnh git rev-parse phân giải đủ"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: none
spine_context: "Một nhóm đang tách lại hub công cụ MCP theo từng pha, và người làm đang chuyển dữ liệu bài học distill của hub thật sang format mới."
spine_context_lines: ["omp:cd4449ab#L6", "omp:cd4449ab#L2374"]
spine_want: Chứng minh file distill.yaml của hub thật chuyển được sang format mới.
spine_want_lines: ["omp:cd4449ab#L2374"]
spine_obstacle: File có 77 mục commit viết tắt cần phân giải.
spine_obstacle_lines: ["omp:cd4449ab#L2416"]
spine_action: "Phân giải hash viết tắt bằng git rev-parse trên mirror, copy file vào testdata, rồi chạy test và kiểm tra key, what và trạng thái."
spine_action_lines: ["omp:cd4449ab#L2438", "omp:cd4449ab#L2440", "omp:cd4449ab#L2492", "omp:cd4449ab#L2512", "omp:cd4449ab#L2515", "omp:cd4449ab#L2518", "omp:cd4449ab#L2521"]
spine_outcome: "39 bài candidate, 3 bài planned; không key sai định dạng, không trùng key, không thiếu what."
spine_outcome_lines: ["omp:cd4449ab#L2515", "omp:cd4449ab#L2518", "omp:cd4449ab#L2521", "omp:cd4449ab#L2524"]
spine_takeaway: "Phân giải hash viết tắt bằng git trước khi siết schema, thay vì đoán."
spine_takeaway_lines: ["omp:cd4449ab#L2438", "omp:cd4449ab#L2440"]
completeness: 6
---

# 77 hash commit rút gọn trong distill.yaml được phân giải

**Bối cảnh:** File distill.yaml của hub thật có khoảng 1184 dòng, 46161 byte, 42 bài học, mỗi bài học trỏ tới commit của một nguồn upstream.
**Chuyện gì xảy ra:** Đếm được 77 mục tham chiếu commit viết tắt. Dùng git rev-parse trên mirror của hai nguồn để phân giải về đủ 40 ký tự, ví dụ một hash 11 ký tự thành hash đầy đủ. Sau đó kiểm tra: không có key sai định dạng, không trùng key, không bài học thiếu what. Kết quả: 39 bài candidate, 3 bài planned.
**Bài học:** Dữ liệu viết tay luôn có hash rút gọn; phân giải bằng git trước khi siết schema, đừng đoán.
**Artefact:** Bảng rút gọn sang đầy đủ cho năm mẫu, không kèm tên repo.
