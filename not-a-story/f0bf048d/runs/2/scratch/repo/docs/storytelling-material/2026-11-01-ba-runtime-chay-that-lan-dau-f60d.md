---
id: 2026-11-01-ba-runtime-chay-that-lan-dau-f60d
code: M-E1ZV
aliases: [M-E1ZV]
date: 2026-11-01
repo: repo
status: raw
signals: [so_truoc_so_sau, nguyen_nhan_bat_ngo]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L3139", "claude:f0bf048d#L3146", "claude:f0bf048d#L3151", "claude:f0bf048d#L3165"]
hook: "Model chạy thật khác cấu hình, Google và DuckDuckGo chặn"
tension: tuong_ma_hoa_ra
sides: ["Cấu hình ghi gpt-5.5 và grok-4.6", "Thống kê token cho thấy gpt-6.1-sol và grok-4.7"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một team marketing muốn có agent AI làm SEO, theo dõi GA4 và đọc số liệu, và người làm đang chạy thử ba runtime để dựng chúng. Agent tin cấu hình ghi model là gpt-5.5 và grok-4.6, nhưng thống kê token cho thấy model thật là gpt-6.1-sol và grok-4.7. Người dựng agent nên quan tâm vì cấu hình không đủ để biết agent đang chạy model nào, và công cụ tìm kiếm có thể bị chặn ngay trên máy chủ, nên agent SEO phải đi qua API."
audience: dev dựng agent AI cho team không chuyên kỹ thuật
spine_context: "Team marketing cần agent AI cho SEO, GA4 và đọc phân tích số liệu. Người làm đã đăng nhập cả 3 runtime."
spine_context_lines: ["claude:f0bf048d#L7", "claude:f0bf048d#L2890"]
spine_want: "Muốn có agent làm SEO, theo dõi GA4 và đọc số liệu cho team marketing."
spine_want_lines: ["claude:f0bf048d#L7"]
spine_obstacle: "Chưa có agent nào làm SEO, GA4 hay đọc số liệu."
spine_obstacle_lines: ["claude:f0bf048d#L7"]
spine_turn: Agent tưởng model chạy là gpt-5.5 và grok-4.6 theo cấu hình; thống kê token cho thấy model thật là gpt-6.1-sol và grok-4.7.
spine_turn_lines: ["claude:f0bf048d#L3165"]
spine_action: "Tạo hai agent thử, spike-pi-web và spike-grok-web, rồi chạy 5 issue trên đó."
spine_action_lines: ["claude:f0bf048d#L3165"]
spine_outcome: "Cả 5 issue chạy xong không lỗi. Google chặn bằng lỗi 429, DuckDuckGo đòi CAPTCHA, chỉ Bing còn dùng được."
spine_outcome_lines: ["claude:f0bf048d#L3139", "claude:f0bf048d#L3165"]
spine_takeaway: Đọc model thật từ thống kê sử dụng thay vì cấu hình. Đo công cụ tìm kiếm trên máy chủ trước khi phụ thuộc vào nó.
spine_takeaway_lines: ["claude:f0bf048d#L3165"]
completeness: 7
---

# Ba runtime chạy thật lần đầu: model khác cấu hình, Google và DuckDuckGo chặn máy chủ

**Góc kể:** Một team marketing muốn có agent AI làm SEO, theo dõi GA4 và đọc số liệu, và người làm đang chạy thử ba runtime để dựng chúng. Agent tin cấu hình ghi model là gpt-5.5 và grok-4.6, nhưng thống kê token cho thấy model thật là gpt-6.1-sol và grok-4.7. Người dựng agent nên quan tâm vì cấu hình không đủ để biết agent đang chạy model nào, và công cụ tìm kiếm có thể bị chặn ngay trên máy chủ, nên agent SEO phải đi qua API.
**Bối cảnh:** Người vận hành yêu cầu kiểm chạy thật. Agent tạo hai agent thử và giao năm issue nhỏ.
**Chuyện gì xảy ra:** Năm issue chạy xong, không lỗi. Model thực tế khác cấu hình: thống kê token ghi gpt-6.1-sol và grok-4.7, trong khi cấu hình là gpt-5.5 và grok-4.6. Google chặn máy chủ với lỗi 429, DuckDuckGo đòi CAPTCHA, chỉ Bing còn dùng được. Agent SEO nên đi qua API thay vì cào trang tìm kiếm.
**Bài học:** Đừng tin model trong cấu hình. Hãy đọc model thật từ thống kê sử dụng, và đo công cụ tìm kiếm trên máy chủ trước khi trông cậy vào nó.
**Artefact:** Bảng năm issue với kết quả và trạng thái.
