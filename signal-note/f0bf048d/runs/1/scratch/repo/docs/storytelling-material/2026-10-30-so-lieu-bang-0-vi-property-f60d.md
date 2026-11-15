---
id: 2026-10-30-so-lieu-bang-0-vi-property-f60d
code: M-F5JN
aliases: [M-F5JN]
date: 2026-10-30
repo: repo
status: raw
signals: [so_truoc_so_sau, nguyen_nhan_bat_ngo]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L749", "claude:f0bf048d#L783", "claude:f0bf048d#L915"]
hook: "GA4 có 58 session, Search Console lại báo 0 lượt hiển thị"
tension: tuong_ma_hoa_ra
sides: ["GA4 trả 58 session trong 7 ngày", "Search Console 0 vì cấp quyền nhầm bản www cũ"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một team marketing đang dựng bộ agent SEO và phân tích cho website bán hàng, để agent tự đọc số liệu GA4 và Search Console thay vì người làm tay. Họ tin property đã cấp quyền là đúng site, nên số 0 ở Search Console nghĩa là website chưa có lượt hiển thị. Hoá ra property đó là bản www cũ, còn site đã chuyển hướng 301 sang bản không www. Người làm agent nên kiểm redirect trước khi tin một con số 0."
audience: dev và người làm marketing đang nối AI với GA4 và Search Console
spine_context: "Một team marketing đang dựng bộ agent SEO và phân tích cho website bán hàng, để agent tự đọc số liệu GA4 và Search Console."
spine_context_lines: ["claude:f0bf048d#L7", "claude:f0bf048d#L920"]
spine_want: Muốn agent đọc được số liệu thật từ GA4 và Search Console để làm SEO.
spine_want_lines: ["claude:f0bf048d#L675"]
spine_obstacle: "Search Console trả về toàn số 0, trong khi GA4 đã có số liệu."
spine_obstacle_lines: ["claude:f0bf048d#L783"]
spine_turn: "Tưởng property đã cấp quyền là đúng site, nên số 0 nghĩa là chưa có lượt hiển thị; hoá ra đó là bản www cũ, site đã chuyển hướng 301 sang bản không www."
spine_turn_lines: ["claude:f0bf048d#L761", "claude:f0bf048d#L915"]
spine_action: "Giao việc tìm property đúng và chẩn đoán cho SEO Specialist qua issue, thay vì tự làm thay agent."
spine_action_lines: ["claude:f0bf048d#L923"]
spine_outcome: Chưa có số liệu Search Console; lịch báo cáo tuần đang paused chờ property đúng.
spine_outcome_lines: ["claude:f0bf048d#L915"]
spine_takeaway: Một domain có thể có nhiều property trong Search Console; kiểm redirect và chọn đúng property trước khi tin số 0.
spine_takeaway_lines: ["claude:f0bf048d#L915"]
completeness: 7
---

# Số liệu bằng 0 vì property Search Console cũ bản www

**Góc kể:** Một team marketing đang dựng bộ agent SEO và phân tích cho website bán hàng, để agent tự đọc số liệu GA4 và Search Console thay vì người làm tay. Họ tin property đã cấp quyền là đúng site, nên số 0 ở Search Console nghĩa là website chưa có lượt hiển thị. Hoá ra property đó là bản www cũ, còn site đã chuyển hướng 301 sang bản không www. Người làm agent nên kiểm redirect trước khi tin một con số 0.
**Bối cảnh:** Sau khi có key, agent gọi thử API để kiểm xác thực. Lần đầu trả về rỗng vì chưa cấp quyền cho service account.
**Chuyện gì xảy ra:** Sau khi chủ cấp quyền, GA4 trả về số liệu thật: kênh Direct có 58 session trong 7 ngày. Search Console trả về 0 lượt hiển thị từ tháng 7. Website đã chuyển hướng 301 từ bản www sang bản không www, nhưng property được cấp quyền là bản www cũ.
**Bài học:** Một domain có thể có nhiều property trong Search Console. Kiểm redirect trước khi tin số 0.
**Artefact:** Bảng số 0 theo ngày trong Search Console (che tên site và property ID).
