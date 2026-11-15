---
id: 2026-10-21-kiem-tra-tung-tai-khoan-bang
date: 2026-10-21
repo: repo
status: raw
signals: []
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:9514b261#L1994", "claude:9514b261#L2069", "claude:9514b261#L2212", "claude:9514b261#L2222", "claude:9514b261#L2246", "claude:9514b261#L3305", "claude:9514b261#L3338"]
hook: "Kiểm tài khoản bằng lệnh 'trả lời đúng chữ OK', lưu lại để so sánh"
tension: it_ma_nhieu
sides: ["Chỉ một câu hỏi ngắn 'trả lời đúng một chữ OK'", "Phân loại được ok, quota, auth, trust-prompt và so sánh giữa các lần"]
strength: 1
stakes: 1
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Kiểm tra từng tài khoản bằng một lượt hỏi đọc-chỉ rất ngắn ("trả lời đúng một chữ OK") cùng một bộ kịch bản, chạy nền, phân loại kết quả (ok, quota, auth, trust-prompt). Kết quả cũ được chuyển sang thư mục phụ thay vì xoá, để so sánh giữa các lần.

**Chuyện gì xảy ra:** Kiểm tra từng tài khoản bằng một lượt hỏi đọc-chỉ rất ngắn ("trả lời đúng một chữ OK") cùng một bộ kịch bản, chạy nền, phân loại kết quả (ok, quota, auth, trust-prompt). Kết quả cũ được chuyển sang thư mục phụ thay vì xoá, để so sánh giữa các lần.
**Góc người ngoài:** cách làm phổ biến là Người dùng thường gọi API bằng curl một lần, đọc lỗi rồi xoá file tạm, không giữ kết quả để so sánh; ở đây khác ở Việc kiểm được lặp lại được và so sánh được qua các lần, nên biết chắc tài khoản nào hỏng vì lý do gì, không đoán theo cảm giác.
