---
id: 2026-11-01-luot-chay-that-dau-tien-tim
date: 2026-11-01
repo: repo
status: raw
signals: ["6", "2"]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L3139", "claude:f0bf048d#L3165", "claude:f0bf048d#L3199"]
hook: "5 issue xong không lỗi, nhưng Google và DuckDuckGo đều chặn máy chủ"
tension: tuong_ma_hoa_ra
sides: ["5 issue hoàn thành không báo lỗi", "Chỉ Bing trả kết quả, token ghi sai cả model"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Lượt chạy thật đầu tiên: tìm kiếm web bị chặn từ máy chủ

**Bối cảnh:** Chạy 5 issue thử trên runtime Pi và Grok, rồi thêm runtime Gemini qua omp.
**Chuyện gì xảy ra:** 5 issue đều hoàn thành không lỗi, nhưng nguồn tìm kiếm khác nhau: DuckDuckGo đòi CAPTCHA, Google trả 429 và chuyển sang trang sorry, chỉ Bing trả kết quả. Thống kê token ghi model khác model cấu hình (gpt-6.1-sol và grok-4.7, thay vì gpt-5.5 và grok-4.6). Runtime Gemini chạy xong trong khoảng 30 giây.
**Bài học:** Máy chủ có IP cố định dễ bị chặn tìm kiếm; agent SEO nên dùng API, không cào trang Google.
**Artefact:** Bảng 5 issue: agent, kết quả, trạng thái cuối.
