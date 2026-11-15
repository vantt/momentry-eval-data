---
id: 2026-11-02-vault-that-khong-roi-may-eval
date: 2026-11-02
repo: repo
status: raw
signals: []
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L3623", "claude:c4caee3c#L3633", "claude:c4caee3c#L3645", "claude:c4caee3c#L3797", "claude:c4caee3c#L3825"]
hook: "Vault thật không rời máy; script từ chối ghi nếu đường dẫn nằm trong repo"
tension: cam_ma_van_lot
sides: ["Eval chạy trên vault thật chỉ in số tổng hợp", "Chế độ chi tiết ghi từng câu ra file, nhưng bị khoá đường dẫn, quyền 0600"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Vault thật không rời máy: eval chi tiết chỉ ghi ra ngoài repo, có kiểm đường dẫn

**Bối cảnh:** Golden set gán nhãn trên vault thật của người dùng. Nội dung vault không được vào repo, CI hay báo cáo.
**Chuyện gì xảy ra:** Eval trên vault thật chỉ in số tổng hợp. Chế độ chi tiết ghi từng câu ra file ngoài repo với quyền 0600, và script từ chối ghi nếu đường dẫn nằm trong repo, trong worktree khác hoặc qua symlink. Kết quả cho thấy 61 câu, nDCG@5 tổng 0,600 lên 0,698, nhưng vài hạng mục nhỏ tụt vì chỉ có 2 đến 6 câu mỗi hạng mục.
**Bài học:** Ràng buộc riêng tư nên được biến thành kiểm tra trong công cụ, không chỉ là quy tắc trong tài liệu.
**Artefact:** Bảng số tổng hợp theo hạng mục; không chụp câu hỏi hay đường dẫn.
