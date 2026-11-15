---
id: 2026-11-01-chay-that-lan-dau-3-model
date: 2026-11-01
repo: repo
status: raw
signals: [artefact nhìn được, số trước số sau]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:f0bf048d#L3139", "claude:f0bf048d#L3165", "claude:f0bf048d#L3199"]
hook: "Chạy thật lần đầu: model chạy khác model đã cấu hình, Google chặn luôn"
tension: tuong_ma_hoa_ra
sides: ["Cấu hình đặt gpt-5.5 và grok-4.6, 5 issue chạy không lỗi", "Thực tế chạy gpt-6.1-sol và grok-4.7, chỉ Bing còn tìm được"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Chạy thật lần đầu: 3 model khác nhau, 1 lệnh tìm kiếm bị chặn

**Bối cảnh:** Sau khi nối ba runtime (OpenAI, Grok, Gemini), chưa runtime nào chạy một lượt thật cho đến khi chủ yêu cầu.
**Chuyện gì xảy ra:** Hai agent thử (Pi·OpenAI, Pi·Grok) chạy 5 issue, không lỗi. Model thực tế khác model trong cấu hình: gpt-6.1-sol và grok-4.7 thay vì gpt-5.5 và grok-4.6. Google và DuckDuckGo chặn truy cập từ máy chủ (429, CAPTCHA), chỉ Bing còn dùng được. Gemini chạy trong khoảng 30 giây, đúng model đặt trong cấu hình.
**Bài học:** Kiểm trạng thái online không đủ; phải giao một việc thật, và đọc model thực từ thống kê token, vì model có thể khác cấu hình.
**Artefact:** Bảng 5 issue với kết quả (đọc web, gom issue con, comment, done); che ID và tên agent.
**Góc người ngoài:** cách làm phổ biến là Chỉ kiểm tra trạng thái online trên dashboard hoặc chạy lệnh --version rồi coi là đã dùng được; ở đây khác ở Kiểm bằng lượt chạy thật phát hiện được những khác biệt như model thực tế khác model khai báo và công cụ bị chặn. Người đọc muốn biết cách kiểm tra như vậy thay vì tin cấu hình.
