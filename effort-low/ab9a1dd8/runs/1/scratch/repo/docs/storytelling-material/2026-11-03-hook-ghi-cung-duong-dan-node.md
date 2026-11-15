---
id: 2026-11-03-hook-ghi-cung-duong-dan-node
date: 2026-11-03
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, ràng buộc định hình thiết kế]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L236", "claude:ab9a1dd8#L1170", "claude:ab9a1dd8#L1409"]
hook: "Nâng Node một lần, hook chết im lặng vì đường dẫn ghi cứng"
tension: nho_ma_to
sides: ["chỉ nâng phiên bản Node qua nvm", "hook hỏng im lặng, không ai biết"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Hook ghi cứng đường dẫn Node tuyệt đối: nâng Node là hook chết mà không ai biết

**Bối cảnh:** Lệnh hook luôn thoát 0 và không in gì, nên khi đường dẫn Node không còn tồn tại thì không có tín hiệu nào báo lỗi.
**Chuyện gì xảy ra:** Cấu hình hook in ra đường dẫn node và bin tuyệt đối. Khi nâng Node qua nvm hoặc chuyển thư mục clone, hook hỏng im lặng. Đổi sang gọi qua lệnh momentry đã cài, qua shim, nên đường dẫn Node không còn bị ghi cứng.
**Bài học:** Hook không được ghi đường dẫn runtime cứng; cho nó gọi qua một lệnh ổn định do installer quản lý, và có lệnh doctor kiểm hook còn sống.
**Artefact:** Hai đoạn cấu hình hook: trước là đường dẫn tuyệt đối, sau là tên lệnh ngắn. Che đường dẫn thư mục người dùng.
