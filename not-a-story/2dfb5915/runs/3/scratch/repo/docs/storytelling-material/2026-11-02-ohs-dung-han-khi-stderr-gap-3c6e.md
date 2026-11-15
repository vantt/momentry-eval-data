---
id: 2026-11-02-ohs-dung-han-khi-stderr-gap-3c6e
code: M-F4HK
aliases: [M-F4HK]
date: 2026-11-02
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L607", "claude:2dfb5915#L631"]
hook: "Một byte lỗi trên stderr làm OHS đứng im 60 giây"
tension: nho_ma_to
sides: ["Một dòng stderr có byte 0xFF trên máy code page Việt", "Pipe đầy, event loop dừng, mọi search timeout mà không restart"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# OHS đứng hẳn khi stderr gặp byte UTF-8 lỗi, trên máy có code page Việt

**Bối cảnh:** Module OHS giữ một tiến trình Node chạy lâu, đọc stdout và stderr qua pipe.
**Chuyện gì xảy ra:** Trên Windows có code page như CP1258, một dòng stderr có byte không hợp lệ làm reader thoát. Pipe đầy, mọi console.error của OHS block và event loop dừng. Vì stdout vẫn mở nên không có sự kiện Exited, không restart, và mọi search timeout sau 60 giây. Fix là đọc tới EOF với from_utf8_lossy, và ghi nhận test có byte 0xFF.
**Bài học:** Lỗi mã hoá ở một luồng phụ có thể làm đứng cả tiến trình mà không có tín hiệu thoát nào. Đọc luồng phải luôn tới EOF.
