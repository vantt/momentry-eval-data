---
id: 2026-11-03-viet-installer-windows-dua-tren-installer-d5ef
code: M-RXTV
aliases: [M-RXTV]
date: 2026-11-03
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:ab9a1dd8#L1336", "claude:ab9a1dd8#L1339", "claude:ab9a1dd8#L1346", "claude:ab9a1dd8#L1359", "claude:ab9a1dd8#L1364"]
hook: "Thông báo installer chỉ dùng ASCII vì PowerShell đọc sai UTF-8"
tension: nho_ma_to
sides: ["Tiếng có dấu trong thông báo là chuyện nhỏ", "PowerShell 5.1 đọc sai UTF-8 qua irm | iex"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Viết installer Windows dựa trên installer dự án khác; thông báo chỉ ASCII vì PowerShell 5.1 đọc sai UTF-8

**Bối cảnh:** Cần installer PowerShell cho Windows mà không có máy Windows để thử.
**Chuyện gì xảy ra:** Agent tìm được installer PowerShell của một dự án khác đã chạy được và dùng làm mẫu. Thông báo trong file giữ ASCII vì PowerShell 5.1 đọc sai UTF-8 khi chạy qua irm | iex. Trên Linux không có pwsh nên kiểm lại bằng CI windows-2025.
**Bài học:** Tái dùng installer đã chạy được là cách rẻ nhất, nhưng ghi lý do cho từng chỗ lệch khỏi mẫu và kiểm bằng CI thật.
**Artefact:** Không có artefact đáng chụp.
