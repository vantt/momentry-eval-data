---
id: 2026-10-09-commit-bi-chan-vi-checkout-chinh-4257
code: M-EPYG
aliases: [M-EPYG]
date: 2026-10-09
repo: repo
status: raw
signals: [khac, nguoi_duyet_may_soan]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [harvest]
lines: ["omp:cd4449ab#L1342", "omp:cd4449ab#L1344", "omp:cd4449ab#L1347", "omp:cd4449ab#L1348", "omp:cd4449ab#L1364", "omp:cd4449ab#L1365", "omp:cd4449ab#L1374", "omp:cd4449ab#L2344", "omp:cd4449ab#L2345", "omp:cd4449ab#L2370", "omp:cd4449ab#L2372"]
hook: "Agent dừng vì file của người khác, lead nói đó không phải blocker"
tension: khac
sides: ["agent thận trọng dừng commit", "lead đổi luật: chỉ dừng nếu file của mình"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Commit bị chặn vì checkout chính có file worktree khác

**Bối cảnh:** Hai worktree cùng làm việc quanh một checkout chính. Luật ban đầu: trước mỗi commit, git status của checkout chính phải sạch ngoài một file kế hoạch.
**Chuyện gì xảy ra:** Lần kiểm tra đầu thấy một file đã sửa thuộc worktree khác; agent dừng và báo cáo, không commit. Lead trả lời các file đó không phải blocker và đổi luật: chỉ dừng nếu có file mình sở hữu. Từ đó agent tiếp tục commit, status chỉ còn file untracked của lead.
**Bài học:** Luật an toàn cho nhiều agent nên ghi 'file nào là của mình' thay vì 'status phải sạch', nếu không sẽ dừng oan.
**Artefact:** Mẫu luật pre-commit đã sửa, không cần ảnh.
