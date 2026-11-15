---
id: 2026-11-03-hook-tren-windows-mot-duong-dan-d5ef
code: M-2X9T
aliases: [M-2X9T]
date: 2026-11-03
repo: repo
status: raw
signals: [rang_buoc_thiet_ke]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:ab9a1dd8#L2837", "claude:ab9a1dd8#L2855", "claude:ab9a1dd8#L2868", "claude:ab9a1dd8#L2888"]
hook: "Một dấu gạch chéo đủ cho hook chạy ở cả Git Bash lẫn cmd"
tension: it_ma_nhieu
sides: ["Hai shell Windows hiểu đường dẫn khác nhau", "Một kiểu dấu gạch chéo chạy được cả hai"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Hook trên Windows: một đường dẫn chạy được cả Git Bash lẫn cmd

**Bối cảnh:** Claude Code và Codex trên Windows chạy lệnh hook qua hai shell khác nhau.
**Chuyện gì xảy ra:** Theo báo cáo cộng đồng, Claude Code chạy hook qua Git Bash còn Codex chạy qua cmd. Agent đổi lệnh hook sang dấu gạch chéo trong đường dẫn momentry.cmd để chạy được cả hai, và /bip gọi momentry theo tên vì installer đưa thư mục shim vào PATH. Tài liệu ghi rõ phần nào chưa kiểm.
**Bài học:** Trên Windows, cùng một lệnh hook có thể đi qua hai shell; viết đường dẫn bằng dấu gạch chéo và gọi bằng tên thay vì đường dẫn tuyệt đối.
**Artefact:** Ví dụ dòng lệnh hook trong cấu hình, đã che tên người dùng.
**Góc người ngoài:** cách làm phổ biến là Hook ghi đường dẫn tuyệt đối tới `node` và script, nên hỏng khi đổi phiên bản Node hoặc chuyển thư mục; ở đây khác ở Đường dẫn ổn định qua các lần nâng cấp là điều dev muốn có nhưng hiếm ai làm. Người đọc sẽ hỏi cách làm cho hook không chết khi đổi môi trường.
