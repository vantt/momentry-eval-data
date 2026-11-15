---
id: 2026-10-21-may-kiem-tuoi-tai-lieu-khong
date: 2026-10-21
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, số trước sau]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L1448", "claude:9514b261#L1476", "claude:9514b261#L1511"]
hook: "332 tài liệu quá hạn 55 ngày, máy cảnh báo vẫn im vì NaN"
tension: cam_ma_van_lot
sides: ["Có máy canh tài liệu quá hạn", "332 doc cũ 47-55 ngày không bị báo lần nào vì phép trừ ra NaN"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Máy kiểm tuổi tài liệu không bao giờ báo vì trừ chuỗi ngày ISO ra NaN

**Bối cảnh:** Knowledge Registry chạy thật trên main cho tài liệu end-user. Ba agent quét song song để dò trùng lắp với engine tài liệu đề xuất.
**Chuyện gì xảy ra:** Registry có 479 doc, trong đó 332 đang provisional và 147 active. Check cảnh báo doc provisional quá hạn trừ updatedAt là chuỗi ISO nên ra NaN, nên check chưa bao giờ bắn, trong khi 332 doc đã 47 đến 55 ngày. Cùng lúc có ba chỉ mục tài liệu song song với 492, 479 và 0 mục. Có 365 role khác nhau trên 479 doc, trong khi thiết kế là tập đóng nhỏ.
**Bài học:** Kiểm kiểu dữ liệu trước khi trừ thời gian. Một cảnh báo chưa từng bắn không chứng minh là không có vi phạm.
**Artefact:** Bảng ba chỉ mục với số mục và số provisional/active. Không kèm tên tài liệu.
