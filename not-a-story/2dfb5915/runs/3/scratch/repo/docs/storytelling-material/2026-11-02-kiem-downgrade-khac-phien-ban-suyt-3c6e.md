---
id: 2026-11-02-kiem-downgrade-khac-phien-ban-suyt-3c6e
code: M-TF32
aliases: [M-TF32]
date: 2026-11-02
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L3286", "claude:2dfb5915#L3299"]
hook: "Kiểm «khác phiên bản» suýt hạ cấp gói OHS đang mới hơn"
tension: giup_ma_hai
sides: ["Kiểm khác phiên bản để giữ gói đúng bản ghim", "Máy có vantt.4 mới hơn lại bị hạ về vantt.3"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Kiểm downgrade: «khác phiên bản» suýt hạ cấp gói OHS đang mới hơn

**Bối cảnh:** Nhánh từ máy Windows thay gói OHS trong thư mục của pkm khi phiên bản khác bản ghim.
**Chuyện gì xảy ra:** Nếu máy đã có vantt.4 mới hơn trong khi bản ghim là vantt.3, nhánh gốc sẽ hạ cấp về vantt.3. Agent đổi sang so sánh thứ tự phiên bản, chỉ nâng khi gói cũ hơn hoặc không rõ phiên bản, và không bao giờ ghi đè gói đưa vào bằng --ohs.
**Bài học:** So sánh «khác» với «cũ hơn» là hai điều kiện khác nhau. Khi cài tự động, chỉ nâng cấp đúng chiều.
