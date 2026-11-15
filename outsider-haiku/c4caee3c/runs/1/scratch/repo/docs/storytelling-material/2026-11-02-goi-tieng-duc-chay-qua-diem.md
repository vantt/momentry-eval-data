---
id: 2026-11-02-goi-tieng-duc-chay-qua-diem
date: 2026-11-02
repo: repo
status: raw
signals: [Ràng buộc định hình thiết kế, "Số trước, số sau"]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L780", "claude:c4caee3c#L816", "claude:c4caee3c#L1114", "claude:c4caee3c#L1711"]
hook: "Gói tiếng Đức nâng nDCG@5 từ 0,57 lên 0,97 mà không sửa lõi"
tension: it_ma_nhieu
sides: ["không sửa dòng nào ở lõi", "nDCG@5 tiếng Đức từ 0,57 lên 0,97"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Gói tiếng Đức chạy qua điểm cắm P01 mà không sửa lõi: nDCG@5 0,57 lên 0,97

**Bối cảnh:** Mục tiêu là chứng minh điểm cắm gói ngôn ngữ mang tính chung, không gắn với tiếng Việt.
**Chuyện gì xảy ra:** Gói tiếng Đức có ghép từ, biến thể dấu và từ dừng chạy qua P01 mà không đổi lõi. nDCG@5 trên eval tiếng Đức tăng từ 0,57 lên 0,97, không hạng mục nào tụt. Sau đó vẫn phải bổ sung hợp đồng (viewTerms, trọng số view) để gói thật sự dùng được.
**Bài học:** Thử ngôn ngữ thứ hai sớm sẽ lộ ra chỗ nào trong lõi đang đóng đinh cho tiếng Việt.
**Artefact:** Bảng eval tiếng Đức trước và sau khi có gói.
