---
id: 2026-11-02-tu-dien-tu-ghep-danh-sach
date: 2026-11-02
repo: repo
status: raw
signals: [đảo quyết định có lý do, số trước sau, ràng buộc định hình thiết kế]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L1685", "claude:c4caee3c#L2155", "claude:c4caee3c#L2862", "claude:c4caee3c#L2875"]
hook: "Danh sách từ ghép MIT có thể mang nguồn GPL, nên đổi sang dữ liệu CC BY"
tension: tuong_ma_hoa_ra
sides: ["Danh sách giấy phép MIT trông an toàn", "Nguồn gốc có thể là GPL; học lại từ CC BY còn tốt hơn, 0,632 lên 0,983"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Obsidian Hybrid Search là gói npm tìm ghi chú Obsidian theo nghĩa và từ khoá, và người làm đang đưa phần tiếng Việt lên, trong đó có một từ điển từ ghép để tách từ đúng. Từ điển này lấy từ một repo MIT nên trông an toàn để dùng, nhưng khoảng 95% nội dung trùng với một danh sách GPL, nên giấy phép của bản chép không nói được nguồn gốc. Người làm dựng lại bằng thống kê trên dữ liệu CC BY 4.0, và chất lượng không giảm: vi-compound tăng từ 0,632 lên 0,983. Ai dùng dữ liệu có sẵn nên kiểm nguồn gốc chứ không chỉ đọc giấy phép."
audience: dev làm công cụ có dùng dữ liệu bên thứ ba và quan tâm đến giấy phép
spine_context: "Obsidian Hybrid Search là gói npm tìm ghi chú Obsidian theo nghĩa và từ khoá. Người làm đang đưa phần tiếng Việt lên, trong đó có một từ điển từ ghép để tách từ đúng."
spine_context_lines: [profile, "claude:c4caee3c#L11"]
spine_want: Muốn có từ điển từ ghép có giấy phép rõ ràng để đạt yêu cầu Q9.
spine_want_lines: ["claude:c4caee3c#L1672"]
spine_obstacle: "Danh sách lấy từ một repo MIT, nhưng khoảng 95% trùng với một danh sách GPL, nên giấy phép của bản chép không nói được nguồn gốc."
spine_obstacle_lines: ["claude:c4caee3c#L1672"]
spine_turn: Tưởng giấy phép MIT của repo là đủ để dùng; hoá ra nguồn gốc dữ liệu có thể là GPL.
spine_turn_lines: ["claude:c4caee3c#L1672"]
spine_action: "Dựng lại từ điển bằng thống kê cặp âm tiết trên ba bộ dữ liệu CC BY 4.0. Chỉ dùng danh sách cũ để chọn ngưỡng, không chép mục nào."
spine_action_lines: ["claude:c4caee3c#L2155", "claude:c4caee3c#L2862"]
spine_outcome: "Từ điển mới có 20.523 từ. vi-compound tăng từ 0,632 lên 0,983, tốt hơn hoặc bằng danh sách cũ ở mọi hạng mục."
spine_outcome_lines: ["claude:c4caee3c#L2862"]
spine_takeaway: "Kiểm nguồn gốc dữ liệu, không chỉ giấy phép của bản chép: một danh sách MIT có thể mang nguồn GPL."
spine_takeaway_lines: ["claude:c4caee3c#L1672"]
completeness: 7
---

# Từ điển từ ghép: danh sách MIT có thể mang nguồn GPL, đổi sang thống kê dữ liệu CC BY

**Góc kể:** Obsidian Hybrid Search là gói npm tìm ghi chú Obsidian theo nghĩa và từ khoá, và người làm đang đưa phần tiếng Việt lên, trong đó có một từ điển từ ghép để tách từ đúng. Từ điển này lấy từ một repo MIT nên trông an toàn để dùng, nhưng khoảng 95% nội dung trùng với một danh sách GPL, nên giấy phép của bản chép không nói được nguồn gốc. Người làm dựng lại bằng thống kê trên dữ liệu CC BY 4.0, và chất lượng không giảm: vi-compound tăng từ 0,632 lên 0,983. Ai dùng dữ liệu có sẵn nên kiểm nguồn gốc chứ không chỉ đọc giấy phép.
**Bối cảnh:** Danh sách 22.574 từ ghép lấy từ một repo MIT, nhưng agent ước lượng phần lớn trùng với một danh sách GPL. Giấy phép của bản chép không phản ánh nguồn gốc.
**Chuyện gì xảy ra:** Agent đọc giấy phép từng nguồn, chọn ba bộ dữ liệu CC BY 4.0 và học bằng thống kê cặp âm tiết, ra 20.523 từ. Không chép mục nào từ danh sách cũ, chỉ dùng nó để chọn ngưỡng. vi-compound trên fixture khó tăng từ 0,632 lên 0,983, tốt hơn hoặc bằng danh sách cũ ở mọi hạng mục. Nguồn được ghi trong file ATTRIBUTION.
**Bài học:** Kiểm nguồn gốc dữ liệu chứ không chỉ giấy phép của bản chép; một danh sách MIT có thể mang nguồn GPL.
**Artefact:** Bảng so vi-compound giữa các phiên bản từ điển.
