---
id: 2026-11-02-tach-tu-bat-mac-dinh-vi
date: 2026-11-02
repo: repo
status: raw
signals: [số trước sau, đảo quyết định có lý do]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L1637", "claude:c4caee3c#L1672", "claude:c4caee3c#L1685"]
hook: "Bộ test chung đã đạt, nhưng bộ khó mới cho thấy tác dụng: 0,52 lên 0,86"
tension: tuong_ma_hoa_ra
sides: ["Tổng điểm đã đạt, tưởng đủ bằng chứng", "Bộ câu từ ghép khó mới lộ mức tăng, từ 0,52 lên 0,86 đến 1,00"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Obsidian Hybrid Search là công cụ tìm kiếm ghi chú Obsidian chạy cục bộ, và nhóm đang hoàn tất roadmap có gói tiếng Việt. Để tách từ ghép, agent chọn một danh sách từ lấy từ pyvi vì giấy phép MIT có vẻ đủ sạch. Khi truy nguồn gốc, danh sách này trùng khoảng 95% với Viet74K, một nguồn GPL, nên giấy phép MIT chưa nói hết câu chuyện. Ai làm công cụ có dữ liệu từ bên thứ ba nên kiểm tra nguồn gốc trước khi dùng."
audience: dev làm công cụ có dữ liệu từ bên thứ ba và quan tâm đến giấy phép
spine_context: "Nhóm làm Obsidian Hybrid Search, công cụ tìm kiếm ghi chú Obsidian chạy cục bộ, đang hoàn tất roadmap, trong đó có gói xử lý tiếng Việt."
spine_context_lines: [profile, "claude:c4caee3c#L11"]
spine_want: "Hoàn tất các mục trong roadmap; gói tiếng Việt phải hơn baseline tối thiểu 0,1."
spine_want_lines: ["claude:c4caee3c#L11", "claude:c4caee3c#L1640"]
spine_obstacle: "Bộ đo chung đã bão hoà: vi-compound đạt 1,00 trước khi tách từ nên không thấy tăng."
spine_obstacle_lines: ["claude:c4caee3c#L1672"]
spine_turn: "Tưởng giấy phép MIT của danh sách từ là đủ; hoá ra danh sách đó trùng khoảng 95% với Viet74K, một nguồn GPL."
spine_turn_lines: ["claude:c4caee3c#L1637", "claude:c4caee3c#L1672"]
spine_action: "Giữ pyvi, lọc còn 22.574 từ hai âm tiết, chép giấy phép và ghi nguồn vào README."
spine_action_lines: ["claude:c4caee3c#L1637"]
spine_outcome: "nDCG@5 tổng tăng từ 0,909 lên 0,932, không hạng mục nào tụt; phần nguồn từ điển còn chờ bạn chốt."
spine_outcome_lines: ["claude:c4caee3c#L1637", "claude:c4caee3c#L1672"]
spine_takeaway: Giấy phép MIT của một danh sách từ không chứng minh được nguồn gốc dữ liệu; cần truy nguồn trước khi dùng.
spine_takeaway_lines: ["claude:c4caee3c#L1672"]
completeness: 7
---

# Tách từ bật mặc định: vi-compound đã đạt trước nhưng bộ khó cho thấy tác dụng

**Góc kể:** Obsidian Hybrid Search là công cụ tìm kiếm ghi chú Obsidian chạy cục bộ, và nhóm đang hoàn tất roadmap có gói tiếng Việt. Để tách từ ghép, agent chọn một danh sách từ lấy từ pyvi vì giấy phép MIT có vẻ đủ sạch. Khi truy nguồn gốc, danh sách này trùng khoảng 95% với Viet74K, một nguồn GPL, nên giấy phép MIT chưa nói hết câu chuyện. Ai làm công cụ có dữ liệu từ bên thứ ba nên kiểm tra nguồn gốc trước khi dùng.
**Bối cảnh:** vi-compound đã đạt 1,00 trước khi tách từ nên không tăng thêm trên bộ hiện có.
**Chuyện gì xảy ra:** Quyết định bật dựa vào nDCG@5 tổng tăng từ 0,909 lên 0,932 và một bộ câu từ ghép khó do agent tự dựng; trên bộ đó nDCG tăng từ 0,52 đến 0,79 lên 0,86 đến 1,00. Không hạng mục nào tụt. Người dùng đồng ý cách đọc quy tắc eval này.
**Bài học:** Khi một hạng mục đã bão hoà, bộ khó riêng mới cho thấy tác dụng; ghi rõ đó là bộ tự dựng.
