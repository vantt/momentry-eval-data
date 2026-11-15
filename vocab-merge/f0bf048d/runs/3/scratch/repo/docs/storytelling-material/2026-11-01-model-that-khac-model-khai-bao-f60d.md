---
id: 2026-11-01-model-that-khac-model-khai-bao-f60d
code: M-QTDM
aliases: [M-QTDM]
date: 2026-11-01
repo: repo
status: raw
signals: [nguyên nhân bất ngờ]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L3139", "claude:f0bf048d#L3165"]
hook: "Cấu hình ghi gpt-5.5, thống kê token lại ghi gpt-6.1-sol"
tension: tuong_ma_hoa_ra
sides: ["Cấu hình khai báo một model", "Token thực tế chạy model khác"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Model thật khác model khai báo: thống kê token cho thấy model khác cấu hình

**Bối cảnh:** Hai agent thử chạy trên runtime Pi, cấu hình ghi sẵn model mặc định.
**Chuyện gì xảy ra:** Thống kê token ghi nhận model gpt-6.1-sol và grok-4.7, còn cấu hình ghi gpt-5.5 và grok-4.6. Có thể do lúc đăng nhập đã chọn model khác, hoặc agent tự chọn. Runtime Gemini qua omp dùng đúng model đã khai báo.
**Bài học:** Đối chiếu model thực tế trong thống kê usage với cấu hình, đừng tin tên model ghi trong cấu hình.
**Artefact:** Bảng usage theo ngày, provider và model (che số token chi tiết).
