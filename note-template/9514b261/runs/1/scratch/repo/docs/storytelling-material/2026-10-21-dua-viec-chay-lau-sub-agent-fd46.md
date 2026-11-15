---
id: 2026-10-21-dua-viec-chay-lau-sub-agent-fd46
code: M-KZ7K
aliases: [M-KZ7K]
date: 2026-10-21
repo: repo
status: raw
signals: []
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:9514b261#L957", "claude:9514b261#L1347", "claude:9514b261#L2085", "claude:9514b261#L3195", "claude:9514b261#L3518"]
hook: "Việc chạy lâu đưa xuống nền, agent chờ thông báo thay vì hỏi liên tục"
tension: none
sides: []
strength: 0
stakes: 0
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đưa việc chạy lâu (sub-agent, probe, hội đồng) xuống nền rồi chờ thông báo hoàn thành, thay vì chờ đồng bộ hoặc hỏi liên tục

**Chuyện gì xảy ra:** Đưa việc chạy lâu (sub-agent, probe, hội đồng) xuống nền rồi chờ thông báo hoàn thành, thay vì chờ đồng bộ hoặc hỏi liên tục
**Góc người ngoài:** cách làm phổ biến là Chờ đồng bộ, hoặc poll file kết quả liên tục; ở đây khác ở Phiên mở ba sub-agent song song và nhiều probe nền, mỗi cái báo lại bằng thông báo, nên người dùng vẫn làm việc khác. Người đọc sẽ hỏi làm sao để không phải ngồi chờ.
