---
id: 2026-11-02-goi-tieng-duc-chay-qua-diem-40f9
code: M-MYST
aliases: [M-MYST]
date: 2026-11-02
repo: repo
status: raw
signals: [số trước sau, ràng buộc định hình thiết kế]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L780", "claude:c4caee3c#L816", "claude:c4caee3c#L1114"]
hook: "Gói tiếng Đức nâng nDCG từ 0,57 lên 0,97 mà không sửa lõi"
tension: it_ma_nhieu
sides: ["không động vào mã lõi", "điểm tăng từ 0,57 lên 0,97, không hạng mục nào tụt"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Gói tiếng Đức chạy qua điểm cắm mà không sửa lõi: nDCG@5 0,57 lên 0,97

**Bối cảnh:** Ngôn ngữ thứ hai dùng cùng điểm cắm để kiểm tra hợp đồng có đủ tổng quát không.
**Chuyện gì xảy ra:** Gói chuẩn hoá, tách từ ghép bằng quy hoạch động trên từ điển gốc và loại từ chức năng, chạy qua P01 mà không sửa lõi. nDCG@5 từ 0,57 lên 0,97, không hạng mục nào tụt.
**Bài học:** Viết gói ngôn ngữ thứ hai là kiểm tra thật cho hợp đồng plug-in; nếu phải sửa lõi thì hợp đồng chưa đủ tổng quát.
**Artefact:** Bảng nDCG@5 trước và sau.
