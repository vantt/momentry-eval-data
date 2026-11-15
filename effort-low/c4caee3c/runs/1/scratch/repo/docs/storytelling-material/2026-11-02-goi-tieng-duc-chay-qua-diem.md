---
id: 2026-11-02-goi-tieng-duc-chay-qua-diem
date: 2026-11-02
repo: repo
status: raw
signals: [số trước sau, ràng buộc định hình thiết kế]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L780", "claude:c4caee3c#L816", "claude:c4caee3c#L1114", "claude:c4caee3c#L1711"]
hook: "Thêm cả tiếng Đức mà không sửa lõi: nDCG từ 0,57 lên 0,97"
tension: it_ma_nhieu
sides: ["Không sửa dòng nào trong lõi", "nDCG@5 tiếng Đức từ 0,57 lên 0,97, không hạng mục nào tụt"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Gói tiếng Đức chạy qua điểm cắm mà không sửa lõi

**Bối cảnh:** Mục tiêu là chứng minh điểm cắm gói ngôn ngữ đủ tổng quát, nên gói thứ hai không được phép sửa lõi.
**Chuyện gì xảy ra:** Gói tiếng Đức được viết với tách từ ghép bằng quy hoạch động trên lexicon và đi qua cùng điểm cắm. Trên eval tiếng Đức nDCG@5 tăng từ 0,57 lên 0,97 và không hạng mục nào tụt. Số này được lặp lại qua nhiều báo cáo.
**Bài học:** Một gói thứ hai không sửa lõi là bài kiểm tra tốt nhất cho điểm cắm; nếu phải sửa lõi thì điểm cắm chưa đủ.
**Artefact:** Bảng nDCG@5 tiếng Đức trước và sau. Không cần che.
