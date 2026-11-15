---
id: 2026-11-10-khi-user-yeu-cau-mo-mot-fd46
code: M-MHH8
aliases: [M-MHH8]
date: 2026-11-10
repo: repo
status: raw
signals: []
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [outsider]
lines: []
hook: "Trước khi gọi model ngoài tốn tiền, agent liệt kê rồi chờ duyệt"
tension: khac
sides: ["Việc có thể chạy ngay cho nhanh", "Tốn tiền và thời gian nên phải chờ chủ duyệt"]
strength: 1
stakes: 1
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Khi user yêu cầu mở một việc tốn thời gian hoặc tốn tiền (hội đồng nhiều model, probe ngoài), agent kiểm tra điều kiện an toàn và chi phí trước, báo danh sách cho user, rồi chờ duyệt trước khi chạy.

**Chuyện gì xảy ra:** Khi user yêu cầu mở một việc tốn thời gian hoặc tốn tiền (hội đồng nhiều model, probe ngoài), agent kiểm tra điều kiện an toàn và chi phí trước, báo danh sách cho user, rồi chờ duyệt trước khi chạy.
**Góc người ngoài:** cách làm phổ biến là Nhiều người để AI tự chạy luôn các lệnh gọi model ngoài, hoặc không biết có những lệnh đó; ở đây khác ở Agent trình bày bảng 'ghế nào, family nào, trạng thái ra sao' và hỏi lại trước khi mở, kể cả khi user đã đồng ý ý tưởng chung. Người đọc muốn có thói quen dừng để duyệt với các việc có chi phí hoặc tác động ngoài máy.
