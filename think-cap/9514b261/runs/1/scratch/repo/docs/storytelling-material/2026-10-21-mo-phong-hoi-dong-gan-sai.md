---
id: 2026-10-21-mo-phong-hoi-dong-gan-sai
date: 2026-10-21
repo: repo
status: raw
signals: [đảo quyết định, nguyên nhân bất ngờ]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:9514b261#L1901", "claude:9514b261#L1906", "claude:9514b261#L2600", "claude:9514b261#L2612", "claude:9514b261#L2623", "claude:9514b261#L2630"]
hook: "Mô phỏng thiếu herdr xếp sai ghế, agent phải đính chính ba điều"
tension: giup_ma_hai
sides: ["Chạy mô phỏng để biết trước ghế sẽ gán thế nào", "Thiếu một biến môi trường nên kết quả sai so với phiên thật"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Mô phỏng hội đồng gán sai ghế vì không bật môi trường có herdr

**Bối cảnh:** Trước khi mở hội đồng kiến trúc, agent mô phỏng gán ghế để biết family và model nào sẽ tham gia, dựa trên cấu hình.
**Chuyện gì xảy ra:** Bộ mô phỏng chạy không có herdr nên chọn invocation khác với phiên thật. Lệnh explain (có herdr) cho kết quả khác, và các capability mức critical dùng tầng frontier chứ không bị giới hạn ở flagship như agent đã nói. Agent phải đính chính ba điều đã nói trước và đưa bảng ghế mới.
**Bài học:** Mô phỏng phải chạy đúng điều kiện môi trường như lúc thật, và ưu tiên lệnh explain của chính hệ thống hơn suy luận từ cấu hình.
**Artefact:** Bảng ghế hai cột: trước (mô phỏng không có herdr) và sau (explain có herdr), chỉ ghi family và tầng.
**Góc người ngoài:** cách làm phổ biến là Hầu hết người dùng chạy thẳng workflow tốn tiền và đợi xem có lỗi không; ở đây khác ở Mô phỏng cho thấy ghế nào không có ứng viên trước khi tốn lượt gọi. Probe ngắn tách lỗi tài khoản khỏi lỗi workflow. Người đọc muốn biết cách làm này để tránh chạy hỏng giữa chừng.
