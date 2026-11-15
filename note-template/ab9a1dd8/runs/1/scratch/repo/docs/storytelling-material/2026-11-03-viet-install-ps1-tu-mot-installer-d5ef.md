---
id: 2026-11-03-viet-install-ps1-tu-mot-installer-d5ef
code: M-PSWM
aliases: [M-PSWM]
date: 2026-11-03
repo: repo
status: raw
signals: [rang_buoc_thiet_ke]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:ab9a1dd8#L1329", "claude:ab9a1dd8#L1336", "claude:ab9a1dd8#L1339", "claude:ab9a1dd8#L1346", "claude:ab9a1dd8#L1359", "claude:ab9a1dd8#L1364"]
hook: "Không có Windows để thử, agent viết install.ps1 từ installer dự án khác"
tension: none
sides: []
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Viết install.ps1 từ một installer đã chạy thật ở dự án khác

**Bối cảnh:** Skill yêu cầu tái dùng bản đã chạy thật trước khi thiết kế lại, và máy không có pwsh hay PowerShell để chạy thử.
**Chuyện gì xảy ra:** Đường dẫn installer của một dự án thứ nhất không tồn tại. Agent tìm được installer PowerShell của một dự án khác và đọc để viết lại. Thông báo chỉ dùng ASCII vì PowerShell 5.1 đọc sai UTF-8 khi chạy qua irm và iex. Không có Windows để chạy thử, nên CI Windows là nơi xác nhận.
**Bài học:** Khi không chạy được runtime đích, chép từ bản đã chạy thật và để CI của đúng nền tảng xác nhận.
