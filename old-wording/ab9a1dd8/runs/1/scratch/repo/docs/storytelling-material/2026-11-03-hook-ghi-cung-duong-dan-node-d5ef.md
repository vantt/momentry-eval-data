---
id: 2026-11-03-hook-ghi-cung-duong-dan-node-d5ef
code: M-8ZGC
aliases: [M-8ZGC]
date: 2026-11-03
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L236", "claude:ab9a1dd8#L1170"]
hook: "Nâng Node một lần, hook chết im lặng mà không ai biết"
tension: nho_ma_to
sides: ["Nâng Node qua nvm hay fnm, việc rất thường", "Hook ghi cứng đường dẫn chết mà lệnh vẫn thoát 0"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: none
spine_context: "Dự án momentry nhặt những chuyện đáng kể từ phiên làm việc với coding agent, và đang chuẩn bị đóng gói để người dùng cài và chạy được."
spine_context_lines: [profile, "claude:ab9a1dd8#L42"]
spine_want: Muốn người mới và agent tự đi từ cài đặt tới lần chạy đầu thành công.
spine_want_lines: ["claude:ab9a1dd8#L42"]
spine_obstacle: "Cấu hình hook ghi cứng đường dẫn Node tuyệt đối. Nâng Node là hook hỏng, mà lệnh hook vẫn thoát 0 nên không ai biết."
spine_obstacle_lines: ["claude:ab9a1dd8#L236"]
spine_action: Đổi hook sang gọi qua lệnh momentry thay vì đường dẫn Node cứng.
spine_action_lines: ["claude:ab9a1dd8#L1170"]
completeness: 4
---

# Hook ghi cứng đường dẫn Node tuyệt đối: nâng Node là hook chết mà không ai biết

**Bối cảnh:** Cấu hình hook in ra cho Claude Code và Codex có đường dẫn node và bin tuyệt đối.
**Chuyện gì xảy ra:** Lệnh hook luôn thoát 0 nên lỗi im lặng. Nâng Node qua nvm hoặc fnm, hoặc chuyển thư mục clone, là hook hỏng và không có doctor nào phát hiện. Sửa bằng cách cài một lệnh momentry vào ~/.local/bin, để hook gọi qua tên lệnh đó nên không còn đường dẫn Node cứng.
**Bài học:** Hook không nên ghi cứng đường dẫn runtime. Cho nó gọi qua một shim ổn định, và có lệnh kiểm tra để báo hook đang trỏ tới đâu.
**Artefact:** Đoạn JSON hook trước và sau khi sửa. Che đường dẫn HOME.
