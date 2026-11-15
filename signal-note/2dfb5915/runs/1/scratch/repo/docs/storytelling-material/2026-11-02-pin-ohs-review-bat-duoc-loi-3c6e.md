---
id: 2026-11-02-pin-ohs-review-bat-duoc-loi-3c6e
code: M-FVM2
aliases: [M-FVM2]
date: 2026-11-02
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L3286", "claude:2dfb5915#L3299"]
hook: "Bản vantt.4 người dùng đang chạy suýt bị ghi đè về vantt.3"
tension: giup_ma_hai
sides: ["Pin phiên bản để cài đặt ổn định", "Máy đang chạy bản mới bị hạ cấp"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Pin OHS: review bắt được lỗi hạ cấp, gói mới vantt.4 sẽ bị ghi đè về vantt.3

**Bối cảnh:** Nhánh từ máy Windows thay gói OHS mỗi khi phiên bản khác với bản ghim trong main, và bản ghim lúc đó là vantt.3.
**Chuyện gì xảy ra:** Máy người dùng đã chạy vantt.4 nên bị hạ về vantt.3 khi cài. Fix chỉ nâng khi gói cũ hơn hoặc không xác định được phiên bản; gói được đưa vào bằng cờ --ohs không bao giờ bị ghi đè. Có test cho cả hai.
**Bài học:** So khớp phiên bản phải là so sánh thứ tự, không phải so sánh bằng nhau; và đừng ghi đè thứ người dùng tự đưa vào.
**Artefact:** Bảng ba trường hợp: cũ hơn, bằng, mới hơn.
