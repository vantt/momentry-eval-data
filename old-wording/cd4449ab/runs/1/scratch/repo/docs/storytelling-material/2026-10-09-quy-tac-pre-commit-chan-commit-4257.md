---
id: 2026-10-09-quy-tac-pre-commit-chan-commit-4257
code: M-V9XT
aliases: [M-V9XT]
date: 2026-10-09
repo: repo
status: raw
signals: [rang_buoc_thiet_ke, dao_quyet_dinh]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["omp:cd4449ab#L1342", "omp:cd4449ab#L1344", "omp:cd4449ab#L1356", "omp:cd4449ab#L1364", "omp:cd4449ab#L1365"]
hook: "Quy tắc an toàn chặn commit vì file của người khác"
tension: cam_ma_van_lot
sides: ["Quy tắc dừng commit khi main có file dở", "File dở là của worktree khác, lead phải nới quy tắc"]
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Quy tắc pre-commit chặn commit khi worktree khác để file dở trên main

**Bối cảnh:** Hai agent làm song song: worktree C làm Phase 4, worktree D sửa thẳng trên main checkout. Quy tắc ban đầu cấm commit nếu main checkout có bất kỳ file lạ nào.
**Chuyện gì xảy ra:** Lần kiểm tra đầu, git status trên main hiện file telemetry đã sửa, nên agent dừng và chưa commit. Lead nới quy tắc: chỉ dừng khi file mình sở hữu xuất hiện trong danh sách, còn file của D thì bỏ qua. Sau đó main còn hai file của D, nhưng commit vẫn tiếp tục được.
**Bài học:** Quy tắc kiểm tra sạch cho worktree song song phải định nghĩa theo file mình sở hữu, không theo cả thư mục.
**Artefact:** Đầu ra git status -s trên main, che tên file nếu cần.
**Góc người ngoài:** cách làm phổ biến là Nhiều agent sẽ bỏ qua bước kiểm tra hoặc tự sửa điều kiện để chạy tiếp; ở đây khác ở Agent giữ đúng ranh giới, và khi quy tắc đổi thì nó áp dụng quy tắc mới đúng phạm vi người dùng nêu, không mở rộng thêm.
