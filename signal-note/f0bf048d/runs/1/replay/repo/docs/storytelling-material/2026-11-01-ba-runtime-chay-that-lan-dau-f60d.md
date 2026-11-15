---
id: 2026-11-01-ba-runtime-chay-that-lan-dau-f60d
code: M-E1ZV
aliases: [M-E1ZV]
date: 2026-11-01
repo: repo
status: raw
signals: [artefact_nhin_duoc, khac]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L3115", "claude:f0bf048d#L3139", "claude:f0bf048d#L3154", "claude:f0bf048d#L3159", "claude:f0bf048d#L3165", "claude:f0bf048d#L3193", "claude:f0bf048d#L3199"]
hook: "Model chạy thật là gpt-6.1-sol, không phải gpt-5.5 đã cấu hình"
tension: tuong_ma_hoa_ra
sides: ["cấu hình ghi gpt-5.5 và grok-4.6", "thống kê token ghi gpt-6.1-sol và grok-4.7"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Người làm đang dựng agent trên Multica cho team marketing, cần làm SEO, GA4 và đọc số liệu. Agent ghi model mình chạy là gpt-5.5 và grok-4.6 theo cấu hình, nhưng thống kê sử dụng cho thấy gpt-6.1-sol và grok-4.7. Ai cấu hình model theo tên có thể không biết model thật đang chạy, nên nên đọc thống kê để xác nhận."
audience: dev dùng agent AI và cấu hình nhiều model
spine_context: "Người làm đang dựng agent trên Multica cho team marketing, cần làm SEO, GA4 và đọc số liệu."
spine_context_lines: ["claude:f0bf048d#L7", "claude:f0bf048d#L2890"]
spine_want: "Muốn có agent chạy thật trên các runtime mới (OpenAI, Grok, Gemini) cho công việc marketing."
spine_want_lines: ["claude:f0bf048d#L7", "claude:f0bf048d#L2890"]
spine_obstacle: "Ba runtime mới đã đăng nhập nhưng chưa có lượt chạy thật; khi báo cáo, Gemini vẫn chưa chạy lượt nào."
spine_obstacle_lines: ["claude:f0bf048d#L2890", "claude:f0bf048d#L3165"]
spine_turn: Agent tưởng model chạy là gpt-5.5 và grok-4.6 theo cấu hình; hoá ra thống kê ghi gpt-6.1-sol và grok-4.7.
spine_turn_lines: ["claude:f0bf048d#L3165"]
spine_action: "Tạo agent thử spike-pi-web và spike-grok-web có Playwright, giao 5 issue; sau đó tạo spike-gemini và giao STU-15."
spine_action_lines: ["claude:f0bf048d#L3170", "claude:f0bf048d#L3199"]
spine_outcome: "Cả 5 issue chạy xong không lỗi; Gemini hoàn thành trong khoảng 30 giây và comment đúng một lần; Google trả 429, DuckDuckGo đòi CAPTCHA, chỉ Bing trả kết quả."
spine_outcome_lines: ["claude:f0bf048d#L3165", "claude:f0bf048d#L3199"]
spine_takeaway: "Model thật có thể khác cấu hình, nên đọc thống kê sử dụng để xác nhận; công cụ tìm kiếm có thể chặn IP máy chủ, nên đi qua API."
spine_takeaway_lines: ["claude:f0bf048d#L3165"]
completeness: 7
---

# Ba runtime chạy thật lần đầu: model khác cấu hình, Google và DuckDuckGo chặn máy chủ

**Góc kể:** Người làm đang dựng agent trên Multica cho team marketing, cần làm SEO, GA4 và đọc số liệu. Agent ghi model mình chạy là gpt-5.5 và grok-4.6 theo cấu hình, nhưng thống kê sử dụng cho thấy gpt-6.1-sol và grok-4.7. Ai cấu hình model theo tên có thể không biết model thật đang chạy, nên nên đọc thống kê để xác nhận.
**Bối cảnh:** Chủ hỏi 'kiểm tra xem, anh thấy chạy rồi đấy' sau khi runtime đã online.
**Chuyện gì xảy ra:** Thống kê token cho thấy Pi·OpenAI và Pi·Grok đã chạy 3 lượt mỗi bên qua 5 issue. Model ghi nhận là gpt-6.1-sol và grok-4.7, khác cấu hình gpt-5.5 và grok-4.6. Google trả 429, DuckDuckGo đòi CAPTCHA, chỉ Bing trả kết quả. Agent Gemini (omp) hoàn thành trong 30 giây, comment đúng một lần và chuyển in_review.
**Bài học:** Model thực tế có thể khác cấu hình, nên đọc thống kê sử dụng để xác nhận. Công cụ tìm kiếm chặn IP máy chủ, nên việc tìm kiếm cần đi qua API.
**Artefact:** Bảng 5 issue với kết quả (không đưa nội dung trả lời).
