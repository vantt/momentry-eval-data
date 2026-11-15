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
hook: "Dựng lại từ điển từ dữ liệu CC BY, điểm từ 0,632 lên 0,983"
tension: it_ma_nhieu
sides: ["Không chép một mục nào từ danh sách không rõ nguồn", "Từ điển tự học vẫn kéo điểm từ 0,632 lên 0,983"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Obsidian Hybrid Search là công cụ tìm kiếm cho ghi chú Obsidian trên máy, và người làm đang hoàn thiện gói tiếng Việt của nó. Gói cần danh sách từ ghép; danh sách lấy từ pyvi có giấy phép MIT nên tưởng là dùng được, nhưng nguồn của nó không ghi rõ và phần lớn trùng với một bộ từ điển GPL. Người làm dựng lại danh sách từ thống kê cặp âm tiết trên dữ liệu CC BY 4.0, và điểm vi-compound trên bộ thử khó tăng từ 0,632 lên 0,983. Ai đưa dữ liệu bên thứ ba vào sản phẩm nên kiểm nguồn gốc của nó, không chỉ đọc dòng giấy phép."
audience: dev đưa dữ liệu bên thứ ba vào sản phẩm
spine_context: "Obsidian Hybrid Search là công cụ tìm kiếm cho ghi chú Obsidian trên máy, đang hoàn thiện gói tiếng Việt."
spine_context_lines: [profile]
spine_want: Gói cần danh sách từ ghép với giấy phép và nguồn rõ ràng.
spine_want_lines: ["claude:c4caee3c#L1672"]
spine_obstacle: "Danh sách từ ghép lấy từ pyvi không ghi nguồn gốc, và 95% trùng với Viet74K (GPL)."
spine_obstacle_lines: ["claude:c4caee3c#L1672"]
spine_turn: Tưởng giấy phép MIT của pyvi là đủ; hoá ra nguồn của danh sách không rõ và phần lớn trùng với nguồn GPL.
spine_turn_lines: ["claude:c4caee3c#L1672"]
spine_action: "Dựng lại danh sách bằng thống kê cặp âm tiết trên ba bộ dữ liệu CC BY 4.0, không chép mục nào từ pyvi."
spine_action_lines: ["claude:c4caee3c#L2155", "claude:c4caee3c#L2875"]
spine_outcome: "Danh sách có 20.523 từ; điểm vi-compound trên bộ thử khó tăng từ 0,632 lên 0,983."
spine_outcome_lines: ["claude:c4caee3c#L2875"]
spine_takeaway: "Kiểm nguồn gốc dữ liệu tải về, kể cả khi giấy phép ghi MIT."
spine_takeaway_lines: ["claude:c4caee3c#L1672"]
completeness: 7
---

# Từ điển từ ghép: danh sách pyvi không rõ nguồn, dựng lại từ dữ liệu CC BY

**Góc kể:** Obsidian Hybrid Search là công cụ tìm kiếm cho ghi chú Obsidian trên máy, và người làm đang hoàn thiện gói tiếng Việt của nó. Gói cần danh sách từ ghép; danh sách lấy từ pyvi có giấy phép MIT nên tưởng là dùng được, nhưng nguồn của nó không ghi rõ và phần lớn trùng với một bộ từ điển GPL. Người làm dựng lại danh sách từ thống kê cặp âm tiết trên dữ liệu CC BY 4.0, và điểm vi-compound trên bộ thử khó tăng từ 0,632 lên 0,983. Ai đưa dữ liệu bên thứ ba vào sản phẩm nên kiểm nguồn gốc của nó, không chỉ đọc dòng giấy phép.
**Bối cảnh:** Gói tiếng Việt cần danh sách từ ghép. Danh sách lấy từ pyvi có giấy phép MIT nhưng không rõ nguồn, và 95% trùng với nguồn GPL.
**Chuyện gì xảy ra:** Người dùng chọn học thống kê cặp âm tiết từ ba bộ dữ liệu CC BY 4.0 (câu dịch Wikinews, văn bản pháp luật và một bộ sinh bằng model), không chép mục nào từ pyvi. Kết quả là 20.523 từ, và vi-compound trên fixture khó tăng từ 0,632 lên 0,983. Tách từ được bật mặc định dựa trên bộ câu do agent tự dựng, nên người duyệt phải đồng ý với cách đọc quy tắc eval.
**Bài học:** Kiểm nguồn gốc dữ liệu tải về, kể cả khi giấy phép ghi MIT. Ưu tiên dữ liệu có giấy phép và nguồn rõ ràng.
**Artefact:** Bảng vi-compound trước và sau, không kèm dữ liệu.
