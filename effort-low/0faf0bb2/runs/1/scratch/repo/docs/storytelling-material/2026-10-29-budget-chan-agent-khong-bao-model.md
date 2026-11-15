---
id: 2026-10-29-budget-chan-agent-khong-bao-model
date: 2026-10-29
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, ràng buộc định hình thiết kế]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L1170", "claude:0faf0bb2#L1174", "claude:0faf0bb2#L1183", "claude:0faf0bb2#L1185", "claude:0faf0bb2#L1204"]
hook: "Đặt ngân sách để kiểm soát chi phí, cả ba agent bị chặn im lặng"
tension: giup_ma_hai
sides: ["đặt ngân sách tháng để kiểm soát chi phí", "mọi lần đánh thức bị 409, agent không chạy được và không báo gì"]
strength: 3
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Budget chặn agent không báo: model gói thuê bao không có giá nên mọi lần đánh thức bị 409

**Bối cảnh:** Sau khi giao SEN-1, comment của board không đánh thức được agent Mai dù không có lỗi rõ ràng.
**Chuyện gì xảy ra:** Lệnh wake trả 409 'recorded usage has no reliable price'. Đặt ngân sách tháng cho agent khiến Paperclip từ chối mọi lần đánh thức vì model gói không có giá để tính chi phí. Đặt budget về 0 cho cả ba agent, resume Mai, run mới chạy và task hoàn thành trong 53 giây.
**Bài học:** Hạn mức chi phí cần có giá cho mọi model; model theo gói cố định không có giá thì hạn mức làm chặn việc âm thầm.
**Artefact:** Chuỗi sự kiện: comment → không có run → lỗi 409 → budget=0 → run succeeded. Che: id agent, id công ty.
