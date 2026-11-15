---
id: 2026-11-03-installer-windows-sao-chep-tu-du
date: 2026-11-03
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:ab9a1dd8#L1300", "claude:ab9a1dd8#L1303", "claude:ab9a1dd8#L1336", "claude:ab9a1dd8#L1339", "claude:ab9a1dd8#L1346", "claude:ab9a1dd8#L1359"]
hook: "Installer Windows lấy từ dự án khác, vẫn phải đọc và sửa"
tension: none
sides: []
strength: 0
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Installer Windows sao chép từ dự án khác đã kiểm, nhưng vẫn phải đọc lại và sửa

**Bối cảnh:** Skill đóng gói có một template install.sh đã test. Với bản PowerShell, agent tìm installer của một dự án khác trên máy để làm mẫu.
**Chuyện gì xảy ra:** Một đường dẫn install.ps1 không tồn tại, nhưng bản ở dự án khác thì có. Agent đọc nó và viết install.ps1 dựa trên đó, và cảnh báo rằng PowerShell 5.1 đọc sai UTF-8 khi chạy qua irm và iex nên thông báo chỉ dùng ASCII.
**Bài học:** Mẫu từ dự án khác là điểm khởi đầu tốt, nhưng cần đối chiếu với phiên bản shell đích; chữ có dấu trong script PowerShell 5.1 có thể hỏng.
**Artefact:** Đoạn đầu install.ps1 với thông báo ASCII và chú thích lý do. Không cần che gì.
