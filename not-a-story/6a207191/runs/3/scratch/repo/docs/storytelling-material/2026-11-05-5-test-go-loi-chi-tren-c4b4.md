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
hook: "5 test chỉ đỏ trên máy tôi: nó đọc nhầm cấu hình thật"
tension: cam_ma_van_lot
sides: ["Test đã đổi HOME sang thư mục tạm để cách ly", "thư mục làm việc vẫn là HOME thật nên đọc cấu hình thật, CI không thấy lỗi"]
strength: 3
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một dự án CLI viết bằng Go tên skillstation, có hub để đồng bộ skill, đang chuẩn bị commit phần web. Test đã đổi HOME sang thư mục tạm nên tưởng đã tách khỏi máy thật, nhưng lệnh status và doctor vẫn đi ngược lên thư mục làm việc và đọc cấu hình thật, nên 5 test chỉ lỗi trên máy người làm. CI xanh không chứng minh test đã cách ly, và ai viết test cho CLI đọc cấu hình người dùng đều có thể gặp lỗi tương tự."
audience: dev Go viết test cho CLI đọc cấu hình người dùng
spine_context: "Dự án skillstation là một công cụ dòng lệnh viết bằng Go, có hub để đồng bộ skill. Người làm đang sửa phần web và phải chạy make check trước khi commit."
spine_context_lines: ["claude:6a207191#L2052", "claude:6a207191#L2221"]
spine_want: Muốn make check xanh trước khi commit.
spine_want_lines: ["claude:6a207191#L2052"]
spine_obstacle: "5 test Go lỗi trên máy người làm, còn CI trên GitHub vẫn xanh."
spine_obstacle_lines: ["claude:6a207191#L2063", "claude:6a207191#L2221"]
spine_turn: "Tưởng việc đổi HOME sang thư mục tạm đã cách ly test khỏi máy thật; hoá ra lệnh status và doctor vẫn đi ngược từ thư mục làm việc lên và đọc cấu hình Codex, Gemini thật."
spine_turn_lines: ["claude:6a207191#L2221"]
spine_action: "Tìm nguyên nhân, lập bảng 5 test và kỳ vọng của từng test; chưa sửa, hỏi người làm có muốn cách ly test không."
spine_action_lines: ["claude:6a207191#L2215", "claude:6a207191#L2221"]
spine_outcome: CI trên GitHub cho commit web đã qua hết; 5 test chỉ lỗi trên máy có cấu hình thật.
spine_outcome_lines: ["claude:6a207191#L2243", "claude:6a207191#L2246"]
spine_takeaway: "Test cách ly HOME chưa đủ: phải đổi cả thư mục làm việc và không để test đi ngược lên tìm cấu hình ở HOME thật."
spine_takeaway_lines: ["claude:6a207191#L2221"]
completeness: 7
---

# 5 test Go lỗi chỉ trên máy chủ vì HOME đổi mà thư mục làm việc vẫn là HOME thật

**Góc kể:** Một dự án CLI viết bằng Go tên skillstation, có hub để đồng bộ skill, đang chuẩn bị commit phần web. Test đã đổi HOME sang thư mục tạm nên tưởng đã tách khỏi máy thật, nhưng lệnh status và doctor vẫn đi ngược lên thư mục làm việc và đọc cấu hình thật, nên 5 test chỉ lỗi trên máy người làm. CI xanh không chứng minh test đã cách ly, và ai viết test cho CLI đọc cấu hình người dùng đều có thể gặp lỗi tương tự.
**Bối cảnh:** make check báo 5 test lỗi trên main, trong khi CI trên GitHub xanh.
**Chuyện gì xảy ra:** Test đổi HOME sang thư mục tạm nhưng không đổi thư mục làm việc. Lệnh status và doctor đi ngược lên thư mục cha, gặp ~/.codex/config.toml và ~/.gemini/settings.json đã trỏ tới hub vừa kết nối lúc 14:46. Code coi /home/vantt là một dự án, so sánh binary đăng ký với binary test, thấy khác nhau và báo FAILED. Các test chỉ lỗi trên máy có cấu hình thật, nên 5 lỗi không xuất hiện trên CI.
**Bài học:** Test cách ly HOME không đủ: phải đổi cả thư mục làm việc, và test không được đi ngược lên tìm cấu hình ở HOME thật.
**Artefact:** Bảng 5 test, kỳ vọng và lý do lỗi (không chụp output dài 3,2MB).
**Góc người ngoài:** cách làm phổ biến là Thường dev sẽ đánh dấu 'flaky' hoặc bỏ qua test, hoặc sửa đại vào test cho pass; hiếm khi giải thích được vì sao chỉ máy mình lỗi; ở đây khác ở Kết quả là hiểu được cơ chế (HOME đổi nhưng thư mục làm việc không đổi, nên công cụ đi ngược lên và đọc nhầm cấu hình của người dùng), và biết rằng việc sửa là tách môi trường test chứ không phải sửa logic. Người đọc sẽ muốn biết cách truy nguyên này.
