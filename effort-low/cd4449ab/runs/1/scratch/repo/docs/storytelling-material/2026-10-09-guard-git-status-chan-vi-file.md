---
id: 2026-10-09-guard-git-status-chan-vi-file
date: 2026-10-09
repo: repo
status: raw
signals: [người duyệt, ràng buộc định hình]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [harvest]
lines: ["omp:cd4449ab#L1342", "omp:cd4449ab#L1363", "omp:cd4449ab#L1364", "omp:cd4449ab#L2331", "omp:cd4449ab#L2344", "omp:cd4449ab#L2345"]
hook: "Agent dừng cả buổi vì một file không phải của nó"
tension: cam_ma_van_lot
sides: ["guard chặn mọi file lạ trong status", "agent tự dừng vì file của worktree khác"]
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Guard git status chặn vì file của worktree khác

**Bối cảnh:** Quy tắc trước commit yêu cầu git status của checkout chính chỉ chứa file của prompt. Một worktree khác làm việc trực tiếp trong checkout chính.
**Chuyện gì xảy ra:** Guard báo file không phải của mình trong checkout chính và agent dừng báo cáo. Lead đổi quy tắc: chỉ dừng khi file của chính mình xuất hiện. Từ đó agent kiểm tra theo danh sách file sở hữu thay vì toàn bộ status.
**Bài học:** Guard kiểm tra trạng thái chung dễ chặn công việc của người khác; hãy giới hạn kiểm tra vào file mình sở hữu.
**Artefact:** Đoạn quy tắc mới (không kèm đường dẫn).
