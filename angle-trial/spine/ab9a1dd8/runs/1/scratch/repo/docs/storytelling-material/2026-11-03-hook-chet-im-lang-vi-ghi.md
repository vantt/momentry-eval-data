---
id: 2026-11-03-hook-chet-im-lang-vi-ghi
date: 2026-11-03
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, ràng buộc định hình thiết kế]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L236", "claude:ab9a1dd8#L1170", "claude:ab9a1dd8#L2230"]
hook: "Nâng Node một lần, hook chết im lặng không báo gì"
tension: nho_ma_to
sides: ["Chỉ nâng phiên bản Node hoặc dời thư mục", "Hook hỏng hoàn toàn mà không có tín hiệu nào"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một công cụ dòng lệnh nhặt chất liệu kể chuyện từ phiên làm việc với coding agent, đang tự đóng gói để người mới cài bằng một lệnh. Cấu hình hook ghi đường dẫn Node tuyệt đối trông có vẻ ổn, nhưng khi rà lại thì thấy nâng Node có thể làm hook chết mà không báo gì, vì lệnh hook luôn thoát 0. Lời giải là để hook gọi qua một lệnh momentry đã cài, và thêm lệnh doctor kiểm hook còn chạy được. Ai viết hook cho công cụ dòng lệnh nên để ý chuyện này."
audience: dev viết hook hoặc công cụ dòng lệnh cho agent
spine_context: "Một công cụ dòng lệnh nhặt chất liệu kể chuyện từ phiên làm việc với coding agent, đang tự đóng gói để người mới cài bằng một lệnh."
spine_context_lines: [profile]
spine_want: Đóng gói để người mới cài bằng một lệnh và đạt thành công đầu tiên nhanh.
spine_want_lines: ["claude:ab9a1dd8#L42"]
spine_obstacle: "Phần phân phối gần như chưa có: init báo lỗi với cờ --yes, và không có lệnh kiểm tra hook."
spine_obstacle_lines: ["claude:ab9a1dd8#L232", "claude:ab9a1dd8#L236"]
spine_turn: "Tưởng cấu hình hook ghi đường dẫn Node tuyệt đối là ổn; rà lại thì thấy nâng Node có thể làm hook chết mà không báo gì, vì lệnh hook luôn thoát 0."
spine_turn_lines: ["claude:ab9a1dd8#L236", "claude:ab9a1dd8#L1170"]
spine_action: "Đổi hook sang gọi qua lệnh momentry đã cài, thay vì đường dẫn Node tuyệt đối."
spine_action_lines: ["claude:ab9a1dd8#L1170"]
spine_outcome: "Hook gọi qua lệnh đã cài nên nâng Node không còn làm hook chết; 232 test qua trên Linux, 43/45 việc xong."
spine_outcome_lines: ["claude:ab9a1dd8#L2230"]
spine_takeaway: "Hook nên gọi qua tên lệnh ổn định, không ghi cứng đường dẫn runtime, và cần một lệnh doctor kiểm hook còn chạy được."
spine_takeaway_lines: ["claude:ab9a1dd8#L236", "claude:ab9a1dd8#L1170"]
completeness: 7
---

# Hook chết im lặng vì ghi cứng đường dẫn Node

**Góc kể:** Một công cụ dòng lệnh nhặt chất liệu kể chuyện từ phiên làm việc với coding agent, đang tự đóng gói để người mới cài bằng một lệnh. Cấu hình hook ghi đường dẫn Node tuyệt đối trông có vẻ ổn, nhưng khi rà lại thì thấy nâng Node có thể làm hook chết mà không báo gì, vì lệnh hook luôn thoát 0. Lời giải là để hook gọi qua một lệnh momentry đã cài, và thêm lệnh doctor kiểm hook còn chạy được. Ai viết hook cho công cụ dòng lệnh nên để ý chuyện này.
**Bối cảnh:** Cấu hình hook in ra đường dẫn Node tuyệt đối. Lệnh `hook` luôn thoát 0 nên lỗi không ai thấy.
**Chuyện gì xảy ra:** Khi nâng Node qua trình quản lý phiên bản hoặc chuyển thư mục clone, hook hỏng mà không có tín hiệu nào. Agent đề xuất lệnh `momentry` cài vào thư mục bin, và hook gọi qua lệnh đó, nên lệnh tự tìm Node lúc chạy.
**Bài học:** Hook cần gọi qua một tên lệnh ổn định, không ghi cứng đường dẫn runtime. Và phải có lệnh doctor kiểm hook còn chạy được.
**Artefact:** Đoạn settings.json trước và sau khi sửa. Che đường dẫn home và tên người dùng.
