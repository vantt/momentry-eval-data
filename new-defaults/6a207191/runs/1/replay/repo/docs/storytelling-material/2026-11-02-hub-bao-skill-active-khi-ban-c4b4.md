---
id: 2026-11-02-hub-bao-skill-active-khi-ban-c4b4
code: M-QFMQ
aliases: [M-QFMQ]
date: 2026-11-02
repo: repo
status: raw
signals: [rang_buoc_thiet_ke, nguyen_nhan_bat_ngo]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:6a207191#L1040", "claude:6a207191#L1060", "claude:6a207191#L1183", "claude:6a207191#L1489", "claude:6a207191#L1503", "claude:6a207191#L1507", "claude:6a207191#L1515"]
hook: "Trang skill báo active, nhưng bản mới đang chờ duyệt không hiện đâu cả"
tension: cam_ma_van_lot
sides: ["Trang skill hiển thị bản active", "Bản mới chờ duyệt nằm ngoài, người duyệt dễ duyệt nhầm bản cũ"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Hub báo skill active khi bản mới còn chờ duyệt, và skill-curator không có trên máy khách

**Bối cảnh:** Bản gửi mới đã được đưa lên hub. Người dùng mở web thấy skill vẫn active và tưởng bản mới đã được duyệt.
**Chuyện gì xảy ra:** Agent không kích hoạt được skill-curator trên máy khách, vì skillstation chỉ cài curator trên máy chạy hub; skill_get trả not_found. Bản đang active trên hub là bản của một lần duyệt trước. Bản gửi mới nằm riêng trong Waiting for review và không gắn gì vào trang skill. Vì thế trang skill không cảnh báo có bản chờ duyệt, và người duyệt dễ duyệt nhầm bản cũ.
**Bài học:** Bản đang chạy và bản chờ duyệt phải hiển thị ở cùng một chỗ; nếu không người vận hành sẽ tin nhầm bản mình đang xem.
**Artefact:** Ảnh trang skill trước khi có banner, đặt cạnh mục Waiting for review. Cần che mã SUB và tên máy.
