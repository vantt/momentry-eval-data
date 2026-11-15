---
id: 2026-10-21-bon-agent-soat-cheo-nhau-con
date: 2026-10-21
repo: repo
status: raw
signals: [người duyệt thứ máy soạn, nguyên nhân bất ngờ]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L1399", "claude:9514b261#L1432", "claude:9514b261#L1447", "claude:9514b261#L1476", "claude:9514b261#L1477", "claude:9514b261#L1482", "claude:9514b261#L1511", "claude:9514b261#L1572"]
hook: "Subagent báo 332/332 đã migrate, chạy lại chỉ có 332/147"
tension: tuong_ma_hoa_ra
sides: ["Subagent báo toàn bộ 332 doc đã migrate", "Chạy lại lệnh đếm: 332 provisional, 147 active, không khớp"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Bốn agent soát chéo nhau: con số của subagent cần chạy lại trước khi kết luận

**Bối cảnh:** Ba agent researcher quét song song plans, history và work item để tìm trùng lặp với Knowledge and Documentation Engine. Agent chính đọc lại báo cáo và tự kiểm các điểm quan trọng.
**Chuyện gì xảy ra:** Registry tài liệu có 479 doc, 332 doc đang provisional và 147 active; có doc đã provisional 47 đến 55 ngày. Check doc-provisional-aged không bao giờ bắn vì nó trừ hai chuỗi thời gian ISO, cho kết quả NaN. Agent chạy lại đúng lệnh đếm và xác nhận 332/147, còn con số “332/332 đã migrate” từ subagent không được xác nhận.
**Bài học:** Đừng đưa con số của subagent vào kết luận khi chưa chạy lại lệnh đếm; check cảnh báo có thể không bao giờ bắn mà không ai hay.
**Artefact:** Đoạn so sánh thời gian: now trừ một chuỗi ISO cho NaN, kèm bảng số đã kiểm và số đã không kiểm được.
