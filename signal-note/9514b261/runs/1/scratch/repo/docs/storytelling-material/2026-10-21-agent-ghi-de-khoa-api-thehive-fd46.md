---
id: 2026-10-21-agent-ghi-de-khoa-api-thehive-fd46
code: M-X0C3
aliases: [M-X0C3]
date: 2026-10-21
repo: repo
status: raw
signals: [khac]
signal_note: "Agent tự nhận lỗi quy trình: một lệnh 'nhập khoá' ghi đè khoá đang chạy được mà không có bản sao lưu."
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L3864", "claude:9514b261#L3920", "claude:9514b261#L3930", "claude:9514b261#L3949"]
hook: "Khoá API mới dài 25 ký tự, khoá cũ 24: dán thừa một ký tự là 401"
tension: nho_ma_to
sides: ["Chỉ một ký tự thừa lúc dán khoá", "API trả 401, agent không sao lưu nên phải nhập lại"]
strength: 3
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: none
spine_context: "Người làm đang xây fgOS, tầng nền để chạy ứng dụng agent, và đang cài provider TheHive cho hai công cụ pi và omp."
spine_context_lines: [profile, "claude:9514b261#L3609"]
spine_want: Cài TheHive cho pi và omp theo hướng dẫn.
spine_want_lines: ["claude:9514b261#L3609"]
spine_obstacle: "API trả 401 với khoá vừa nhập, cho cả pi và omp."
spine_obstacle_lines: ["claude:9514b261#L3920"]
spine_action: "Nhập khoá mới bằng lệnh không sao lưu khoá cũ đang chạy, rồi nhập lại có sao lưu và lọc khoảng trắng."
spine_action_lines: ["claude:9514b261#L3864", "claude:9514b261#L3930"]
spine_outcome: "Khoá 24 ký tự nhận 200, và bốn lượt kiểm pi và omp đều trả OK."
spine_outcome_lines: ["claude:9514b261#L3930", "claude:9514b261#L3949"]
spine_takeaway: "Sao lưu thông tin xác thực đang chạy trước khi ghi đè, và lọc khoảng trắng khi dán khoá."
spine_takeaway_lines: ["claude:9514b261#L3920", "claude:9514b261#L3949"]
completeness: 6
---

# Agent ghi đè khoá API TheHive mà không sao lưu: khoá dán thừa một ký tự, 401, phải nhập lại

**Bối cảnh:** Owner nhờ cài provider TheHive cho pi và omp theo hướng dẫn. Máy đã có sẵn khoá cũ chạy được.
**Chuyện gì xảy ra:** Agent đưa lệnh nhập khoá mà không sao lưu auth.json trước. Owner dán khoá, API trả 401 cho cả pi và omp. Khoá mới dài 25 ký tự trong khi khoá cũ dài 24, nên có ký tự thừa lúc dán. Sau khi owner nhập lại bằng lệnh có sao lưu và tr -d khoảng trắng, API trả 200 và bốn lượt kiểm đều OK.
**Bài học:** Trước khi ghi đè một thông tin xác thực đang chạy, sao lưu nó; và lọc khoảng trắng khi dán khoá, rồi kiểm bằng một lệnh gọi API trước khi tin vào cấu hình.
**Artefact:** Không có khoá. Chỉ dùng: 'API trả 401 với khoá 25 ký tự, 200 với khoá 24 ký tự', kèm đoạn lệnh tr -d (không in khoá).
