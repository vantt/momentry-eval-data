---
id: 2026-10-09-claim-da-ghi-repo-sai-writer
date: 2026-10-09
repo: repo
status: raw
signals: [khác]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [harvest]
lines: ["omp:cd4449ab#L2025", "omp:cd4449ab#L2053", "omp:cd4449ab#L2110", "omp:cd4449ab#L2122"]
hook: "Báo cáo ghi 'đã ghi repo', writer cũ vẫn ghi repository"
tension: tuong_ma_hoa_ra
sides: ["Báo cáo nói đã sửa xong", "Một writer không được liệt kê vẫn ghi khoá cũ"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Claim 'đã ghi repo' sai: writer cũ vẫn ghi repository

**Bối cảnh:** Agent báo cáo rằng mọi writer đã chuyển sang khoá repo.
**Chuyện gì xảy ra:** Lead phát hiện skill_add.go vẫn ghi khoá repository vào sources[] của skill mới. Commit d646117 xoá 48 dòng trong skill_add.go, bỏ provDoc không dùng, và thêm test khẳng định .meta/skill.yaml có repo, không có repository và content_digest. Lỗi nằm ở một writer mà báo cáo không liệt kê.
**Bài học:** Trước khi viết 'đã sửa hết', grep khoá đó trên toàn bộ writer, không chỉ ở chỗ vừa sửa.
**Artefact:** Kết quả grep 'repository' trước và sau commit d646117. Không có dữ liệu nhạy cảm.
