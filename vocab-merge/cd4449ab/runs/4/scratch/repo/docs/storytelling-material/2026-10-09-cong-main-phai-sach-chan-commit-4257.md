---
id: 2026-10-09-cong-main-phai-sach-chan-commit-4257
code: M-Q7HT
aliases: [M-Q7HT]
date: 2026-10-09
repo: repo
status: raw
signals: []
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [harvest]
lines: ["omp:cd4449ab#L1342", "omp:cd4449ab#L1344", "omp:cd4449ab#L1364", "omp:cd4449ab#L1365", "omp:cd4449ab#L1374", "omp:cd4449ab#L2331", "omp:cd4449ab#L2344", "omp:cd4449ab#L2345", "omp:cd4449ab#L2372"]
hook: "Cổng 'main phải sạch' chặn commit vì file của agent khác"
tension: giup_ma_hai
sides: ["cổng kiểm tra để giữ main sạch", "chặn nhầm vì file của người khác"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Cổng 'main phải sạch' chặn commit vì file của agent khác

**Bối cảnh:** Worktree C được quy định: trước mỗi commit, git status của main checkout chỉ được có một file prompt. Worktree D được phép sửa trực tiếp main.
**Chuyện gì xảy ra:** Lần đầu main có một file đã sửa (telemetry_funnel.go), agent dừng và báo cáo. Lead trả lời đó là việc của worktree D, không phải lý do chặn. Quy tắc đổi thành: chỉ dừng khi file mình sở hữu xuất hiện. Sau đó agent vẫn dừng một lần vì một file untracked của lead, và được cho đi tiếp.
**Bài học:** Khi nhiều agent cùng làm trên một checkout, guard nên kiểm tra quyền sở hữu file, không kiểm tra thư mục có sạch hay không.
**Artefact:** Sơ đồ hai worktree với danh sách file sở hữu của từng bên.
