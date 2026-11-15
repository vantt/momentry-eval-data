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
hook: "Model chạy thật là gpt-6.1-sol, không phải gpt-5.5 đã cấu hình"
tension: tuong_ma_hoa_ra
sides: ["Cấu hình ghi gpt-5.5 và grok-4.6", "Thống kê token cho thấy chạy gpt-6.1-sol và grok-4.7"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Người làm đang dựng hệ thống giao việc cho agent AI chạy trên ba runtime và muốn biết chúng có chạy thật không. Họ tin model đang chạy là gpt-5.5 và grok-4.6 theo đúng cấu hình. Thống kê token cho thấy model thật là gpt-6.1-sol và grok-4.7, nên file cấu hình không đáng tin để biết model nào đang xử lý việc. Ai chạy agent với nhiều model nên đọc model từ thống kê sử dụng, không đọc từ cấu hình."
audience: dev dùng agent AI và muốn biết model thật đang chạy trong hệ thống của mình
spine_context: "Người làm đang dựng hệ thống giao việc cho agent AI (multica) chạy trên ba runtime: Pi·OpenAI, Pi·Grok và Gemini qua omp."
spine_context_lines: ["claude:f0bf048d#L2890", "claude:f0bf048d#L3165"]
spine_want: "Muốn kiểm xem ba runtime có chạy thật không, không chỉ cấu hình xong."
spine_want_lines: ["claude:f0bf048d#L3079"]
spine_obstacle: Gemini (omp) chưa có lượt chạy nào; Google và DuckDuckGo chặn truy cập từ máy chủ.
spine_obstacle_lines: ["claude:f0bf048d#L3165"]
spine_turn: Tưởng model chạy là gpt-5.5 và grok-4.6 theo cấu hình; hoá ra thống kê ghi gpt-6.1-sol và grok-4.7.
spine_turn_lines: ["claude:f0bf048d#L3165"]
spine_action: "Chạy năm issue nhỏ trên hai agent thử, rồi đọc thống kê token của runtime."
spine_action_lines: ["claude:f0bf048d#L3133", "claude:f0bf048d#L3165"]
spine_outcome: Năm issue chạy xong không lỗi; trong các công cụ tìm kiếm chỉ Bing còn dùng được.
spine_outcome_lines: ["claude:f0bf048d#L3165"]
spine_takeaway: "Đừng tin model trong cấu hình: đọc model thật từ thống kê sử dụng, và đo công cụ tìm kiếm trên máy chủ trước khi dựa vào nó."
spine_takeaway_lines: ["claude:f0bf048d#L3133", "claude:f0bf048d#L3165"]
completeness: 7
---

# Ba runtime chạy thật lần đầu: model khác cấu hình, Google và DuckDuckGo chặn máy chủ

**Góc kể:** Người làm đang dựng hệ thống giao việc cho agent AI chạy trên ba runtime và muốn biết chúng có chạy thật không. Họ tin model đang chạy là gpt-5.5 và grok-4.6 theo đúng cấu hình. Thống kê token cho thấy model thật là gpt-6.1-sol và grok-4.7, nên file cấu hình không đáng tin để biết model nào đang xử lý việc. Ai chạy agent với nhiều model nên đọc model từ thống kê sử dụng, không đọc từ cấu hình.
**Bối cảnh:** Người vận hành yêu cầu kiểm chạy thật. Agent tạo hai agent thử và giao năm issue nhỏ.
**Chuyện gì xảy ra:** Năm issue chạy xong, không lỗi. Model thực tế khác cấu hình: thống kê token ghi gpt-6.1-sol và grok-4.7, trong khi cấu hình là gpt-5.5 và grok-4.6. Google chặn máy chủ với lỗi 429, DuckDuckGo đòi CAPTCHA, chỉ Bing còn dùng được. Agent SEO nên đi qua API thay vì cào trang tìm kiếm.
**Bài học:** Đừng tin model trong cấu hình. Hãy đọc model thật từ thống kê sử dụng, và đo công cụ tìm kiếm trên máy chủ trước khi trông cậy vào nó.
**Artefact:** Bảng năm issue với kết quả và trạng thái.
