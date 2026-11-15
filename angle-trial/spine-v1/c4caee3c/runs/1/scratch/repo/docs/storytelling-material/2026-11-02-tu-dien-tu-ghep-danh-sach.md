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
angle: "Obsidian Hybrid Search là công cụ tìm kiếm ghi chú Obsidian, và nhóm đang làm gói tách từ tiếng Việt cho nó. Từ điển từ ghép lấy từ một repo MIT được coi là an toàn, nhưng 95% nội dung trùng với một danh sách GPL, nên giấy phép của bản chép không cho biết nguồn gốc thật. Nhóm học lại từ ba bộ dữ liệu CC BY 4.0, ra 20.523 từ, và điểm vi-compound tăng từ 0,632 lên 0,983. Ai dùng dữ liệu mã nguồn mở nên kiểm nguồn gốc, không chỉ đọc giấy phép."
audience: dev làm tìm kiếm hoặc xử lý tiếng Việt với dữ liệu mã nguồn mở
spine_context: "Obsidian Hybrid Search là công cụ tìm kiếm ghi chú Obsidian (plugin, CLI, MCP), đang làm gói tách từ tiếng Việt cho tìm kiếm."
spine_context_lines: [profile]
spine_want: Đạt yêu cầu giấy phép Q9 cho danh sách từ ghép.
spine_want_lines: ["claude:c4caee3c#L1672"]
spine_obstacle: "pyvi không ghi danh sách lấy từ đâu, và 95% trùng với Viet74K (GPL)."
spine_obstacle_lines: ["claude:c4caee3c#L1672"]
spine_turn: Tưởng giấy phép MIT của bản chép là đủ; hoá ra nguồn gốc là GPL.
spine_turn_lines: ["claude:c4caee3c#L1672"]
spine_action: Học lại từ ba bộ CC BY 4.0 bằng thống kê cặp âm tiết; pyvi chỉ dùng để chọn ngưỡng.
spine_action_lines: ["claude:c4caee3c#L2851"]
spine_outcome: "Ra 20.523 từ; vi-compound tăng từ 0,632 lên 0,983."
spine_outcome_lines: ["claude:c4caee3c#L2862"]
spine_takeaway: "Kiểm nguồn gốc dữ liệu, không chỉ giấy phép của bản chép."
spine_takeaway_lines: ["claude:c4caee3c#L1672"]
completeness: 7
---

# Từ điển từ ghép: danh sách MIT có thể mang nguồn GPL, đổi sang thống kê dữ liệu CC BY

**Góc kể:** Obsidian Hybrid Search là công cụ tìm kiếm ghi chú Obsidian, và nhóm đang làm gói tách từ tiếng Việt cho nó. Từ điển từ ghép lấy từ một repo MIT được coi là an toàn, nhưng 95% nội dung trùng với một danh sách GPL, nên giấy phép của bản chép không cho biết nguồn gốc thật. Nhóm học lại từ ba bộ dữ liệu CC BY 4.0, ra 20.523 từ, và điểm vi-compound tăng từ 0,632 lên 0,983. Ai dùng dữ liệu mã nguồn mở nên kiểm nguồn gốc, không chỉ đọc giấy phép.
**Bối cảnh:** Danh sách 22.574 từ ghép lấy từ một repo MIT, nhưng agent ước lượng phần lớn trùng với một danh sách GPL. Giấy phép của bản chép không phản ánh nguồn gốc.
**Chuyện gì xảy ra:** Agent đọc giấy phép từng nguồn, chọn ba bộ dữ liệu CC BY 4.0 và học bằng thống kê cặp âm tiết, ra 20.523 từ. Không chép mục nào từ danh sách cũ, chỉ dùng nó để chọn ngưỡng. vi-compound trên fixture khó tăng từ 0,632 lên 0,983, tốt hơn hoặc bằng danh sách cũ ở mọi hạng mục. Nguồn được ghi trong file ATTRIBUTION.
**Bài học:** Kiểm nguồn gốc dữ liệu chứ không chỉ giấy phép của bản chép; một danh sách MIT có thể mang nguồn GPL.
**Artefact:** Bảng so vi-compound giữa các phiên bản từ điển.
