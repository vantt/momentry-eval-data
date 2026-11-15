---
id: 2026-10-30-search-console-tro-sai-property-0-f60d
code: M-J3ME
aliases: [M-J3ME]
date: 2026-10-30
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo, so_truoc_so_sau]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L749", "claude:f0bf048d#L915", "claude:f0bf048d#L929"]
hook: "Search Console báo 0 lượt hiển thị từ tháng 7: trỏ nhầm bản www"
tension: tuong_ma_hoa_ra
sides: ["Tưởng traffic về 0 từ tháng 7", "Property cấp quyền là bản www cũ, site đã redirect"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một người làm đang dựng bộ agent marketing, bắt đầu với một website khách, để agent tự đọc số liệu GA4 và Search Console rồi làm SEO. Người làm tưởng property vừa cấp quyền trong Search Console là site đang chạy, nhưng hoá ra đó là bản www cũ: site đã chuyển hướng 301 sang bản không www, nên property cũ chỉ còn số 0 từ tháng 7. Ai cho agent đọc số liệu cũng dễ gặp chuyện này, vì số 0 trông như traffic sụp trong khi thực ra chỉ là đọc nhầm nơi."
audience: dev và người làm marketing cho agent đọc số liệu GA4 hoặc Search Console
spine_context: "Một người làm đang dựng bộ agent marketing, bắt đầu với một website khách, để agent tự đọc số liệu GA4 và Search Console rồi làm SEO."
spine_context_lines: ["claude:f0bf048d#L7", "claude:f0bf048d#L747"]
spine_want: Muốn agent đọc được số liệu GA4 và Search Console để làm SEO.
spine_want_lines: ["claude:f0bf048d#L675"]
spine_obstacle: Cả hai công cụ trả về rỗng vì service account chưa được cấp quyền vào property nào.
spine_obstacle_lines: ["claude:f0bf048d#L749", "claude:f0bf048d#L751"]
spine_turn: "Tưởng property vừa cấp quyền là site đang chạy; hoá ra là bản www cũ, site đã chuyển hướng 301 sang bản không www, và chỉ có số 0 từ tháng 7."
spine_turn_lines: ["claude:f0bf048d#L761", "claude:f0bf048d#L915"]
spine_action: "Giao cho agent SEO một issue không nêu trước lỗi www, để xem agent có tự phát hiện không."
spine_action_lines: ["claude:f0bf048d#L929"]
spine_outcome: "GA4 đã có số liệu thật, kênh Direct 58 session trong 7 ngày; Search Console vẫn chưa có số liệu vì đang cấp nhầm property."
spine_outcome_lines: ["claude:f0bf048d#L915"]
spine_takeaway: "Trước khi tin số 0 từ công cụ đọc số liệu, kiểm property nào là bản chính thức (domain hay URL, www hay không www)."
spine_takeaway_lines: ["claude:f0bf048d#L915"]
completeness: 7
---

# Search Console trỏ sai property: 0 lượt hiển thị từ tháng 7

**Góc kể:** Một người làm đang dựng bộ agent marketing, bắt đầu với một website khách, để agent tự đọc số liệu GA4 và Search Console rồi làm SEO. Người làm tưởng property vừa cấp quyền trong Search Console là site đang chạy, nhưng hoá ra đó là bản www cũ: site đã chuyển hướng 301 sang bản không www, nên property cũ chỉ còn số 0 từ tháng 7. Ai cho agent đọc số liệu cũng dễ gặp chuyện này, vì số 0 trông như traffic sụp trong khi thực ra chỉ là đọc nhầm nơi.
**Bối cảnh:** Gắn MCP GA4 và Search Console cho agent SEO để đọc số liệu của website khách đầu tiên.
**Chuyện gì xảy ra:** Service account xác thực được với cả GA4 lẫn Search Console, nhưng cả hai trả về rỗng vì chưa được cấp quyền. Sau khi cấp quyền, Search Console chỉ có số 0 từ tháng 7. Website đã redirect 301 từ bản www sang bản không www, còn property được cấp quyền là bản www cũ. Để kiểm agent, issue giao việc không kể trước lỗi này, xem agent có tự phát hiện không.
**Bài học:** Khi cấp quyền cho công cụ đọc số liệu, kiểm xem property nào đang là bản chính thức (domain hay URL, www hay không www) trước khi tin vào số 0.
**Artefact:** Ảnh dropdown chọn property trong Search Console, che email service account và tên miền nếu cần.
