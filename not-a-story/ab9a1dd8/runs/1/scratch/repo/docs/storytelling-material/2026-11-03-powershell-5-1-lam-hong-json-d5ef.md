---
id: 2026-11-03-powershell-5-1-lam-hong-json-d5ef
code: M-FVD8
aliases: [M-FVD8]
date: 2026-11-03
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L2614", "claude:ab9a1dd8#L2674", "claude:ab9a1dd8#L2810"]
hook: "PowerShell 5.1 làm hỏng JSON, runner Windows lại chạy quyền Administrator"
tension: nho_ma_to
sides: ["Một đối số JSON truyền cho lệnh ngoài", "PowerShell 5.1 làm hỏng nó, momentry còn từ chối chạy root"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# PowerShell 5.1 làm hỏng JSON truyền cho lệnh ngoài; runner Windows chạy quyền Administrator

**Bối cảnh:** Lifecycle installer trên Windows chạy trong CI, sau khi unit test đã xanh.
**Chuyện gì xảy ra:** Bước 'config set privacy.sources' kèm JSON hỏng vì PowerShell 5.1 làm hỏng đối số khi truyền cho chương trình ngoài. Runner CI chạy Administrator nên momentry từ chối chạy root. Trên Windows đổi sang 'config privacy-add', và test bật cờ cho phép root. Sau đó test Windows đạt 231 pass, 0 fail.
**Bài học:** Đừng truyền JSON qua PowerShell 5.1 cho lệnh ngoài. Dùng đối số đơn giản thay cho JSON.
**Artefact:** Đoạn lệnh PowerShell trước và sau. Không chứa khoá hay tên người.
