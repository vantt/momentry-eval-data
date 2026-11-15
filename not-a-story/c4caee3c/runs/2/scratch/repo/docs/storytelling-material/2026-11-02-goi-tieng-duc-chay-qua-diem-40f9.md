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
hook: "Gói tiếng Đức cắm vào mà không sửa lõi: 0,57 lên 0,97"
tension: it_ma_nhieu
sides: ["Không sửa dòng nào ở lõi", "Điểm tìm kiếm tiếng Đức nhảy từ 0,57 lên 0,97"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: none
spine_context: "Dự án Obsidian Hybrid Search, công cụ tìm kiếm cho vault Obsidian chạy local, đang làm lộ trình fork."
spine_context_lines: [profile]
spine_action: "Gói tiếng Đức (V21) chạy qua điểm cắm P01 mà không sửa lõi, đã commit và push `fedc3d0`."
spine_action_lines: ["claude:c4caee3c#L816"]
spine_outcome: "nDCG@5 tăng từ 0,57 lên 0,97, không hạng mục nào tụt."
spine_outcome_lines: ["claude:c4caee3c#L816"]
completeness: 3
---

# Gói tiếng Đức chạy qua điểm cắm mà không sửa lõi, nDCG@5 từ 0,57 lên 0,97

**Bối cảnh:** Mục tiêu của P01 là điểm cắm đủ tổng quát cho mọi ngôn ngữ. Gói tiếng Đức là bài kiểm chứng đầu tiên.
**Chuyện gì xảy ra:** Gói ohs-lang-de có tách từ ghép bằng quy hoạch động, bỏ dấu và danh sách từ dừng, và chạy qua P01 không cần đổi lõi. nDCG@5 tăng từ 0,57 lên 0,97, không hạng mục nào tụt. Lead dùng kết quả này làm bằng chứng điểm cắm đã tổng quát.
**Bài học:** Thử một ngôn ngữ thứ hai sớm là cách kiểm điểm cắm có thật sự tổng quát hay không.
**Artefact:** Bảng nDCG@5 trước và sau, không kèm dữ liệu.
