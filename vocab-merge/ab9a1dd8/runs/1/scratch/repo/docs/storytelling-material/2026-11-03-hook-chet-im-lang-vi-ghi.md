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
---

# Hook chết im lặng vì ghi cứng đường dẫn Node

**Bối cảnh:** Cấu hình hook in ra đường dẫn Node tuyệt đối. Lệnh `hook` luôn thoát 0 nên lỗi không ai thấy.
**Chuyện gì xảy ra:** Khi nâng Node qua trình quản lý phiên bản hoặc chuyển thư mục clone, hook hỏng mà không có tín hiệu nào. Agent đề xuất lệnh `momentry` cài vào thư mục bin, và hook gọi qua lệnh đó, nên lệnh tự tìm Node lúc chạy.
**Bài học:** Hook cần gọi qua một tên lệnh ổn định, không ghi cứng đường dẫn runtime. Và phải có lệnh doctor kiểm hook còn chạy được.
**Artefact:** Đoạn settings.json trước và sau khi sửa. Che đường dẫn home và tên người dùng.
