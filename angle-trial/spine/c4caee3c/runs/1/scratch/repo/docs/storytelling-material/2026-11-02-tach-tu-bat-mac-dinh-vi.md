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
angle: none
spine_context: "Obsidian Hybrid Search là gói npm tìm ghi chú Obsidian theo nghĩa, từ khoá, tiêu đề, thẻ và liên kết; đang làm gói tiếng Việt cho bản phát hành theo plan."
spine_context_lines: [profile]
spine_want: "Hoàn tất các mục trong plan lộ trình, trong đó có gói tiếng Việt."
spine_want_lines: ["claude:c4caee3c#L11"]
spine_obstacle: "Một test fast-check thỉnh thoảng hỏng, có từ thời V13 và hỏng cả trên master."
spine_obstacle_lines: ["claude:c4caee3c#L1672"]
spine_action: "Thêm tách từ tiếng Việt với view seg, bật mặc định, rồi merge vào master."
spine_action_lines: ["claude:c4caee3c#L1640"]
spine_outcome: "nDCG@5 tổng từ 0,909 lên 0,932, không hạng mục nào tụt; vi-compound hơn baseline upstream 0,156."
spine_outcome_lines: ["claude:c4caee3c#L1640"]
completeness: 5
---

# Tách từ bật mặc định: vi-compound đã đạt trước nhưng bộ khó cho thấy tác dụng

**Bối cảnh:** vi-compound đã đạt 1,00 trước khi tách từ nên không tăng thêm trên bộ hiện có.
**Chuyện gì xảy ra:** Quyết định bật dựa vào nDCG@5 tổng tăng từ 0,909 lên 0,932 và một bộ câu từ ghép khó do agent tự dựng; trên bộ đó nDCG tăng từ 0,52 đến 0,79 lên 0,86 đến 1,00. Không hạng mục nào tụt. Người dùng đồng ý cách đọc quy tắc eval này.
**Bài học:** Khi một hạng mục đã bão hoà, bộ khó riêng mới cho thấy tác dụng; ghi rõ đó là bộ tự dựng.
