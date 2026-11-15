---
id: 2026-11-02-gom-cac-cau-hoi-cong-thanh-3c6e
code: M-45ZT
aliases: [M-45ZT]
date: 2026-11-02
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:2dfb5915#L485", "claude:2dfb5915#L486", "claude:2dfb5915#L555", "claude:2dfb5915#L563"]
hook: "Agent gom hai câu hỏi cổng thành một lần, người dùng gật luôn"
tension: none
sides: []
strength: 0
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Gom các câu hỏi cổng thành một lần hỏi người dùng

**Bối cảnh:** Plan có các cổng (gate G0) nằm trước phase 08, agent phải hỏi người dùng trước khi làm tiếp.
**Chuyện gì xảy ra:** Agent hỏi gom một lần: đã test chưa và có đổi schema không. Người dùng trả lời đồng ý chạy tiếp. Sau đó người dùng hỏi có câu nào còn chặn bản cài được không, và agent trả lời là không, chỉ còn ba việc để nghiệm thu sau.
**Bài học:** Gom mọi câu hỏi cổng thành một lần hỏi và nói rõ việc nào chặn, việc nào chỉ để nghiệm thu.
**Góc người ngoài:** cách làm phổ biến là Hỏi người dùng từng bước khi gặp quyết định nhỏ, hoặc tự quyết hết mà không ghi lại; ở đây khác ở Các cổng như 'chạy trên vault thật' hoặc 'tuần dùng song song' được ghi rõ trong plan; agent làm được phần còn lại và báo đúng việc đang chờ ai. Người đọc muốn biết cách ghi cổng để không phải hỏi lại từng việc.
