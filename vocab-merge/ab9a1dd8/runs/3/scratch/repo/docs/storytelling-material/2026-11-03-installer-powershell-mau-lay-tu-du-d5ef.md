---
id: 2026-11-03-installer-powershell-mau-lay-tu-du-d5ef
code: M-4BJV
aliases: [M-4BJV]
date: 2026-11-03
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L1336", "claude:ab9a1dd8#L1346", "claude:ab9a1dd8#L1359"]
hook: "Viết installer Windows chỉ bằng ASCII, vì UTF-8 làm PowerShell 5.1 đọc sai"
tension: nho_ma_to
sides: ["Vài ký tự có dấu trong script", "PowerShell 5.1 đọc sai khi chạy qua irm và iex"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Installer PowerShell mẫu lấy từ dự án cùng nhà

**Bối cảnh:** Cần viết install.ps1 cho Windows nhưng chưa có mẫu trong dự án.
**Chuyện gì xảy ra:** Agent kiểm hai thư mục dự án khác trên máy, một có install.ps1 có thể dùng làm mẫu. Agent đọc mẫu rồi viết lại, chỉ dùng ASCII vì PowerShell 5.1 đọc sai UTF-8 khi chạy qua irm và iex.
**Bài học:** Tái dùng mẫu đã chạy được tốt hơn viết từ đầu, nhưng phải kiểm lại từng dòng cho nền tảng đích.
**Artefact:** Không có.
