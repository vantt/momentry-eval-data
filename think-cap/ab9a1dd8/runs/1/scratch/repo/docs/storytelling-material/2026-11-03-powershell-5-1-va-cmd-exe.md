---
id: 2026-11-03-powershell-5-1-va-cmd-exe
date: 2026-11-03
repo: repo
status: raw
signals: ["2", "5"]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L2026", "claude:ab9a1dd8#L2049", "claude:ab9a1dd8#L2674"]
hook: "Uninstall báo thành công, nhưng không xoá gì vì nháy kép bị escape sai"
tension: tuong_ma_hoa_ra
sides: ["uninstall báo thành công", "del thất bại âm thầm, file vẫn còn"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# PowerShell 5.1 và cmd.exe: escape nháy làm uninstall không xoá gì nhưng vẫn báo thành công

**Bối cảnh:** Installer Windows cài bằng PowerShell 5.1, gọi node -p và lập lịch xoá bằng cmd.exe khi file shim đang chạy.
**Chuyện gì xảy ra:** Node escape nháy kép thành \" mà cmd không hiểu, nên lệnh del thất bại âm thầm và file vẫn còn. Ở installer, node -p với dấu nháy kép lồng trong PowerShell 5.1 làm lệnh hỏng, nên bản cài luôn báo 'Node quá cũ' dù Node đủ mới.
**Bài học:** Trên PowerShell 5.1, lồng nháy đơn bên trong nháy kép. Khi gọi cmd từ Node trên Windows, dùng windowsVerbatimArguments, nếu không lệnh xoá sẽ thất bại mà không báo lỗi.
**Artefact:** Hai đoạn lệnh trước và sau khi sửa, không có đường dẫn người dùng.
