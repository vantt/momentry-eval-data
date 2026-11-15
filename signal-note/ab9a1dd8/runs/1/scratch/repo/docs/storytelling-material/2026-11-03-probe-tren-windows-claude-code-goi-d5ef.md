---
id: 2026-11-03-probe-tren-windows-claude-code-goi-d5ef
code: M-BSF3
aliases: [M-BSF3]
date: 2026-11-03
repo: repo
status: raw
signals: [artefact_nhin_duoc, nguyen_nhan_bat_ngo]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L2830", "claude:ab9a1dd8#L2855", "claude:ab9a1dd8#L2868", "claude:ab9a1dd8#L3052", "claude:ab9a1dd8#L3074", "claude:ab9a1dd8#L3077", "claude:ab9a1dd8#L3082", "claude:ab9a1dd8#L3091"]
hook: "Claude Code gọi được hook trên Windows, Codex thì không"
tension: tuong_ma_hoa_ra
sides: ["Hai công cụ cùng chạy hook như nhau", "Một chạy qua Git Bash, một qua cmd, chỉ dấu gạch xuôi dùng chung"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Probe trên Windows: Claude Code gọi được hook, còn Codex chưa; lệnh hook dùng dấu gạch xuôi

**Bối cảnh:** Issue #1 hỏi: trên Windows thật, Claude Code và Codex có gọi hook của momentry không. Máy làm việc không có Windows.
**Chuyện gì xảy ra:** Agent viết workflow chỉ chạy tay trên runner windows-2025, cài Claude Code và Codex thật, chạy phiên không đăng nhập rồi đọc hook.log. Claude Code có dấu hiệu đã gọi hook. Theo báo cáo cộng đồng, Claude Code chạy hook qua Git Bash còn Codex qua cmd, nên lệnh hook dùng dấu gạch xuôi để chạy được ở cả hai.
**Bài học:** Đo hành vi host bằng phiên thật không cần khoá API: log hook có thể là bằng chứng đủ dù phiên báo lỗi đăng nhập.
**Artefact:** Trích dòng hook.log cho thấy hook đã được gọi (che đường dẫn).
