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
hook: "Một byte lỗi trên stderr làm đứng cả OHS, mọi search treo 60 giây"
tension: nho_ma_to
sides: ["Một dòng stderr có byte UTF-8 không hợp lệ trên máy code page Việt", "Reader thoát, pipe đầy, event loop dừng, không restart, mọi search timeout"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Công cụ dòng lệnh hỏi Claude Desktop về graph vault Obsidian đang thay bản Python bằng lõi Rust, và module OHS giữ một tiến trình Node chạy nền. Người làm tưởng đọc stderr bằng lines() là đủ, nhưng một byte UTF-8 lỗi trên máy code page tiếng Việt làm reader thoát; pipe đầy, cả tiến trình đứng và mọi tìm kiếm timeout sau 60 giây mà không có tín hiệu thoát nào. Ai giữ tiến trình con qua pipe nên đọc tới EOF và chịu được byte lỗi."
audience: dev giữ tiến trình con qua pipe trong Rust hoặc Node
spine_context: "Một công cụ dòng lệnh để hỏi Claude Desktop về graph của vault Obsidian, đang thay bản Python bằng lõi Rust. Module OHS giữ một tiến trình Node chạy lâu."
spine_context_lines: [profile, "claude:2dfb5915#L11"]
spine_want: Đưa lõi Rust tới một bản installable.
spine_want_lines: ["claude:2dfb5915#L571"]
spine_obstacle: Review tìm ra hai lỗi mức High có thể làm đứng OHS hoặc treo khi thoát.
spine_obstacle_lines: ["claude:2dfb5915#L607"]
spine_turn: "Tưởng đọc stderr bằng lines() là đủ; hoá ra một byte UTF-8 lỗi trên máy code page tiếng Việt làm reader thoát, pipe đầy, OHS đứng mà không có tín hiệu thoát, và mọi tìm kiếm timeout sau 60 giây."
spine_turn_lines: ["claude:2dfb5915#L607"]
spine_action: "Gửi kết quả review về cho agent đã viết module để sửa trên nhánh của nó; agent sửa trong một commit, rồi merge và push."
spine_action_lines: ["claude:2dfb5915#L615", "claude:2dfb5915#L631", "claude:2dfb5915#L639"]
spine_outcome: "Các lỗi review đã được sửa, đã merge và push. Clippy qua cho Windows và macOS; test mới chỉ chạy trên Linux, CI sẽ là lần chạy đầu trên hai hệ kia."
spine_outcome_lines: ["claude:2dfb5915#L631", "claude:2dfb5915#L640"]
spine_takeaway: Đọc luồng phụ phải tới EOF và chịu được byte lỗi; lỗi mã hoá ở đó có thể làm đứng cả tiến trình mà không có tín hiệu thoát.
spine_takeaway_lines: ["claude:2dfb5915#L607"]
completeness: 7
---

# OHS đứng hẳn khi stderr gặp byte UTF-8 lỗi, trên máy có code page Việt

**Góc kể:** Công cụ dòng lệnh hỏi Claude Desktop về graph vault Obsidian đang thay bản Python bằng lõi Rust, và module OHS giữ một tiến trình Node chạy nền. Người làm tưởng đọc stderr bằng lines() là đủ, nhưng một byte UTF-8 lỗi trên máy code page tiếng Việt làm reader thoát; pipe đầy, cả tiến trình đứng và mọi tìm kiếm timeout sau 60 giây mà không có tín hiệu thoát nào. Ai giữ tiến trình con qua pipe nên đọc tới EOF và chịu được byte lỗi.
**Bối cảnh:** Module OHS giữ một tiến trình Node chạy lâu, đọc stdout và stderr qua pipe.
**Chuyện gì xảy ra:** Trên Windows có code page như CP1258, một dòng stderr có byte không hợp lệ làm reader thoát. Pipe đầy, mọi console.error của OHS block và event loop dừng. Vì stdout vẫn mở nên không có sự kiện Exited, không restart, và mọi search timeout sau 60 giây. Fix là đọc tới EOF với from_utf8_lossy, và ghi nhận test có byte 0xFF.
**Bài học:** Lỗi mã hoá ở một luồng phụ có thể làm đứng cả tiến trình mà không có tín hiệu thoát nào. Đọc luồng phải luôn tới EOF.
