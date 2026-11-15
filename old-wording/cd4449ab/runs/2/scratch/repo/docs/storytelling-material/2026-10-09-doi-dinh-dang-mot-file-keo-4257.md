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
hook: "Đổi định dạng một file, test đỏ ở 7 package"
tension: nho_ma_to
sides: ["chỉ đổi định dạng một file", "test đỏ ở 7 package, phải tạo lại golden"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đổi định dạng một file kéo theo test đỏ ở 7 package và cờ -update golden

**Bối cảnh:** Đổi schema từ v1 sang v3 làm nhiều test ở app, skill, cli, mcpserver, web và các golden manifest đỏ. Giữa Phase 4 có 49 file đã sửa nhưng chưa commit.
**Chuyện gì xảy ra:** Agent sửa fixture từng package. Kết quả cuối go test ./... xanh ở 24 package. Ở web, golden được tạo lại bằng cờ -update. Manifest CLI đổi experiment_id để khớp replay. Lead nhắc giữ fixture ở mức tối thiểu vì worktree D cũng có thể sửa cùng file.
**Bài học:** Cờ -update tạo golden từ đầu ra hiện tại, nên chỉ dùng sau khi đã kiểm đầu ra là đúng, không dùng để làm test xanh.
**Artefact:** Diff của một file golden, che nội dung.
