---
id: 2026-11-02-installer-chuyen-sang-tieng-anh-vi-3c6e
code: M-B8B4
aliases: [M-B8B4]
date: 2026-11-02
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L1237"]
hook: "PowerShell 5.1 làm hỏng dấu tiếng Việt, installer đành nói tiếng Anh"
tension: chon_mot_mat_mot
sides: ["Thông điệp tiếng Việt cho người dùng", "Script chạy được trên PowerShell 5.1"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Installer chuyển sang tiếng Anh vì PowerShell 5.1 làm hỏng dấu tiếng Việt

**Bối cảnh:** Script cài được tải và chạy qua irm trên Windows PowerShell 5.1.
**Chuyện gì xảy ra:** Khi đọc script qua irm, PowerShell 5.1 làm hỏng dấu tiếng Việt trong thông điệp. Thông điệp chuyển sang tiếng Anh và script chỉ dùng ASCII.
**Bài học:** Kiểm mã hoá theo đúng đường đi mà người dùng sẽ tải, không theo file trên máy dev.
