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
hook: "Danh sách từ không rõ nguồn, dựng lại từ dữ liệu CC BY: 0,632 lên 0,983"
tension: it_ma_nhieu
sides: ["Bỏ danh sách pyvi không rõ nguồn gốc, không chép mục nào", "Tự học từ dữ liệu CC BY, được 20.523 từ, điểm lên 0,983"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Obsidian Hybrid Search là công cụ tìm kiếm cho vault Obsidian cục bộ, và gói tiếng Việt của nó cần một danh sách từ ghép để tách từ. Danh sách lấy từ pyvi được coi là ổn vì ghi giấy phép MIT, nhưng nguồn gốc không rõ và gần như trùng nguồn GPL. Người làm bỏ hẳn danh sách đó, tự học thống kê cặp âm tiết từ ba bộ dữ liệu CC BY 4.0, và điểm vi-compound lên 0,983. Ai đóng gói dữ liệu mở nên kiểm nguồn gốc file tải về, kể cả khi nhãn giấy phép ghi MIT."
audience: "dev làm công cụ hoặc gói ngôn ngữ mã mở, quan tâm đến giấy phép dữ liệu"
spine_context: "Obsidian Hybrid Search là công cụ tìm kiếm cho vault Obsidian cục bộ, đang dựng gói tiếng Việt."
spine_context_lines: [profile, "claude:c4caee3c#L1672"]
spine_want: Gói tiếng Việt cần một danh sách từ ghép để tách từ.
spine_want_lines: ["claude:c4caee3c#L1672"]
spine_obstacle: "Danh sách lấy từ pyvi có giấy phép MIT nhưng nguồn gốc không rõ, và 95% trùng với nguồn GPL."
spine_obstacle_lines: ["claude:c4caee3c#L1672"]
spine_turn: Tưởng nhãn MIT là đủ để dùng danh sách pyvi; hoá ra nguồn gốc không rõ và gần như trùng nguồn GPL.
spine_turn_lines: ["claude:c4caee3c#L1672"]
spine_action: "Học thống kê cặp âm tiết từ ba bộ dữ liệu CC BY 4.0, không chép mục nào từ pyvi."
spine_action_lines: ["claude:c4caee3c#L2875"]
spine_outcome: "Có 20.523 từ; vi-compound trên fixture khó tăng từ 0,632 lên 0,983."
spine_outcome_lines: ["claude:c4caee3c#L2875"]
spine_takeaway: "Kiểm nguồn gốc file tải về, kể cả khi nhãn giấy phép ghi MIT; ưu tiên dữ liệu có giấy phép và nguồn rõ ràng."
spine_takeaway_lines: ["claude:c4caee3c#L1672", "claude:c4caee3c#L2875"]
completeness: 7
---

# Từ điển từ ghép: danh sách pyvi không rõ nguồn, dựng lại từ dữ liệu CC BY

**Góc kể:** Obsidian Hybrid Search là công cụ tìm kiếm cho vault Obsidian cục bộ, và gói tiếng Việt của nó cần một danh sách từ ghép để tách từ. Danh sách lấy từ pyvi được coi là ổn vì ghi giấy phép MIT, nhưng nguồn gốc không rõ và gần như trùng nguồn GPL. Người làm bỏ hẳn danh sách đó, tự học thống kê cặp âm tiết từ ba bộ dữ liệu CC BY 4.0, và điểm vi-compound lên 0,983. Ai đóng gói dữ liệu mở nên kiểm nguồn gốc file tải về, kể cả khi nhãn giấy phép ghi MIT.
**Bối cảnh:** Gói tiếng Việt cần danh sách từ ghép. Danh sách lấy từ pyvi có giấy phép MIT nhưng không rõ nguồn, và 95% trùng với nguồn GPL.
**Chuyện gì xảy ra:** Người dùng chọn học thống kê cặp âm tiết từ ba bộ dữ liệu CC BY 4.0 (câu dịch Wikinews, văn bản pháp luật và một bộ sinh bằng model), không chép mục nào từ pyvi. Kết quả là 20.523 từ, và vi-compound trên fixture khó tăng từ 0,632 lên 0,983. Tách từ được bật mặc định dựa trên bộ câu do agent tự dựng, nên người duyệt phải đồng ý với cách đọc quy tắc eval.
**Bài học:** Kiểm nguồn gốc dữ liệu tải về, kể cả khi giấy phép ghi MIT. Ưu tiên dữ liệu có giấy phép và nguồn rõ ràng.
**Artefact:** Bảng vi-compound trước và sau, không kèm dữ liệu.
