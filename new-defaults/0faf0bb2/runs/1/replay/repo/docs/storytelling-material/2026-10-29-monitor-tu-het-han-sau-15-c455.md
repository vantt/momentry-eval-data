---
id: 2026-10-29-monitor-tu-het-han-sau-15-c455
code: M-F2H6
aliases: [M-F2H6]
date: 2026-10-29
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L1205", "claude:0faf0bb2#L1228", "claude:0faf0bb2#L3502", "claude:0faf0bb2#L3592"]
hook: "Monitor tự chết sau 20 phút, kéo theo run đang chạy bị huỷ"
tension: cam_ma_van_lot
sides: ["Gắn monitor để theo dõi liên tục", "Nó tự hết hạn và run thành cancelled"]
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Monitor tự hết hạn sau 15 đến 25 phút, phải gắn lại để tiếp tục theo dõi

**Bối cảnh:** Theo dõi trạng thái run bằng Monitor trong lúc chờ agent làm việc.
**Chuyện gì xảy ra:** Monitor báo 'expires in 20m' rồi tự kết thúc. Lần đầu, luồng kết thúc khi run đang chạy, và trạng thái run đã thành cancelled. Agent phải gắn lại monitor và đọc lý do huỷ run từ log.
**Bài học:** Monitor có hạn sử dụng. Hãy đặt điều kiện thoát rõ ràng và gắn lại khi cần.
**Artefact:** Thông báo 'expires in 20m' của Monitor. Id đã che.
