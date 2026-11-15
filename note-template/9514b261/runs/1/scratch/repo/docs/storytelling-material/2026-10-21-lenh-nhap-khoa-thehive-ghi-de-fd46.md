---
id: 2026-10-21-lenh-nhap-khoa-thehive-ghi-de-fd46
code: M-MHGP
aliases: [M-MHGP]
date: 2026-10-21
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [hotspot, harvest, outsider]
lines: ["claude:9514b261#L3864", "claude:9514b261#L3874", "claude:9514b261#L3879", "claude:9514b261#L3906", "claude:9514b261#L3915", "claude:9514b261#L3920", "claude:9514b261#L3930", "claude:9514b261#L3949"]
hook: "Khoá cũ 24 ký tự bị ghi đè bởi khoá mới 25 ký tự lỗi"
tension: giup_ma_hai
sides: ["Đưa lệnh nhập khoá mới cho nhanh", "Không sao lưu nên mất khoá cũ đang chạy, khoá mới thừa một ký tự cho 401"]
strength: 3
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Forgent là nền tảng dựng ứng dụng agent, đang ở alpha, và chủ dự án đang cài TheHive cho hai công cụ dòng lệnh pi và omp. Agent đưa lệnh ghi khoá vào file mà không sao lưu, vì tưởng khoá dán vào là đúng và ghi đè là an toàn. Khoá dán hoá ra dài hơn khoá cũ một ký tự, API từ chối với 401, và khoá đang chạy đã bị ghi đè mất. Người dựng công cụ với khoá API nên biết: sao lưu trước, cắt khoảng trắng khi dán, và gọi thử API một lần trước khi tin."
audience: dev dùng công cụ AI dòng lệnh và lưu khoá API trên máy
spine_context: "Forgent là nền tảng dựng ứng dụng agent, đang ở alpha; chủ dự án đang cài nhà cung cấp mô hình TheHive cho hai công cụ dòng lệnh pi và omp."
spine_context_lines: [profile, "claude:9514b261#L3609"]
spine_want: Muốn TheHive chạy được trên cả pi và omp theo hướng dẫn.
spine_want_lines: ["claude:9514b261#L3609"]
spine_obstacle: "Khoá mới bị API TheHive trả 401 \"Invalid or expired token\", kể cả khi gọi thẳng."
spine_obstacle_lines: ["claude:9514b261#L3915"]
spine_turn: "Agent tưởng khoá dán vào là đúng và ghi đè là an toàn; hoá ra khoá dán dài 25 ký tự trong khi khoá cũ dài 24, và khoá đang chạy đã mất vì không có bản sao."
spine_turn_lines: ["claude:9514b261#L3864", "claude:9514b261#L3888", "claude:9514b261#L3920"]
spine_action: "Agent đưa lệnh ghi khoá không sao lưu; khi lỗi, đề xuất nhập lại bằng lệnh có sao lưu và cắt khoảng trắng."
spine_action_lines: ["claude:9514b261#L3864", "claude:9514b261#L3920"]
spine_outcome: "API trả 200; khoá mới dài 24 ký tự khớp khoá cũ, và cả bốn lượt kiểm pi và omp với deepseek lẫn glm đều OK."
spine_outcome_lines: ["claude:9514b261#L3930", "claude:9514b261#L3944", "claude:9514b261#L3949"]
spine_takeaway: "Sao lưu thông tin xác thực trước khi ghi đè, cắt khoảng trắng khi dán, và gọi thử API một lần trước khi tin."
spine_takeaway_lines: ["claude:9514b261#L3920", "claude:9514b261#L3949"]
completeness: 7
---

# Lệnh nhập khoá TheHive ghi đè khoá đang chạy không sao lưu, khoá dán thừa một ký tự cho 401

**Góc kể:** Forgent là nền tảng dựng ứng dụng agent, đang ở alpha, và chủ dự án đang cài TheHive cho hai công cụ dòng lệnh pi và omp. Agent đưa lệnh ghi khoá vào file mà không sao lưu, vì tưởng khoá dán vào là đúng và ghi đè là an toàn. Khoá dán hoá ra dài hơn khoá cũ một ký tự, API từ chối với 401, và khoá đang chạy đã bị ghi đè mất. Người dựng công cụ với khoá API nên biết: sao lưu trước, cắt khoảng trắng khi dán, và gọi thử API một lần trước khi tin.
**Bối cảnh:** Chủ dự án cài TheHive cho pi và omp theo hướng dẫn. Máy đã có khoá chạy được từ trước.
**Chuyện gì xảy ra:** Agent đưa lệnh ghi khoá mới nhưng không sao lưu auth.json trước, nên khoá cũ đang chạy bị ghi đè. Khoá mới dài 25 ký tự bị API trả 401 Invalid or expired token, còn khoá cũ dài 24. Agent đã đoán khoá dán thừa một ký tự và tự nhận lỗi vì không đưa lệnh có sao lưu. Sau khi chủ dự án nhập lại với sao lưu và loại khoảng trắng, API trả 200 và pi, omp cho cả deepseek lẫn glm đều OK.
**Bài học:** Luôn sao lưu thông tin xác thực trước khi ghi đè, loại khoảng trắng khi dán khoá, và kiểm bằng một lượt gọi API trước khi tin.
**Artefact:** Đoạn lệnh có sao lưu và curl kiểm tra, với khoá thay bằng placeholder, không in giá trị khoá.
**Góc người ngoài:** cách làm phổ biến là Sửa thẳng file, hoặc chỉ dựa vào git để hoàn tác. Với file không nằm trong git (config home, zshrc) thì thường không có bản sao nào; ở đây khác ở Phiên có sao lưu config và zshrc, nhưng riêng lần nhập khoá TheHive lại ghi đè không sao lưu, nên đoạn này rút ra bài học ngược. Người đọc sẽ muốn biết cách sao lưu chuẩn trước khi sửa file ngoài git.
