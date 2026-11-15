---
id: 2026-11-02-tu-dien-tu-ghep-danh-sach-40f9
code: M-MHZ7
aliases: [M-MHZ7]
date: 2026-11-02
repo: repo
status: raw
signals: [rang_buoc_thiet_ke, khac]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L1640", "claude:c4caee3c#L1672", "claude:c4caee3c#L2155", "claude:c4caee3c#L2862", "claude:c4caee3c#L2875"]
hook: "Dựng lại từ điển từ dữ liệu CC BY, vi-compound từ 0,632 lên 0,983"
tension: giup_ma_hai
sides: ["Danh sách không rõ nguồn, phải dựng lại sạch từ dữ liệu CC BY", "Bật mặc định dựa trên bộ câu agent tự dựng"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Từ điển từ ghép: danh sách pyvi không rõ nguồn, dựng lại từ dữ liệu CC BY

**Bối cảnh:** Gói tiếng Việt cần danh sách từ ghép. Danh sách lấy từ pyvi có giấy phép MIT nhưng không rõ nguồn, và 95% trùng với nguồn GPL.
**Chuyện gì xảy ra:** Người dùng chọn học thống kê cặp âm tiết từ ba bộ dữ liệu CC BY 4.0 (câu dịch Wikinews, văn bản pháp luật và một bộ sinh bằng model), không chép mục nào từ pyvi. Kết quả là 20.523 từ, và vi-compound trên fixture khó tăng từ 0,632 lên 0,983. Tách từ được bật mặc định dựa trên bộ câu do agent tự dựng, nên người duyệt phải đồng ý với cách đọc quy tắc eval.
**Bài học:** Kiểm nguồn gốc dữ liệu tải về, kể cả khi giấy phép ghi MIT. Ưu tiên dữ liệu có giấy phép và nguồn rõ ràng.
**Artefact:** Bảng vi-compound trước và sau, không kèm dữ liệu.
