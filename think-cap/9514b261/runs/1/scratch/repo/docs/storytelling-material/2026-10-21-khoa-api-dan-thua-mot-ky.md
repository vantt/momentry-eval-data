---
id: 2026-10-21-khoa-api-dan-thua-mot-ky
date: 2026-10-21
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, người duyệt thứ máy soạn]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L3864", "claude:9514b261#L3899", "claude:9514b261#L3915", "claude:9514b261#L3920", "claude:9514b261#L3930", "claude:9514b261#L3949"]
hook: "Dán khoá API thừa đúng 1 ký tự: 25 thay vì 24, và khoá cũ mất"
tension: nho_ma_to
sides: ["Một ký tự thừa khi dán", "API trả 401 và lệnh ghi đè xoá khoá đang chạy, không sao lưu"]
strength: 3
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Khoá API dán thừa một ký tự cho 401, và lệnh ghi đè không sao lưu đã xoá khoá đang chạy

**Bối cảnh:** Người dùng nhập khoá API cho một nhà cung cấp theo hướng dẫn cài đặt. Máy đã có sẵn khoá cũ đang chạy được cho cả hai CLI.
**Chuyện gì xảy ra:** Lệnh agent đưa ra ghi đè khoá cũ mà không sao lưu. Khoá mới dài 25 ký tự, bị API từ chối 401. Khoá đúng dài 24 ký tự, lỗi là một ký tự thừa khi dán. Sau khi người dùng nhập lại với lọc khoảng trắng và kiểm bằng curl trả 200, cả pi và omp đều trả OK.
**Bài học:** Sao lưu trước khi ghi đè khoá, lọc khoảng trắng khi dán, và kiểm bằng một lệnh gọi API trước khi báo xong.
**Artefact:** Bảng kiểm không lộ khoá: độ dài, loại ký tự (chữ, số, ký tự đặc biệt) và kết quả từng lệnh gọi.
