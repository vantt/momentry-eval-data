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
hook: "Một byte 0xFF trên stderr làm OHS đứng, mọi search timeout 60 giây"
tension: nho_ma_to
sides: ["Một byte UTF-8 lỗi trên stderr", "Pipe đầy, event loop dừng, mọi search timeout sau 60 giây"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một công cụ dòng lệnh hỏi Claude Desktop về graph vault Obsidian, đang thay bản Python bằng lõi Rust. Code đọc stderr của tiến trình Node bằng lines(), coi như dòng nào cũng đọc được. Hoá ra một byte không hợp lệ trên máy có code page tiếng Việt làm reader dừng, pipe đầy, và mọi search timeout sau 60 giây mà không có tín hiệu thoát nào. Ai làm tiến trình con qua pipe nên nghe, vì lỗi mã hoá ở luồng phụ có thể đứng cả tiến trình."
audience: dev Rust làm tiến trình con và pipe
spine_context: "Một công cụ dòng lệnh để hỏi Claude Desktop về graph của vault Obsidian, đang thay bản Python bằng lõi Rust."
spine_context_lines: [profile, "claude:2dfb5915#L11"]
spine_want: Hoàn tất plan lõi Rust và có một bản installable.
spine_want_lines: ["claude:2dfb5915#L11", "claude:2dfb5915#L571"]
spine_obstacle: "Module OHS giữ một tiến trình Node chạy lâu; khi stderr gặp byte UTF-8 không hợp lệ, reader thoát, pipe đầy và OHS đứng mà không có tín hiệu thoát."
spine_obstacle_lines: ["claude:2dfb5915#L607"]
spine_turn: "Code đọc stderr bằng lines(), coi như dòng nào cũng đọc được; hoá ra một byte lỗi làm reader dừng và kéo theo cả tiến trình đứng."
spine_turn_lines: ["claude:2dfb5915#L607"]
spine_action: "Sửa để reader đọc tới EOF với UTF-8 lossy, đưa stdin sang luồng ghi riêng, rồi merge và push lên main."
spine_action_lines: ["claude:2dfb5915#L631", "claude:2dfb5915#L639"]
spine_outcome: "Đã push lên main, nhưng test mới chỉ chạy trên Linux; CI sẽ là lần chạy đầu trên Windows và macOS."
spine_outcome_lines: ["claude:2dfb5915#L631", "claude:2dfb5915#L640"]
spine_takeaway: "Đọc luồng phụ phải luôn tới EOF, và lỗi mã hoá nên được thay bằng ký tự thay thế thay vì dừng reader."
spine_takeaway_lines: ["claude:2dfb5915#L607"]
completeness: 7
---

# OHS đứng hẳn khi stderr gặp byte UTF-8 lỗi, trên máy có code page Việt

**Góc kể:** Một công cụ dòng lệnh hỏi Claude Desktop về graph vault Obsidian, đang thay bản Python bằng lõi Rust. Code đọc stderr của tiến trình Node bằng lines(), coi như dòng nào cũng đọc được. Hoá ra một byte không hợp lệ trên máy có code page tiếng Việt làm reader dừng, pipe đầy, và mọi search timeout sau 60 giây mà không có tín hiệu thoát nào. Ai làm tiến trình con qua pipe nên nghe, vì lỗi mã hoá ở luồng phụ có thể đứng cả tiến trình.
**Bối cảnh:** Module OHS giữ một tiến trình Node chạy lâu, đọc stdout và stderr qua pipe.
**Chuyện gì xảy ra:** Trên Windows có code page như CP1258, một dòng stderr có byte không hợp lệ làm reader thoát. Pipe đầy, mọi console.error của OHS block và event loop dừng. Vì stdout vẫn mở nên không có sự kiện Exited, không restart, và mọi search timeout sau 60 giây. Fix là đọc tới EOF với from_utf8_lossy, và ghi nhận test có byte 0xFF.
**Bài học:** Lỗi mã hoá ở một luồng phụ có thể làm đứng cả tiến trình mà không có tín hiệu thoát nào. Đọc luồng phải luôn tới EOF.
