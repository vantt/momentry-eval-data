---
id: 2026-11-02-goi-tieng-duc-chay-qua-diem-40f9
code: M-MYST
aliases: [M-MYST]
date: 2026-11-02
repo: repo
status: raw
signals: [khac, rang_buoc_thiet_ke]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L816", "claude:c4caee3c#L1114"]
hook: "Thêm tiếng Đức không sửa lõi, điểm từ 0,57 lên 0,97"
tension: it_ma_nhieu
sides: ["Không đổi dòng nào trong lõi", "nDCG@5 nhảy từ 0,57 lên 0,97"]
strength: 3
stakes: 3
hits: 1
runs: 1
unverified: [agent_only]
privacy: unchecked
links: []
threads: []
angle: none
spine_context: "Dự án tìm kiếm cho vault Obsidian chạy cục bộ, đang thực hiện lộ trình fork có điểm cắm cho gói ngôn ngữ."
spine_context_lines: [profile, "claude:c4caee3c#L11"]
spine_want: "Chứng minh điểm cắm đủ tổng quát, lấy gói tiếng Đức làm bài kiểm."
spine_want_lines: ["claude:c4caee3c#L810"]
spine_action: Viết gói tiếng Đức chạy qua P01 mà không sửa lõi.
spine_action_lines: ["claude:c4caee3c#L810", "claude:c4caee3c#L816"]
spine_outcome: "nDCG@5 tăng từ 0,57 lên 0,97, không hạng mục nào tụt."
spine_outcome_lines: ["claude:c4caee3c#L816", "claude:c4caee3c#L1114"]
completeness: 4
---

# Gói tiếng Đức chạy qua điểm cắm mà không sửa lõi, nDCG@5 từ 0,57 lên 0,97

**Bối cảnh:** Mục tiêu của P01 là điểm cắm đủ tổng quát cho mọi ngôn ngữ. Gói tiếng Đức là bài kiểm chứng đầu tiên.
**Chuyện gì xảy ra:** Gói ohs-lang-de có tách từ ghép bằng quy hoạch động, bỏ dấu và danh sách từ dừng, và chạy qua P01 không cần đổi lõi. nDCG@5 tăng từ 0,57 lên 0,97, không hạng mục nào tụt. Lead dùng kết quả này làm bằng chứng điểm cắm đã tổng quát.
**Bài học:** Thử một ngôn ngữ thứ hai sớm là cách kiểm điểm cắm có thật sự tổng quát hay không.
**Artefact:** Bảng nDCG@5 trước và sau, không kèm dữ liệu.
