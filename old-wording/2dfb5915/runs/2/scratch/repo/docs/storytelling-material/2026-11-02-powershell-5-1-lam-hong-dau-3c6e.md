---
id: 2026-11-02-powershell-5-1-lam-hong-dau-3c6e
code: M-A5WY
aliases: [M-A5WY]
date: 2026-11-02
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L1237"]
hook: "Script cài tiếng Việt có dấu bị PowerShell 5.1 làm hỏng"
tension: chon_mot_mat_mot
sides: ["Muốn thông báo cài đặt bằng tiếng Việt có dấu", "PowerShell 5.1 làm hỏng dấu, script phải toàn ASCII tiếng Anh"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# PowerShell 5.1 làm hỏng dấu tiếng Việt khi đọc script qua irm

**Bối cảnh:** Script cài trên Windows được chạy qua irm và iex.
**Chuyện gì xảy ra:** Windows PowerShell 5.1 đọc script tải qua irm làm hỏng dấu tiếng Việt. Agent viết toàn bộ thông báo trong script cài bằng tiếng Anh và chỉ dùng ASCII, còn README vẫn viết tiếng Việt.
**Bài học:** Script cài chạy trên PowerShell cũ cần giữ ASCII, đừng tin vào encoding khi tải qua mạng.
