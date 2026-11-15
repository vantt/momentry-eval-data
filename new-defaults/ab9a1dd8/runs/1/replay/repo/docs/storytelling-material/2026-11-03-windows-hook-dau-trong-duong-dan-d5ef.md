---
id: 2026-11-03-windows-hook-dau-trong-duong-dan-d5ef
code: M-12NX
aliases: [M-12NX]
date: 2026-11-03
repo: repo
status: raw
signals: [rang_buoc_thiet_ke]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L2830", "claude:ab9a1dd8#L2837", "claude:ab9a1dd8#L2855", "claude:ab9a1dd8#L2868"]
hook: "Đổi dấu \\ thành / để cả cmd và Git Bash chạy hook"
tension: nho_ma_to
sides: ["Chỉ đổi một dấu gạch trong đường dẫn", "Hook chạy được ở cả hai shell, dù chưa đo bằng phiên thật"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Windows hook: dấu / trong đường dẫn để cmd và Git Bash cùng chạy

**Bối cảnh:** Chưa rõ Claude Code và Codex trên Windows chạy hook bằng cmd, PowerShell hay Git Bash.
**Chuyện gì xảy ra:** Theo báo cáo cộng đồng, Claude Code chạy hook qua Git Bash còn Codex qua cmd. Agent đổi đường dẫn trong lệnh hook sang dấu / để chạy được ở cả hai, rồi ghi vào tài liệu rằng chưa đo bằng phiên thật.
**Bài học:** Đường dẫn Windows trong hook nên dùng dấu / và ghi rõ phần chưa kiểm chứng.
**Artefact:** Đoạn lệnh hook trước và sau khi đổi dấu. Che đường dẫn home.
