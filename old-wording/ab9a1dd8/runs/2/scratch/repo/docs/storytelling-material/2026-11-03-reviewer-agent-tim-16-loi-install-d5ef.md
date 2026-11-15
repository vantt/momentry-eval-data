---
id: 2026-11-03-reviewer-agent-tim-16-loi-install-d5ef
code: M-64WM
aliases: [M-64WM]
date: 2026-11-03
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L2026", "claude:ab9a1dd8#L2039", "claude:ab9a1dd8#L2049", "claude:ab9a1dd8#L2058"]
hook: "Uninstall không xoá gì vẫn báo thành công; reviewer tìm 16 lỗi"
tension: cam_ma_van_lot
sides: ["Test Linux xanh, uninstall báo thành công", "Windows thật ra không xoá gì, install luôn báo Node quá cũ"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Reviewer agent tìm 16 lỗi: install Windows luôn báo 'Node quá cũ', uninstall không xoá gì nhưng vẫn báo thành công

**Bối cảnh:** Code và test đã xanh trên Linux. Một agent review độc lập được gọi đọc installer, uninstall và update.
**Chuyện gì xảy ra:** Reviewer báo 4 lỗi nặng, 5 trung bình, 7 nhẹ. Hai lỗi nặng làm install và uninstall hỏng trên Windows. PowerShell 5.1 làm mất dấu nháy trong lệnh node -p, nên version đọc ra 0 và installer luôn báo quá cũ. cmd.exe không hiểu dấu nháy kiểu Node nên lệnh xoá trễ thất bại mà vẫn báo thành công. Một lỗi khác có thể xoá cả cache trên Windows. Test Linux không bắt được những lỗi này.
**Bài học:** Đường chạy riêng theo nền tảng cần người đọc có hiểu biết về shell cụ thể. Test trên Linux không thay thế được.
**Artefact:** Dòng code PowerShell trước và sau khi sửa dấu nháy. Không có dữ liệu nhạy cảm.
