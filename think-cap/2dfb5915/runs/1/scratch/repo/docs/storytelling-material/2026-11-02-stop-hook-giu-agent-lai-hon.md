---
id: 2026-11-02-stop-hook-giu-agent-lai-hon
date: 2026-11-02
repo: repo
status: raw
signals: [người duyệt, khác]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:2dfb5915#L477", "claude:2dfb5915#L2147", "claude:2dfb5915#L2539", "claude:2dfb5915#L2872"]
hook: "Hook giữ agent lại hơn 20 lượt, dù việc làm được đã hết"
tension: cam_ma_van_lot
sides: ["Hook bắt agent làm tiếp", "Không còn việc nào làm được trên máy này"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Stop hook giữ agent lại hơn 20 lượt vì điều kiện cần cổng người

**Bối cảnh:** Điều kiện goal yêu cầu hoàn tất toàn bộ plan, trong đó có các cổng chỉ user mở.
**Chuyện gì xảy ra:** Hook chặn dừng lặp lại với cùng lý do hơn 20 lần. User đã thu hẹp phạm vi tới bản cài được, nhưng điều kiện vẫn chưa thoả. Agent lặp đi lặp lại việc nói rõ không còn việc làm được trên máy này. Phiên dừng khi user xoá goal.
**Bài học:** Điều kiện dừng nên bám theo phạm vi user đã chốt, và cổng người phải được nêu rõ trong điều kiện để không bị kẹt.
**Artefact:** Không có.
