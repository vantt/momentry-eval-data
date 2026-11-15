---
id: 2026-10-21-nhap-lai-khoa-thehive-ghi-de-fd46
code: M-TGC6
aliases: [M-TGC6]
date: 2026-10-21
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:9514b261#L3864", "claude:9514b261#L3915", "claude:9514b261#L3920", "claude:9514b261#L3930", "claude:9514b261#L3949", "claude:9514b261#L3962"]
hook: "Lỗi một ký tự thừa: khoá dài 25 thay vì 24 bị 401"
tension: nho_ma_to
sides: ["Một ký tự thừa, khoảng trắng nhìn không thấy", "API trả 401 cả khi gọi thẳng, sau khi ghi đè khoá cũ chưa sao lưu"]
strength: 3
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Nhập lại khoá TheHive ghi đè khoá cũ không sao lưu, bị 401, rồi lỗi một ký tự thừa

**Bối cảnh:** Cài nhà cung cấp TheHive cho pi và omp theo hướng dẫn. Máy này đã có một khoá cũ chạy được.
**Chuyện gì xảy ra:** Agent đưa lệnh nhập khoá nhưng không có bước sao lưu auth.json, nên ghi đè khoá cũ đang hoạt động. Khoá mới dài 25 ký tự bị API trả 401 cả khi gọi thẳng, trong khi khoá đúng dài 24 ký tự. Sau khi chủ dán lại có loại khoảng trắng và có sao lưu, API trả 200 và pi, omp đều trả OK. Agent thừa nhận đã nói 'không cần nhập lại' trước khi sao lưu.
**Bài học:** Sao lưu file thông tin xác thực trước khi ghi đè, loại khoảng trắng khi dán khoá, và kiểm bằng một lời gọi API thật trước khi tin.
**Artefact:** Bảng kiểm tra gồm mã HTTP, độ dài khoá và quyền file, không kèm khoá. Không cần ảnh.
**Góc người ngoài:** cách làm phổ biến là Người dùng thường sửa tay file config, không sao lưu hoặc sao lưu không có tên, và chỉ thấy lỗi khi chạy thật; ở đây khác ở Agent sao lưu trước, báo đường dẫn bản sao, và cách hoàn tác (chép đè lại). Vì vậy khi có lỗi như khoá bị ghi đè, user vẫn có đường lùi. Người đọc sẽ thấy đây là thói quen đáng bắt chước, và cũng là bài học từ lần nhập khoá TheHive không có bản sao.
