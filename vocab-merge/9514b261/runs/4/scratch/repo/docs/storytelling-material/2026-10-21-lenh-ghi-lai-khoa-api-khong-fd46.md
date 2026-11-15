---
id: 2026-10-21-lenh-ghi-lai-khoa-api-khong-fd46
code: M-3ASD
aliases: [M-3ASD]
date: 2026-10-21
repo: repo
status: raw
signals: [người duyệt thứ máy soạn, nguyên nhân bất ngờ]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L3864", "claude:9514b261#L3899", "claude:9514b261#L3915", "claude:9514b261#L3920", "claude:9514b261#L3930", "claude:9514b261#L3949"]
hook: "Lệnh ghi khoá không sao lưu làm mất khoá chạy được, khoá mới dư một ký tự"
tension: giup_ma_hai
sides: ["agent đưa lệnh ghi khoá mới, nói không cần nhập lại", "không sao lưu nên mất khoá cũ, khoá mới dư ký tự bị 401"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Lệnh ghi lại khoá API không sao lưu làm mất khoá đang chạy, khoá mới bị 401 vì dư một ký tự cuối

**Bối cảnh:** Người dùng cài nhà cung cấp TheHive cho cả pi và omp theo hướng dẫn. Máy đã có khoá chạy được.
**Chuyện gì xảy ra:** Agent đưa lệnh ghi đè auth.json mà chưa sao lưu, dù trước đó đã nói không cần nhập lại. Khoá mới dài 25 ký tự bị API trả 401 Invalid or expired token, cả khi gọi thẳng. Phân loại ký tự cho thấy ký tự cuối là ký tự đặc biệt, trong khi khoá cũ dài 24 ký tự. Người dùng nhập lại bằng lệnh mới có sao lưu và làm sạch khoảng trắng. API trả 200 và cả bốn lượt pi/omp đều OK.
**Bài học:** Sao lưu trước khi ghi đè thông tin xác thực. Luôn làm sạch khoảng trắng khi dán khoá, và kiểm bằng một lệnh gọi thẳng trước khi tin cấu hình.
**Artefact:** Bảng kiểm bốn lượt pi và omp với hai model, trước và sau sửa. Không in khoá.
