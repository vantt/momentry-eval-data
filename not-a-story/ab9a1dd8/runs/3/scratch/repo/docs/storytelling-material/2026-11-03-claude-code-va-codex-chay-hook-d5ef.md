---
id: 2026-11-03-claude-code-va-codex-chay-hook-d5ef
code: M-C7BT
aliases: [M-C7BT]
date: 2026-11-03
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L2830", "claude:ab9a1dd8#L2837", "claude:ab9a1dd8#L2855", "claude:ab9a1dd8#L2868"]
hook: "Một dấu backslash trong đường dẫn khiến Bash ăn mất hook Windows"
tension: nho_ma_to
sides: ["Chỉ một dấu \\ trong đường dẫn", "Git Bash nuốt mất, hook không chạy; còn chưa kiểm trên phiên thật"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Claude Code và Codex chạy hook Windows qua shell khác nhau: dùng dấu / và gọi bằng tên lệnh

**Bối cảnh:** Trước khi viết hướng dẫn hook trên Windows, agent tìm web về shell mà hai công cụ dùng để chạy hook.
**Chuyện gì xảy ra:** Theo báo cáo cộng đồng, Claude Code chạy hook qua Git Bash, còn Codex qua cmd. Đường dẫn có dấu backslash sẽ bị Bash ăn mất. Lệnh hook đổi sang dấu / trong đường dẫn tới momentry.cmd, và /bip gọi momentry theo tên vì installer đã thêm thư mục shim vào PATH. Tài liệu ghi rõ đây là điều chưa kiểm trên phiên thật.
**Bài học:** Khi không kiểm được trên nền tảng, ghi 'chưa kiểm' vào tài liệu thay vì khẳng định. Chọn cú pháp chạy được ở mọi shell có khả năng.
**Artefact:** Dòng hook trong docs/installation.md trước và sau. Che đường dẫn HOME.
