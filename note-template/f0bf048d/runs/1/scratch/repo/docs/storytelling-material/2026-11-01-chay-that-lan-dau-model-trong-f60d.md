---
id: 2026-11-01-chay-that-lan-dau-model-trong-f60d
code: M-5MHS
aliases: [M-5MHS]
date: 2026-11-01
repo: repo
status: raw
signals: [so_truoc_so_sau, nguyen_nhan_bat_ngo]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L3139", "claude:f0bf048d#L3165", "claude:f0bf048d#L3199"]
hook: "Config ghi gpt-5.5, thống kê lại ghi gpt-6.1-sol"
tension: tuong_ma_hoa_ra
sides: ["Cấu hình nói đang chạy model này", "Thống kê token cho thấy model khác hẳn"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Người làm đang đưa agent AI vào team marketing (làm SEO, đọc số liệu GA4) trên hệ thống giao việc multica, nên cần biết các runtime mới có chạy thật không. Họ tin cấu hình ghi model nào thì runtime chạy model đó, nhưng thống kê token lại cho thấy model khác: gpt-6.1-sol thay vì gpt-5.5, grok-4.7 thay vì grok-4.6. Ai cấu hình agent AI cũng nên đọc model thực tế từ thống kê, và đừng giả định trang tìm kiếm dùng được từ máy chủ."
audience: dev dùng AI muốn đưa agent vào công việc marketing hoặc kiểm model thực tế
spine_context: "Người làm đang đưa agent AI vào team marketing (làm SEO, đọc số liệu GA4) trên hệ thống giao việc multica."
spine_context_lines: ["claude:f0bf048d#L7", "claude:f0bf048d#L3129"]
spine_want: "Muốn biết các runtime mới (OpenAI, Grok, Gemini) có chạy thật trên hệ thống hay không."
spine_want_lines: ["claude:f0bf048d#L2890", "claude:f0bf048d#L3079"]
spine_obstacle: "Công cụ tìm kiếm trên máy chủ bị chặn: DuckDuckGo đòi CAPTCHA, Google trả lỗi 429, chỉ Bing trả kết quả."
spine_obstacle_lines: ["claude:f0bf048d#L3165"]
spine_turn: Tưởng cấu hình gpt-5.5 và grok-4.6 là model đang chạy; hoá ra thống kê token ghi gpt-6.1-sol và grok-4.7.
spine_turn_lines: ["claude:f0bf048d#L3165"]
spine_action: "Tạo hai agent thử, giao 5 issue, rồi thêm agent Gemini chạy issue STU-15."
spine_action_lines: ["claude:f0bf048d#L3165", "claude:f0bf048d#L3199"]
spine_outcome: "Cả 5 issue chạy xong không lỗi; Gemini hoàn thành trong khoảng 30 giây, comment đúng một lần rồi chuyển in_review."
spine_outcome_lines: ["claude:f0bf048d#L3165", "claude:f0bf048d#L3199"]
spine_takeaway: "Đọc model thực tế từ thống kê token, đừng đoán từ cấu hình; trang tìm kiếm thường chặn máy chủ, nên agent SEO nên lấy dữ liệu qua API."
spine_takeaway_lines: ["claude:f0bf048d#L3165"]
completeness: 7
---

# Chạy thật lần đầu: model trong thống kê khác cấu hình, Google và DuckDuckGo chặn máy chủ

**Góc kể:** Người làm đang đưa agent AI vào team marketing (làm SEO, đọc số liệu GA4) trên hệ thống giao việc multica, nên cần biết các runtime mới có chạy thật không. Họ tin cấu hình ghi model nào thì runtime chạy model đó, nhưng thống kê token lại cho thấy model khác: gpt-6.1-sol thay vì gpt-5.5, grok-4.7 thay vì grok-4.6. Ai cấu hình agent AI cũng nên đọc model thực tế từ thống kê, và đừng giả định trang tìm kiếm dùng được từ máy chủ.
**Bối cảnh:** Hai agent thử trên runtime Pi (OpenAI, Grok) mỗi bên chạy năm issue. Sau đó chạy thêm agent trên runtime omp (Gemini).
**Chuyện gì xảy ra:** Cấu hình ghi gpt-5.5 và grok-4.6, nhưng thống kê token ghi gpt-6.1-sol và grok-4.7. Khi đọc web, DuckDuckGo đòi CAPTCHA, Google trả 429, chỉ Bing trả kết quả. Agent báo blocked thay vì cào tiếp. Agent Gemini chạy xong trong khoảng 30 giây, viết đúng một comment rồi chuyển in_review.
**Bài học:** Đọc model thực tế từ thống kê, không đoán từ cấu hình. Công cụ tìm kiếm thường chặn IP máy chủ, nên agent SEO cần đi qua API.
**Artefact:** Bảng năm issue kết quả, không ghi id.
