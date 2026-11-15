---
id: 2026-11-03-hook-bi-bo-qua-im-lang
date: 2026-11-03
repo: repo
status: raw
signals: ["2", "5"]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L236", "claude:ab9a1dd8#L1170", "claude:ab9a1dd8#L1171"]
hook: "Hook hỏng suốt thời gian dài mà vẫn thoát 0, không ai hay"
tension: cam_ma_van_lot
sides: ["hook luôn thoát 0, trông như đang chạy tốt", "đường dẫn cứng đã hỏng sau khi đổi Node, không ai thấy"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Hook bị bỏ qua im lặng: lệnh hook luôn thoát 0 nên lỗi không ai thấy

**Bối cảnh:** momentry ghi hook vào Claude Code và Codex với đường dẫn Node tuyệt đối. Hook được thiết kế không bao giờ chặn phiên.
**Chuyện gì xảy ra:** Khi nâng Node qua nvm hoặc đổi thư mục clone, đường dẫn cứng hỏng, nhưng lệnh hook vẫn thoát 0 nên không có tín hiệu nào. Agent đổi hook sang gọi qua lệnh momentry đã cài, nơi tìm Node lúc chạy.
**Bài học:** Hook không được chặn phiên thì phải có một lệnh kiểm riêng (doctor) để phát hiện hook chết, nếu không lỗi không bao giờ lộ ra.
**Artefact:** Đoạn JSON cấu hình hook trước và sau khi đổi, che đường dẫn người dùng.
