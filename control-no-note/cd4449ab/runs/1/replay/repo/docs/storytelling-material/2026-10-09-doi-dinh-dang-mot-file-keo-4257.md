---
id: 2026-10-09-doi-dinh-dang-mot-file-keo-4257
code: M-FZ8D
aliases: [M-FZ8D]
date: 2026-10-09
repo: repo
status: raw
signals: [khac, rang_buoc_thiet_ke]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [harvest]
lines: ["omp:cd4449ab#L1087", "omp:cd4449ab#L1218", "omp:cd4449ab#L1287", "omp:cd4449ab#L1303", "omp:cd4449ab#L1305", "omp:cd4449ab#L1311", "omp:cd4449ab#L1342", "omp:cd4449ab#L1356", "omp:cd4449ab#L2888", "omp:cd4449ab#L2890"]
hook: "Đổi định dạng một file, bảy package test đỏ cùng lúc"
tension: nho_ma_to
sides: ["Chỉ đổi định dạng của một file", "Bảy package test đỏ và golden phải tạo lại"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: none
spine_context: "Dự án mcp-skill-hub, một agent làm việc trong worktree riêng để tách schema v1 sang v3 ở Phase 4."
spine_context_lines: ["omp:cd4449ab#L6"]
spine_obstacle: "Test đỏ ở package mcpserver và web, và make check lỗi fmt-check."
spine_obstacle_lines: ["omp:cd4449ab#L1221", "omp:cd4449ab#L1290"]
spine_action: Sửa fixture manifest CLI (experiment_id) và chạy cờ -update để tạo lại golden của web.
spine_action_lines: ["omp:cd4449ab#L1087", "omp:cd4449ab#L1303"]
spine_outcome: "go test ./... xanh ở 24 package, 2 package không có test."
spine_outcome_lines: ["omp:cd4449ab#L1311"]
completeness: 4
---

# Đổi định dạng một file kéo theo test đỏ ở 7 package và cờ -update golden

**Bối cảnh:** Đổi schema từ v1 sang v3 làm nhiều test ở app, skill, cli, mcpserver, web và các golden manifest đỏ. Giữa Phase 4 có 49 file đã sửa nhưng chưa commit.
**Chuyện gì xảy ra:** Agent sửa fixture từng package. Kết quả cuối go test ./... xanh ở 24 package. Ở web, golden được tạo lại bằng cờ -update. Manifest CLI đổi experiment_id để khớp replay. Lead nhắc giữ fixture ở mức tối thiểu vì worktree D cũng có thể sửa cùng file.
**Bài học:** Cờ -update tạo golden từ đầu ra hiện tại, nên chỉ dùng sau khi đã kiểm đầu ra là đúng, không dùng để làm test xanh.
**Artefact:** Diff của một file golden, che nội dung.
