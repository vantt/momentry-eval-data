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
angle: "Một công cụ dòng lệnh đọc transcript phiên làm việc với coding agent để nhặt chất liệu build-in-public, và đang làm bản cài đặt một lệnh cho người mới. Cấu hình hook ghi cứng đường dẫn Node tuyệt đối tưởng là ổn, nhưng nâng Node hoặc chuyển thư mục là hook chết mà lệnh hook vẫn thoát 0, không ai biết. Ai viết hook hay tích hợp agent nên nhớ: gọi qua một tên lệnh ổn định và có lệnh kiểm hook còn chạy được."
audience: dev viết hook hoặc tích hợp coding agent
spine_context: "Một công cụ dòng lệnh đọc transcript phiên làm việc với coding agent để nhặt chất liệu build-in-public, và đang làm bản cài đặt một lệnh cho người mới."
spine_context_lines: [profile]
spine_want: Người mới đi từ con số 0 tới lần chạy đầu thành công mà không cần hỏi lại.
spine_want_lines: ["claude:ab9a1dd8#L236"]
spine_obstacle: "Hook ghi cứng đường dẫn Node tuyệt đối, nên nâng Node hoặc chuyển thư mục clone là hook hỏng."
spine_obstacle_lines: ["claude:ab9a1dd8#L236"]
spine_turn: Tưởng hook ghi đường dẫn Node là ổn; hoá ra nâng Node là hook chết mà lệnh hook vẫn thoát 0.
spine_turn_lines: ["claude:ab9a1dd8#L236"]
spine_action: "Cho hook gọi qua lệnh momentry đã cài sẵn, không ghi cứng đường dẫn runtime."
spine_action_lines: ["claude:ab9a1dd8#L2230"]
spine_outcome: Hook không còn chết khi nâng Node; 232 test qua trên Linux.
spine_outcome_lines: ["claude:ab9a1dd8#L2230"]
spine_takeaway: "Hook cần gọi qua một tên lệnh ổn định, và cần một lệnh doctor kiểm hook còn chạy được."
spine_takeaway_lines: ["claude:ab9a1dd8#L236", "claude:ab9a1dd8#L256"]
completeness: 7
---

# Hook chết im lặng vì ghi cứng đường dẫn Node

**Góc kể:** Một công cụ dòng lệnh đọc transcript phiên làm việc với coding agent để nhặt chất liệu build-in-public, và đang làm bản cài đặt một lệnh cho người mới. Cấu hình hook ghi cứng đường dẫn Node tuyệt đối tưởng là ổn, nhưng nâng Node hoặc chuyển thư mục là hook chết mà lệnh hook vẫn thoát 0, không ai biết. Ai viết hook hay tích hợp agent nên nhớ: gọi qua một tên lệnh ổn định và có lệnh kiểm hook còn chạy được.
**Bối cảnh:** Cấu hình hook in ra đường dẫn Node tuyệt đối. Lệnh `hook` luôn thoát 0 nên lỗi không ai thấy.
**Chuyện gì xảy ra:** Khi nâng Node qua trình quản lý phiên bản hoặc chuyển thư mục clone, hook hỏng mà không có tín hiệu nào. Agent đề xuất lệnh `momentry` cài vào thư mục bin, và hook gọi qua lệnh đó, nên lệnh tự tìm Node lúc chạy.
**Bài học:** Hook cần gọi qua một tên lệnh ổn định, không ghi cứng đường dẫn runtime. Và phải có lệnh doctor kiểm hook còn chạy được.
**Artefact:** Đoạn settings.json trước và sau khi sửa. Che đường dẫn home và tên người dùng.
