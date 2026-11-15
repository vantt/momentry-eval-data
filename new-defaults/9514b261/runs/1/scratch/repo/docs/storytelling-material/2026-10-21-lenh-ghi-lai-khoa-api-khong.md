---
id: 2026-10-21-lenh-ghi-lai-khoa-api-khong
date: 2026-10-21
repo: repo
status: raw
signals: [người duyệt thứ máy soạn, nguyên nhân bất ngờ]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L3864", "claude:9514b261#L3899", "claude:9514b261#L3915", "claude:9514b261#L3920", "claude:9514b261#L3930", "claude:9514b261#L3949"]
hook: "Khoá mới dư đúng một ký tự cuối nên API trả 401 dù gọi thẳng"
tension: nho_ma_to
sides: ["Dư một ký tự đặc biệt cuối khoá, 25 thay vì 24", "Cả khoá bị API từ chối 401, và lệnh ghi đè không sao lưu làm mất khoá đang chạy"]
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
