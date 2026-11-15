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
hook: "Khoá API dư đúng một ký tự: 25 thay vì 24, và bị 401"
tension: nho_ma_to
sides: ["Chỉ thừa một ký tự khoảng trắng", "Khoá mới bị 401, còn khoá cũ đã bị ghi đè không sao lưu"]
strength: 3
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Forgent (fgOS) là nền tảng xây app agent, đang ở bản alpha, và người làm đang cài nhà cung cấp model TheHive cho hai công cụ dòng lệnh pi và omp. Họ tưởng máy đã có khoá chạy được nên nhập khoá mới chỉ là thay một chuỗi. Hoá ra khoá dán vào thừa một ký tự, API trả 401, và lệnh nhập đã ghi đè khoá cũ không có bản sao. Sau khi sao lưu, bỏ khoảng trắng và gọi thử API, khoá nhận 200 và cả hai công cụ đều chạy. Ai hay dán khóa API vào công cụ nên đọc để biết vì sao phải sao lưu trước khi ghi đè và kiểm bằng lời gọi thật."
audience: dev dùng công cụ dòng lệnh có khoá API và cần đổi khoá an toàn
spine_context: "Forgent (fgOS) là nền tảng xây và chạy app agent, đang ở bản alpha. Người làm cài nhà cung cấp model TheHive cho hai công cụ dòng lệnh pi và omp."
spine_context_lines: [profile, "claude:9514b261#L3609"]
spine_want: "Dùng được TheHive trên cả pi và omp, với khoá API mới."
spine_want_lines: ["claude:9514b261#L3609"]
spine_obstacle: "Khoá vừa nhập bị API trả 401 cả khi gọi thẳng, trong khi khoá cũ 24 ký tự vẫn chạy."
spine_obstacle_lines: ["claude:9514b261#L3915", "claude:9514b261#L3920"]
spine_turn: "Tưởng nhập khoá mới chỉ là thay một chuỗi và máy 'không cần nhập lại'; hoá ra khoá dán có thừa một ký tự (25 thay vì 24), và lệnh đã ghi đè khoá cũ không sao lưu."
spine_turn_lines: ["claude:9514b261#L3864", "claude:9514b261#L3899", "claude:9514b261#L3920"]
spine_action: "Sao lưu file khoá trước, dán lại khoá với bước bỏ khoảng trắng, rồi gọi thử API."
spine_action_lines: ["claude:9514b261#L3920"]
spine_outcome: "API trả 200; pi và omp đều trả OK với cả hai model; khoá 24 ký tự, quyền 600."
spine_outcome_lines: ["claude:9514b261#L3930", "claude:9514b261#L3949"]
spine_takeaway: "Sao lưu thông tin xác thực trước khi ghi đè, bỏ khoảng trắng khi dán khoá, và kiểm bằng một lời gọi API thật trước khi tin."
spine_takeaway_lines: ["claude:9514b261#L3864", "claude:9514b261#L3920"]
completeness: 7
---

# Nhập lại khoá TheHive ghi đè khoá cũ không sao lưu, bị 401, rồi lỗi một ký tự thừa

**Góc kể:** Forgent (fgOS) là nền tảng xây app agent, đang ở bản alpha, và người làm đang cài nhà cung cấp model TheHive cho hai công cụ dòng lệnh pi và omp. Họ tưởng máy đã có khoá chạy được nên nhập khoá mới chỉ là thay một chuỗi. Hoá ra khoá dán vào thừa một ký tự, API trả 401, và lệnh nhập đã ghi đè khoá cũ không có bản sao. Sau khi sao lưu, bỏ khoảng trắng và gọi thử API, khoá nhận 200 và cả hai công cụ đều chạy. Ai hay dán khóa API vào công cụ nên đọc để biết vì sao phải sao lưu trước khi ghi đè và kiểm bằng lời gọi thật.
**Bối cảnh:** Cài nhà cung cấp TheHive cho pi và omp theo hướng dẫn. Máy này đã có một khoá cũ chạy được.
**Chuyện gì xảy ra:** Agent đưa lệnh nhập khoá nhưng không có bước sao lưu auth.json, nên ghi đè khoá cũ đang hoạt động. Khoá mới dài 25 ký tự bị API trả 401 cả khi gọi thẳng, trong khi khoá đúng dài 24 ký tự. Sau khi chủ dán lại có loại khoảng trắng và có sao lưu, API trả 200 và pi, omp đều trả OK. Agent thừa nhận đã nói 'không cần nhập lại' trước khi sao lưu.
**Bài học:** Sao lưu file thông tin xác thực trước khi ghi đè, loại khoảng trắng khi dán khoá, và kiểm bằng một lời gọi API thật trước khi tin.
**Artefact:** Bảng kiểm tra gồm mã HTTP, độ dài khoá và quyền file, không kèm khoá. Không cần ảnh.
**Góc người ngoài:** cách làm phổ biến là Người dùng thường sửa tay file config, không sao lưu hoặc sao lưu không có tên, và chỉ thấy lỗi khi chạy thật; ở đây khác ở Agent sao lưu trước, báo đường dẫn bản sao, và cách hoàn tác (chép đè lại). Vì vậy khi có lỗi như khoá bị ghi đè, user vẫn có đường lùi. Người đọc sẽ thấy đây là thói quen đáng bắt chước, và cũng là bài học từ lần nhập khoá TheHive không có bản sao.
