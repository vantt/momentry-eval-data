---
id: 2026-10-21-may-kiem-han-tuoi-chua-tung
date: 2026-10-21
repo: repo
status: raw
signals: []
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L1476", "claude:9514b261#L1477", "claude:9514b261#L1482", "claude:9514b261#L1572"]
hook: "332 tài liệu quá hạn 47–55 ngày, máy cảnh báo chưa kêu lần nào"
tension: cam_ma_van_lot
sides: ["có máy kiểm hạn tuổi canh tài liệu", "phép trừ chuỗi ra NaN, 332 tài liệu quá hạn mà không cảnh báo"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Máy kiểm hạn tuổi chưa từng bắn: so chuỗi ISO với số ra NaN trong 47 đến 55 ngày

**Bối cảnh:** Registry tài liệu có check cảnh báo tài liệu provisional quá hạn.
**Chuyện gì xảy ra:** Check doc-provisional-aged so now với updatedAt, nhưng updatedAt là chuỗi ISO nên phép trừ ra NaN và điều kiện không bao giờ đúng. Có 332 tài liệu đang provisional, đã 47 đến 55 ngày mà không có cảnh báo nào.
**Bài học:** Một máy kiểm chưa từng báo gì không chứng minh repo sạch. Thử bằng một ca phải báo để chắc nó hoạt động.
**Artefact:** Đoạn so sánh now với updatedAt, và bảng 332 provisional đối 147 active.
