---
id: 2026-11-05-5-test-go-chi-loi-tren-c4b4
code: M-S8E9
aliases: [M-S8E9]
date: 2026-11-05
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo, khac]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:6a207191#L2060", "claude:6a207191#L2074", "claude:6a207191#L2113", "claude:6a207191#L2135", "claude:6a207191#L2158", "claude:6a207191#L2232", "claude:6a207191#L2243", "claude:6a207191#L2246"]
hook: "5 test lỗi trên máy dev, 0 lỗi trên CI"
tension: nho_ma_to
sides: ["CI xanh nên tưởng test sạch", "Test lén đọc cấu hình agent thật của chủ máy"]
strength: 3
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Skillstation là công cụ chia sẻ skill giữa các máy qua một hub, và người làm đang chuẩn bị đẩy thêm một tính năng. Trên máy dev, 5 test Go lỗi trong khi CI xanh; người làm tưởng test đã được cô lập khỏi máy thật vì TestMain đổi HOME, nhưng hoá ra lệnh status và doctor đi ngược thư mục tới nhà thật và đọc cấu hình agent đang trỏ tới hub. Ai viết test đọc cấu hình ngược thư mục đều có thể dính: đổi HOME chưa đủ, phải cô lập cả thư mục làm việc."
audience: dev viết test cho công cụ CLI đọc cấu hình trong thư mục nhà
spine_context: "Một người làm công cụ skillstation (CLI và hub để chia sẻ skill giữa các máy), đang đẩy thêm thông báo bản cập nhật chờ duyệt."
spine_context_lines: ["claude:6a207191#L2103"]
spine_want: Muốn make check chạy xanh trên máy dev.
spine_want_lines: ["claude:6a207191#L2053"]
spine_obstacle: "5 test Go lỗi trên main, trên máy dev."
spine_obstacle_lines: ["claude:6a207191#L2063"]
spine_turn: "Tưởng test đã cô lập khỏi máy thật vì TestMain đổi HOME; hoá ra status và doctor vẫn đi ngược thư mục làm việc tới thư mục nhà thật, và đọc cấu hình Codex, Gemini trỏ tới hub."
spine_turn_lines: ["claude:6a207191#L2168", "claude:6a207191#L2221"]
spine_action: "Chạy lại test với HOME tạm: vẫn lỗi. Đọc cơ chế và đối chiếu từng test."
spine_action_lines: ["claude:6a207191#L2151", "claude:6a207191#L2152", "claude:6a207191#L2221"]
spine_outcome: Chưa sửa test. CI trên GitHub cho commit 185b75d đã qua hết; 5 test chỉ lỗi trên máy dev.
spine_outcome_lines: ["claude:6a207191#L2243", "claude:6a207191#L2246"]
spine_takeaway: "Test tìm cấu hình ngược thư mục phải cách ly cả thư mục làm việc, không chỉ biến môi trường."
spine_takeaway_lines: ["claude:6a207191#L2221"]
completeness: 7
---

# 5 test Go chỉ lỗi trên máy dev: test đọc cấu hình agent thật của chủ máy

**Góc kể:** Skillstation là công cụ chia sẻ skill giữa các máy qua một hub, và người làm đang chuẩn bị đẩy thêm một tính năng. Trên máy dev, 5 test Go lỗi trong khi CI xanh; người làm tưởng test đã được cô lập khỏi máy thật vì TestMain đổi HOME, nhưng hoá ra lệnh status và doctor đi ngược thư mục tới nhà thật và đọc cấu hình agent đang trỏ tới hub. Ai viết test đọc cấu hình ngược thư mục đều có thể dính: đổi HOME chưa đủ, phải cô lập cả thư mục làm việc.
**Bối cảnh:** make check có 5 test lỗi trên main, và lỗi cả trước khi có commit của agent.
**Chuyện gì xảy ra:** TestMain đổi HOME nhưng không đổi thư mục làm việc. Lệnh status và doctor đi ngược lên thư mục cha đến home thật, gặp cấu hình Codex và Gemini trỏ tới hub, rồi coi đó là một project. Kết quả là 5 test thoát mã 1 hoặc sai thông báo. Trên CI, cả 5 test đều qua vì máy đó không có cấu hình này: 5 lỗi trên máy dev, 0 lỗi trên CI.
**Bài học:** Test của công cụ đi tìm cấu hình ngược thư mục phải cô lập cả thư mục làm việc, không chỉ biến môi trường.
**Artefact:** Bảng 5 test và lý do từng test lỗi. Cần che đường dẫn.
