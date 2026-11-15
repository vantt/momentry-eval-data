---
id: 2026-11-02-tu-dien-tu-ghep-bo-pyvi-40f9
code: M-36XW
aliases: [M-36XW]
date: 2026-11-02
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L1640", "claude:c4caee3c#L1672", "claude:c4caee3c#L2155", "claude:c4caee3c#L2160", "claude:c4caee3c#L2862", "claude:c4caee3c#L2875"]
hook: "Bỏ từ điển không rõ nguồn, tự học 20.523 từ, điểm 0,63 lên 0,98"
tension: it_ma_nhieu
sides: ["Bỏ công cụ có sẵn vì nguồn mập mờ", "Bản tự học còn tốt hơn bản cũ"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Obsidian Hybrid Search là gói npm tìm ghi chú Obsidian cục bộ theo nghĩa và từ khóa, và người làm đang hoàn tất phần tiếng Việt. Danh sách từ ghép lấy từ pyvi có giấy phép MIT nên ban đầu tưởng vậy là đủ, nhưng nguồn gốc danh sách không rõ và 95% trùng một bộ từ điển GPL. Người làm học lại 20.523 từ từ dữ liệu CC BY 4.0, dựng lại được đúng từng byte, và độ chính xác từ ghép tăng từ 0,632 lên 0,983. Ai đóng gói dữ liệu bên thứ ba vào sản phẩm nên kiểm tra nguồn gốc chứ không chỉ giấy phép."
audience: dev đóng gói từ điển hoặc dữ liệu bên thứ ba vào sản phẩm
spine_context: Obsidian Hybrid Search là gói npm tìm ghi chú Obsidian cục bộ theo nghĩa và từ khóa; người làm đang hoàn tất gói tiếng Việt theo plan.
spine_context_lines: [profile, "claude:c4caee3c#L11"]
spine_want: "Muốn gói tiếng Việt tách đúng từ ghép, với dữ liệu có giấy phép rõ ràng."
spine_want_lines: ["claude:c4caee3c#L1640"]
spine_obstacle: "Danh sách từ ghép lấy từ pyvi không ghi nguồn gốc, và 95% trùng với một bộ từ điển GPL."
spine_obstacle_lines: ["claude:c4caee3c#L1672"]
spine_turn: Tưởng giấy phép MIT của danh sách pyvi là đủ để dùng; hoá ra nguồn gốc danh sách không rõ và gần như trùng bộ GPL.
spine_turn_lines: ["claude:c4caee3c#L1637", "claude:c4caee3c#L1672"]
spine_action: Học lại 20.523 từ từ thống kê cặp âm tiết trên ba bộ CC BY 4.0; pyvi chỉ còn dùng để chọn ngưỡng khi phát triển.
spine_action_lines: ["claude:c4caee3c#L2155", "claude:c4caee3c#L2862"]
spine_outcome: "Script dựng lại ra file giống hệt từng byte; vi-compound trên fixture khó tăng từ 0,632 lên 0,983, và không hạng mục nào kém danh sách pyvi."
spine_outcome_lines: ["claude:c4caee3c#L2851", "claude:c4caee3c#L2862"]
spine_takeaway: "Giấy phép MIT của một danh sách không chứng minh nguồn gốc; nếu nguồn không rõ, hãy học lại từ dữ liệu có giấy phép rõ và ghi cách dựng để tái tạo."
spine_takeaway_lines: ["claude:c4caee3c#L1672", "claude:c4caee3c#L2851"]
completeness: 7
---

# Từ điển từ ghép: bỏ pyvi vì không rõ nguồn, học lại từ dữ liệu CC BY 4.0

**Góc kể:** Obsidian Hybrid Search là gói npm tìm ghi chú Obsidian cục bộ theo nghĩa và từ khóa, và người làm đang hoàn tất phần tiếng Việt. Danh sách từ ghép lấy từ pyvi có giấy phép MIT nên ban đầu tưởng vậy là đủ, nhưng nguồn gốc danh sách không rõ và 95% trùng một bộ từ điển GPL. Người làm học lại 20.523 từ từ dữ liệu CC BY 4.0, dựng lại được đúng từng byte, và độ chính xác từ ghép tăng từ 0,632 lên 0,983. Ai đóng gói dữ liệu bên thứ ba vào sản phẩm nên kiểm tra nguồn gốc chứ không chỉ giấy phép.
**Bối cảnh:** Từ điển từ ghép của gói tiếng Việt lấy từ một danh sách trên GitHub có giấy phép MIT nhưng không ghi nguồn gốc, và 95% trùng với một bộ từ điển GPL.
**Chuyện gì xảy ra:** Người dùng yêu cầu thay bằng thống kê cặp âm tiết trên dữ liệu có giấy phép rõ. Agent học được 20.523 từ từ ba bộ CC BY 4.0, script dựng lại cho ra file giống hệt từng byte, và vi-compound trên corpus khó tăng từ 0,632 lên 0,983. Từ điển mới tốt hơn hoặc bằng danh sách cũ ở mọi hạng mục.
**Bài học:** Đừng coi giấy phép MIT của một danh sách là đủ; nếu nguồn gốc không rõ, học lại từ dữ liệu có giấy phép rõ và ghi lại cách dựng để tái tạo.
**Artefact:** Bảng nDCG@5 của hạng mục compound qua các phiên bản từ điển.
