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
hook: "Nâng Node một lần, hook chết mà không ai hay"
tension: nho_ma_to
sides: ["Nâng Node qua nvm hoặc fnm, việc nhỏ", "Hook ghi cứng đường dẫn nên chết im lặng, doctor không bắt được"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Hook ghi cứng đường dẫn Node tuyệt đối: nâng Node là hook chết mà không ai biết

**Bối cảnh:** Cấu hình hook in ra cho Claude Code và Codex có đường dẫn node và bin tuyệt đối.
**Chuyện gì xảy ra:** Lệnh hook luôn thoát 0 nên lỗi im lặng. Nâng Node qua nvm hoặc fnm, hoặc chuyển thư mục clone, là hook hỏng và không có doctor nào phát hiện. Sửa bằng cách cài một lệnh momentry vào ~/.local/bin, để hook gọi qua tên lệnh đó nên không còn đường dẫn Node cứng.
**Bài học:** Hook không nên ghi cứng đường dẫn runtime. Cho nó gọi qua một shim ổn định, và có lệnh kiểm tra để báo hook đang trỏ tới đâu.
**Artefact:** Đoạn JSON hook trước và sau khi sửa. Che đường dẫn HOME.
