---
id: 2026-11-03-installer-muon-tu-du-an-khac
date: 2026-11-03
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:ab9a1dd8#L1336", "claude:ab9a1dd8#L1339", "claude:ab9a1dd8#L1346", "claude:ab9a1dd8#L1349", "claude:ab9a1dd8#L1359"]
hook: "ls báo không có file, nhưng installer chạy được nằm sẵn ở dự án khác"
tension: tuong_ma_hoa_ra
sides: ["ls báo đường dẫn không có file nào", "installer đã chạy thật nằm sẵn ở dự án khác trên máy"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Installer mượn từ dự án khác đã chạy thật

**Bối cảnh:** Cần viết install.ps1 cho Windows. Đường dẫn tham chiếu ban đầu không tồn tại.
**Chuyện gì xảy ra:** Lệnh ls báo không có file ở một đường dẫn, nhưng tìm được installer đã chạy thật ở một dự án khác trên máy. Agent đọc và viết lại theo đó, chỉ dùng ASCII vì PowerShell 5.1 đọc sai UTF-8 khi chạy qua pipe.
**Bài học:** Trước khi viết mới, tìm trong các dự án sẵn có một cách đã chạy thật. Với PowerShell 5.1, giữ thông báo ASCII khi chạy qua irm và iex.
**Artefact:** Không có artefact.
