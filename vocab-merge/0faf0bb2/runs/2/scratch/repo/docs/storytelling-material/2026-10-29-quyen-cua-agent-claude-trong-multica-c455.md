---
id: 2026-10-29-quyen-cua-agent-claude-trong-multica-c455
code: M-12ET
aliases: [M-12ET]
date: 2026-10-29
repo: repo
status: raw
signals: [ràng buộc định hình thiết kế]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L3406", "claude:0faf0bb2#L3412", "claude:0faf0bb2#L3747"]
hook: "Một alias trong shell khiến agent chạy mọi lệnh không cần xin phép"
tension: nho_ma_to
sides: ["Một alias có cờ bỏ kiểm tra quyền", "Agent chạy mọi lệnh với quyền user, không sandbox"]
strength: 3
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Quyền của agent Claude trong Multica: alias luôn bỏ kiểm tra quyền, agent chạy không sandbox

**Bối cảnh:** Trước khi spike Multica với Claude Code, kiểm tra cách Multica gọi Claude.
**Chuyện gì xảy ra:** Shell có alias claude với cờ --dangerously-skip-permissions. Multica gọi claude với bypassPermissions, nên agent chạy mọi lệnh với quyền của user và không có sandbox. Spike vẫn hoạt động, nhưng điểm này phải xử lý trước khi dùng thật.
**Bài học:** Kiểm tra alias và cờ bỏ quyền của CLI trước khi cho agent điều khiển máy.
**Artefact:** Kết quả terminal báo alias. Đã che đường dẫn.
