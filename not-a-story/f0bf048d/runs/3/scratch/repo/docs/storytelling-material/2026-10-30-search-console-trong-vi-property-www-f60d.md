---
id: 2026-10-30-search-console-trong-vi-property-www-f60d
code: M-WZ7Q
aliases: [M-WZ7Q]
date: 2026-10-30
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo, so_truoc_so_sau]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L915", "claude:f0bf048d#L920"]
hook: "Search Console trống trơn: quyền cấp nhầm cho property www cũ 0 lượt hiển thị"
tension: tuong_ma_hoa_ra
sides: ["Tưởng Search Console trống là lỗi quyền truy cập", "Quyền cấp cho property www cũ, site đã 301 sang không www, 0 lượt từ tháng 7"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Search Console trống vì property www cũ trong khi site 301 sang không www

**Bối cảnh:** Search Console không có số liệu cho website của khách dù đã cấp quyền cho service account.
**Chuyện gì xảy ra:** Website chuyển hướng 301 từ www sang không www. Property đã cấp quyền là bản www cũ, có 0 lượt hiển thị từ tháng 7. Lỗi này là chuyện agent phải tự phát hiện bằng công cụ có sẵn, không phải lỗi quyền truy cập.
**Bài học:** Với Search Console, phải chọn đúng property (kể cả www hay không www) trước khi kết luận là không có dữ liệu.
**Artefact:** Dropdown property trong Search Console (che tên miền).
