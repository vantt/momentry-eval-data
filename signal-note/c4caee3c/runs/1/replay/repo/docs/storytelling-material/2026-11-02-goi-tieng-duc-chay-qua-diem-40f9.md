---
id: 2026-11-02-goi-tieng-duc-chay-qua-diem-40f9
code: M-MYST
aliases: [M-MYST]
date: 2026-11-02
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L816", "claude:c4caee3c#L1114"]
hook: "Gói tiếng Đức cắm vào không sửa lõi: 0,57 lên 0,97"
tension: it_ma_nhieu
sides: ["Không sửa dòng nào ở lõi", "Điểm tiếng Đức tăng gần gấp đôi"]
strength: 2
stakes: 3
hits: 1
runs: 1
unverified: [agent_only]
privacy: unchecked
links: []
threads: []
angle: none
spine_context: "Dự án Obsidian Hybrid Search, công cụ tìm ghi chú Obsidian theo nghĩa và từ khoá, đang có điểm cắm để thêm gói ngôn ngữ."
spine_context_lines: [profile, "claude:c4caee3c#L1114"]
spine_want: Chứng minh một gói ngôn ngữ thứ hai chạy qua điểm cắm mà không phải sửa lõi.
spine_want_lines: ["claude:c4caee3c#L816"]
spine_action: Viết gói tiếng Đức và chạy qua điểm cắm P01.
spine_action_lines: ["claude:c4caee3c#L816"]
spine_outcome: "nDCG@5 trên bộ eval tiếng Đức tăng từ 0,57 lên 0,97, không hạng mục nào tụt."
spine_outcome_lines: ["claude:c4caee3c#L816"]
spine_takeaway: Viết gói ngôn ngữ thứ hai là cách kiểm tra điểm cắm có tổng quát thật hay không.
spine_takeaway_lines: ["claude:c4caee3c#L816"]
completeness: 5
---

# Gói tiếng Đức chạy qua điểm cắm mà không sửa lõi: nDCG@5 từ 0,57 lên 0,97

**Bối cảnh:** Mục tiêu của điểm cắm gói ngôn ngữ là chứng minh một gói thứ hai chạy được mà không phải chỉnh lõi.
**Chuyện gì xảy ra:** Agent viết gói tiếng Đức với tách từ ghép bằng quy hoạch động trên từ điển gốc và chạy qua điểm cắm P01. Trên bộ eval tiếng Đức, nDCG@5 tăng từ 0,57 lên 0,97, không hạng mục nào tụt. Đây là bằng chứng để tin điểm cắm đủ tổng quát.
**Bài học:** Viết gói thứ hai là cách kiểm tra điểm cắm thật sự tổng quát, không chỉ đúng với gói đầu.
**Artefact:** Bảng nDCG@5 trước và sau cho bộ eval tiếng Đức.
