---
id: 2026-11-05-nam-test-go-do-chi-tren-c4b4
code: M-CF4C
aliases: [M-CF4C]
date: 2026-11-05
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo, khac]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:6a207191#L2063", "claude:6a207191#L2073", "claude:6a207191#L2103", "claude:6a207191#L2152", "claude:6a207191#L2203", "claude:6a207191#L2221", "claude:6a207191#L2243", "claude:6a207191#L2246"]
hook: "Năm test đỏ chỉ trên máy tôi, vì test đọc nhầm config thật"
tension: nho_ma_to
sides: ["Test đã đổi HOME sang thư mục tạm nên tưởng đã cô lập", "Thư mục làm việc vẫn trỏ ngược lên home thật, đọc file config thật"]
strength: 3
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án skillstation (CLI và hub cho skill) vừa đưa một thay đổi giao diện web lên main, và trên máy dev 5 test Go đỏ dù thay đổi không đụng tới chúng. Người làm tưởng test đã được cô lập vì đổi HOME sang thư mục tạm, nhưng lệnh status và doctor vẫn đi ngược từ thư mục làm việc lên tới home thật và đọc cấu hình Codex, Gemini đang có trên máy. CI trên GitHub vẫn xanh vì máy đó không có các file ấy. Ai viết test đọc cấu hình theo thư mục cha nên cô lập cả thư mục làm việc, không chỉ HOME."
audience: dev viết test cho công cụ CLI có đọc cấu hình trên máy cá nhân
spine_context: Dự án skillstation (CLI và hub cho skill) vừa đưa một thay đổi giao diện web lên main.
spine_context_lines: ["claude:6a207191#L2103"]
spine_want: Muốn đưa commit web lên main và thấy CI xanh.
spine_want_lines: ["claude:6a207191#L2103"]
spine_obstacle: 5 test Go trong internal/delivery/cli đỏ trên máy dev dù commit web không đụng tới chúng.
spine_obstacle_lines: ["claude:6a207191#L2103"]
spine_turn: "Tưởng đổi HOME sang thư mục tạm là đã cô lập test; hoá ra status và doctor vẫn đi ngược từ thư mục làm việc tới home thật và đọc cấu hình Codex, Gemini đã ghi lúc 14:46."
spine_turn_lines: ["claude:6a207191#L2152", "claude:6a207191#L2221"]
spine_action: "Chạy lại test với HOME tạm và vẫn đỏ, rồi truy nguyên nhân trong code và file cấu hình; merge commit web vào main."
spine_action_lines: ["claude:6a207191#L2103", "claude:6a207191#L2151", "claude:6a207191#L2158"]
spine_outcome: CI GitHub cho commit web xanh; 5 test Go vẫn đỏ trên máy dev và chưa được sửa.
spine_outcome_lines: ["claude:6a207191#L2243", "claude:6a207191#L2246"]
spine_takeaway: "Test đi tìm config theo thư mục cha có thể đọc cấu hình thật của người dùng; đổi HOME không đủ, phải cô lập cả thư mục làm việc."
spine_takeaway_lines: ["claude:6a207191#L2221"]
completeness: 7
---

# Năm test Go đỏ chỉ trên máy dev: lỗi vì cấu hình agent thật bị đọc vào test

**Góc kể:** Dự án skillstation (CLI và hub cho skill) vừa đưa một thay đổi giao diện web lên main, và trên máy dev 5 test Go đỏ dù thay đổi không đụng tới chúng. Người làm tưởng test đã được cô lập vì đổi HOME sang thư mục tạm, nhưng lệnh status và doctor vẫn đi ngược từ thư mục làm việc lên tới home thật và đọc cấu hình Codex, Gemini đang có trên máy. CI trên GitHub vẫn xanh vì máy đó không có các file ấy. Ai viết test đọc cấu hình theo thư mục cha nên cô lập cả thư mục làm việc, không chỉ HOME.
**Bối cảnh:** Sau khi merge một thay đổi web, `make check` có 5 test Go lỗi trên máy dev nhưng CI trên GitHub lại xanh.
**Chuyện gì xảy ra:** TestMain đổi HOME sang thư mục tạm nhưng không đổi thư mục làm việc. Lệnh status/doctor đi ngược lên /home/vantt, gặp ~/.codex/config.toml và ~/.gemini/settings.json vừa được ghi lúc 14:46 do connect --global, nên báo 'Connection files FAILED'. Đây không phải lỗi do commit web. CI sạch vì máy CI không có các file đó.
**Bài học:** Test đi tìm config theo thư mục cha có thể đọc cấu hình thật của người dùng; hãy cô lập cả thư mục làm việc, không chỉ HOME.
**Artefact:** Bảng 5 test và nguyên nhân tương ứng; không có nội dung cấu hình thật.
**Góc người ngoài:** cách làm phổ biến là Hầu hết dev sẽ bỏ qua test đỏ trên máy mình hoặc chỉ chạy lại cho qua, không so với máy sạch để tách nguyên nhân; ở đây khác ở Phiên này so kết quả với CI trên GitHub, rồi truy tới đúng file cấu hình thật của agent bị đọc vào test. Người đọc sẽ muốn biết cách chẩn đoán lỗi chỉ xuất hiện trên một máy.
