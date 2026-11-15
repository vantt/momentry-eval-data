---
id: 2026-11-02-script-cai-dung-ascii-vi-powershell
date: 2026-11-02
repo: repo
status: raw
signals: [ràng buộc định hình thiết kế]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L1237"]
hook: "Script cài bỏ hẳn dấu tiếng Việt vì PowerShell 5.1 làm hỏng chữ"
tension: khac
sides: ["Người dùng Việt muốn thông báo tiếng Việt", "PowerShell làm hỏng dấu nên phải dùng tiếng Anh"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Script cài dùng ASCII vì PowerShell 5.1 làm hỏng dấu tiếng Việt

**Bối cảnh:** Script cài chạy bằng irm và iex trên Windows PowerShell 5.1.
**Chuyện gì xảy ra:** PowerShell 5.1 đọc script qua irm làm hỏng dấu tiếng Việt trong thông báo. Vì vậy script cài chỉ dùng ASCII, thông báo bằng tiếng Anh; README tiếng Việt vẫn giữ cho người đọc.
**Bài học:** Với script cài trên Windows cũ, kiểm mã hoá trước khi viết thông báo nhiều ngôn ngữ.
**Artefact:** Ảnh terminal hiển thị dấu bị hỏng, nếu chụp lại được; không có sẵn trong phiên.
