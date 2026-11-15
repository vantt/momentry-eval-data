---
id: 2026-11-05-5-test-go-loi-chi-tren-c4b4
code: M-9A2K
aliases: [M-9A2K]
date: 2026-11-05
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo, khac]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:6a207191#L2053", "claude:6a207191#L2060", "claude:6a207191#L2073", "claude:6a207191#L2123", "claude:6a207191#L2221", "claude:6a207191#L2246"]
hook: "5 test Go chỉ lỗi trên máy thật, vì HOME giả mà thư mục vẫn thật"
tension: cam_ma_van_lot
sides: ["Test đã đổi HOME sang thư mục tạm, tưởng đã cách ly", "Thư mục làm việc vẫn là HOME thật nên đọc cấu hình thật, CI xanh vẫn không bắt được"]
strength: 3
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án skillstation (viết bằng Go, có hub để đồng bộ skill giữa các máy) đang chuẩn bị commit phần giao diện web, nhưng 5 test Go chỉ đỏ trên máy người làm trong khi CI vẫn xanh. Người làm tưởng test đã cách ly khỏi cấu hình thật vì đổi HOME sang thư mục tạm; hoá ra thư mục làm việc vẫn nằm trong HOME thật, nên công cụ đi ngược lên và đọc nhầm cấu hình Codex, Gemini đang trỏ tới hub. Ai viết test để công cụ tự tìm cấu hình theo đường đi ngược sẽ dễ gặp đúng lỗi này, vì đổi biến môi trường không đủ để cô lập."
audience: dev viết test cho công cụ dòng lệnh có đọc cấu hình người dùng
spine_context: "Dự án skillstation, viết bằng Go, có hub để đồng bộ skill giữa các máy; người làm đang chuẩn bị commit phần giao diện web."
spine_context_lines: ["claude:6a207191#L2052", "claude:6a207191#L2080"]
spine_want: "Muốn make check xanh rồi mới commit, theo quy tắc trong AGENTS.md."
spine_want_lines: ["claude:6a207191#L2052"]
spine_obstacle: "5 test Go đỏ trên máy người làm, nhưng CI trên GitHub vẫn xanh."
spine_obstacle_lines: ["claude:6a207191#L2063", "claude:6a207191#L2246"]
spine_turn: "Tưởng test đã cách ly khỏi máy thật vì đã đổi HOME sang thư mục tạm; hoá ra thư mục làm việc vẫn nằm trong HOME thật, nên status và doctor đi ngược lên và đọc cấu hình Codex, Gemini đang trỏ tới hub."
spine_turn_lines: ["claude:6a207191#L2221"]
spine_action: "Chạy lại test với HOME tạm, truy nguyên nguyên nhân, rồi hỏi người làm có muốn sửa phần cách ly không."
spine_action_lines: ["claude:6a207191#L2129", "claude:6a207191#L2221"]
spine_outcome: CI trên commit 185b75d xanh; 5 test cục bộ vẫn đỏ và chưa sửa.
spine_outcome_lines: ["claude:6a207191#L2243", "claude:6a207191#L2246"]
spine_takeaway: "Cách ly HOME chưa đủ: phải đổi cả thư mục làm việc, và test không được đi ngược lên tìm cấu hình ở HOME thật."
spine_takeaway_lines: ["claude:6a207191#L2221"]
completeness: 7
---

# 5 test Go lỗi chỉ trên máy chủ vì HOME đổi mà thư mục làm việc vẫn là HOME thật

**Góc kể:** Dự án skillstation (viết bằng Go, có hub để đồng bộ skill giữa các máy) đang chuẩn bị commit phần giao diện web, nhưng 5 test Go chỉ đỏ trên máy người làm trong khi CI vẫn xanh. Người làm tưởng test đã cách ly khỏi cấu hình thật vì đổi HOME sang thư mục tạm; hoá ra thư mục làm việc vẫn nằm trong HOME thật, nên công cụ đi ngược lên và đọc nhầm cấu hình Codex, Gemini đang trỏ tới hub. Ai viết test để công cụ tự tìm cấu hình theo đường đi ngược sẽ dễ gặp đúng lỗi này, vì đổi biến môi trường không đủ để cô lập.
**Bối cảnh:** make check báo 5 test lỗi trên main, trong khi CI trên GitHub xanh.
**Chuyện gì xảy ra:** Test đổi HOME sang thư mục tạm nhưng không đổi thư mục làm việc. Lệnh status và doctor đi ngược lên thư mục cha, gặp ~/.codex/config.toml và ~/.gemini/settings.json đã trỏ tới hub vừa kết nối lúc 14:46. Code coi /home/vantt là một dự án, so sánh binary đăng ký với binary test, thấy khác nhau và báo FAILED. Các test chỉ lỗi trên máy có cấu hình thật, nên 5 lỗi không xuất hiện trên CI.
**Bài học:** Test cách ly HOME không đủ: phải đổi cả thư mục làm việc, và test không được đi ngược lên tìm cấu hình ở HOME thật.
**Artefact:** Bảng 5 test, kỳ vọng và lý do lỗi (không chụp output dài 3,2MB).
**Góc người ngoài:** cách làm phổ biến là Thường dev sẽ đánh dấu 'flaky' hoặc bỏ qua test, hoặc sửa đại vào test cho pass; hiếm khi giải thích được vì sao chỉ máy mình lỗi; ở đây khác ở Kết quả là hiểu được cơ chế (HOME đổi nhưng thư mục làm việc không đổi, nên công cụ đi ngược lên và đọc nhầm cấu hình của người dùng), và biết rằng việc sửa là tách môi trường test chứ không phải sửa logic. Người đọc sẽ muốn biết cách truy nguyên này.
