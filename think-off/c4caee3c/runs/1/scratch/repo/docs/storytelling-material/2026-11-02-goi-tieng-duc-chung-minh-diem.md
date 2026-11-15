---
id: 2026-11-02-goi-tieng-duc-chung-minh-diem
date: 2026-11-02
repo: repo
status: raw
signals: []
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L780", "claude:c4caee3c#L816", "claude:c4caee3c#L1114", "claude:c4caee3c#L1711"]
hook: "Gói tiếng Đức chạy không sửa lõi, nDCG@5 từ 0,57 lên 0,97"
tension: it_ma_nhieu
sides: ["Không sửa dòng nào ở lõi", "nDCG@5 tiếng Đức tăng 0,57 lên 0,97, không hạng mục nào tụt"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Gói tiếng Đức chứng minh điểm cắm ngôn ngữ dùng được cho ngôn ngữ khác

**Bối cảnh:** Điểm cắm ngôn ngữ (P01) được thiết kế để nhiều gói có thể cắm vào mà không sửa lõi. Gói tiếng Đức là bài kiểm.
**Chuyện gì xảy ra:** Gói ohs-lang-de chạy qua P01 không cần sửa lõi nào. Trong eval tiếng Đức, nDCG@5 tăng từ 0,57 lên 0,97 và không hạng mục nào tụt. Đồng thời đây là bằng chứng cho điểm cắm chung, không chỉ cho tiếng Việt.
**Bài học:** Thử một ngôn ngữ thứ hai sớm là cách kiểm nhanh một điểm cắm có thật sự tổng quát không.
**Artefact:** Bảng 0,57 đến 0,97 theo hạng mục, không kèm mẫu câu.
