---
id: 2026-10-30-hub-skill-qua-proxy-systemd-protecthome-f60d
code: M-50S6
aliases: [M-50S6]
date: 2026-10-30
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L606", "claude:f0bf048d#L2194"]
hook: "Gọi skill qua HTTP trả đường dẫn trong home chủ, agent không đọc được"
tension: cam_ma_van_lot
sides: ["skill_get trả về đường dẫn hợp lệ", "ProtectHome giấu home của chủ khỏi daemon"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Hub skill qua proxy: systemd ProtectHome giấu home của chủ nên không gọi HTTP thẳng được

**Bối cảnh:** Thiết kế hub skill dùng chung cho các daemon; phía agent chạy dưới user daemon có sandbox systemd.
**Chuyện gì xảy ra:** Daemon chạy với ProtectHome=tmpfs nên không thấy home của chủ. Gọi skill_get qua HTTP sẽ trả đường dẫn nằm trong home chủ mà agent không đọc được. Vì vậy phải dùng proxy kéo skill về cache của chính user daemon và kiểm digest.
**Bài học:** Khi dùng sandbox systemd, kiểm xem đường dẫn dịch vụ trả về có nằm trong vùng sandbox không.
**Artefact:** Sơ đồ hai đường: HTTP thẳng và qua proxy.
