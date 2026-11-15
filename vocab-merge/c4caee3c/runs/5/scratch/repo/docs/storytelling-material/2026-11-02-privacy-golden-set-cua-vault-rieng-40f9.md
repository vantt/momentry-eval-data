---
id: 2026-11-02-privacy-golden-set-cua-vault-rieng-40f9
code: M-FPQ2
aliases: [M-FPQ2]
date: 2026-11-02
repo: repo
status: raw
signals: [ràng buộc định hình thiết kế, artefact nhìn được]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:c4caee3c#L2702", "claude:c4caee3c#L3615", "claude:c4caee3c#L3804", "claude:c4caee3c#L3809"]
hook: "Chỉ số tổng hợp thì commit, chi tiết từng câu của vault riêng ở ngoài repo"
tension: cam_ma_van_lot
sides: ["Guard chặn đường dẫn trong repo, worktree khác và symlink", "Log chỉ in số tổng hợp, nhánh chứa kết quả riêng bị xoá"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Privacy: golden set của vault riêng ngoài repo, guard từ chối đường dẫn trong repo

**Bối cảnh:** Eval chạy trên vault cá nhân, còn repo công khai và CI không được thấy nội dung vault.
**Chuyện gì xảy ra:** Chỉ số tổng hợp được commit. Chi tiết từng câu ghi ra file ngoài repo với quyền 0600. Script từ chối đường dẫn nằm trong repo, trong worktree khác hoặc qua symlink. Log chỉ in số tổng hợp. Nhánh chứa kết quả riêng được xoá sau khi merge.
**Bài học:** Đặt guard trong công cụ thay vì dựa vào ghi nhớ; ghi quy tắc privacy vào plan và viết test 'không in nội dung'.
**Artefact:** Ví dụ log chỉ có số tổng hợp, không có câu hỏi hay tên note.
**Góc người ngoài:** cách làm phổ biến là Thường agent sẽ tự tạo dữ liệu giả hoặc yêu cầu người dùng gửi nguyên văn dữ liệu cá nhân lên chat; ở đây khác ở Người đọc sẽ hỏi làm sao đánh giá được trên dữ liệu thật mà vẫn không đưa dữ liệu riêng ra ngoài máy, và cơ chế từ chối đường dẫn trong repo hoạt động thế nào.
