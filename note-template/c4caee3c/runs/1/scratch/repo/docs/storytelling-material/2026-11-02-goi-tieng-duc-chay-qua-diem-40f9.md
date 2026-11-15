---
id: 2026-11-02-goi-tieng-duc-chay-qua-diem-40f9
code: M-MYST
aliases: [M-MYST]
date: 2026-11-02
repo: repo
status: raw
signals: [so_truoc_so_sau]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L816", "claude:c4caee3c#L1114", "claude:c4caee3c#L3434"]
hook: "Gói tiếng Đức từ 0,57 lên 0,97 mà không sửa lõi"
tension: it_ma_nhieu
sides: ["Không sửa dòng nào ở lõi", "nDCG@5 tăng từ 0,57 lên 0,97"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: none
spine_context: "Một công cụ tìm kiếm cục bộ cho ghi chú Obsidian, đang chạy lộ trình fork với nhiều agent làm song song."
spine_context_lines: [profile, "claude:c4caee3c#L11"]
spine_want: Hoàn tất lộ trình fork bằng cách điều phối các agent theo đợt.
spine_want_lines: ["claude:c4caee3c#L748"]
spine_obstacle: "/tmp đầy hạn mức vì các worktree đặt trong đó, làm mọi agent hỏng lệnh shell."
spine_obstacle_lines: ["claude:c4caee3c#L1114"]
spine_action: Chuyển toàn bộ worktree sang thư mục khác rồi cho các agent chạy lại.
spine_action_lines: ["claude:c4caee3c#L1114"]
spine_outcome: Không mất phần việc nào; các agent chạy lại được.
spine_outcome_lines: ["claude:c4caee3c#L1114"]
spine_takeaway: Đặt worktree của agent ngoài /tmp.
spine_takeaway_lines: ["claude:c4caee3c#L1114"]
completeness: 6
---

# Gói tiếng Đức chạy qua điểm cắm mà không sửa lõi

**Bối cảnh:** Điểm cắm ngôn ngữ được thiết kế cho tiếng Việt. Mục tiêu thử nghiệm là chứng minh nó đủ tổng quát cho ngôn ngữ thứ hai.
**Chuyện gì xảy ra:** Gói tiếng Đức có từ điển ghép, bỏ từ dừng và biến thể viết. Trên bộ eval tiếng Đức, nDCG@5 tăng từ 0,57 lên 0,97, không hạng mục nào tụt, và lõi không bị sửa. Sau đó điểm cắm được bổ sung thêm năm điểm mở rộng để gói tiếng Việt dùng.
**Bài học:** Thử ngôn ngữ thứ hai sớm là cách rẻ nhất để biết điểm cắm có thật sự tổng quát không.
**Artefact:** Bảng nDCG@5 tiếng Đức trước và sau gói.
