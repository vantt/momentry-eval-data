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
hook: "Chạy thật lần đầu: model ghi gpt-6.1-sol trong khi cấu hình gpt-5.5"
tension: tuong_ma_hoa_ra
sides: ["Cấu hình khai báo gpt-5.5 và grok-4.6", "Thống kê token cho thấy thực tế chạy gpt-6.1-sol và grok-4.7, còn Google và DuckDuckGo chặn máy chủ"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Ba runtime chạy thật lần đầu: model khác cấu hình, Google và DuckDuckGo chặn máy chủ

**Bối cảnh:** Người vận hành yêu cầu kiểm chạy thật. Agent tạo hai agent thử và giao năm issue nhỏ.
**Chuyện gì xảy ra:** Năm issue chạy xong, không lỗi. Model thực tế khác cấu hình: thống kê token ghi gpt-6.1-sol và grok-4.7, trong khi cấu hình là gpt-5.5 và grok-4.6. Google chặn máy chủ với lỗi 429, DuckDuckGo đòi CAPTCHA, chỉ Bing còn dùng được. Agent SEO nên đi qua API thay vì cào trang tìm kiếm.
**Bài học:** Đừng tin model trong cấu hình. Hãy đọc model thật từ thống kê sử dụng, và đo công cụ tìm kiếm trên máy chủ trước khi trông cậy vào nó.
**Artefact:** Bảng năm issue với kết quả và trạng thái.
