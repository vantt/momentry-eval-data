---
id: 2026-10-29-agent-theo-doi-viec-dang-chay-c455
code: M-N1PN
aliases: [M-N1PN]
date: 2026-10-29
repo: repo
status: raw
signals: []
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:0faf0bb2#L1204", "claude:0faf0bb2#L1212", "claude:0faf0bb2#L1228", "claude:0faf0bb2#L3501", "claude:0faf0bb2#L3591", "claude:0faf0bb2#L3679"]
hook: "Agent có Monitor nền nên không cần sleep hay bấm refresh"
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

# Agent theo dõi việc đang chạy bằng một Monitor nền: mỗi khi trạng thái hoặc comment đổi, agent nhận thông báo, không cần hỏi lại hay chờ bằng sleep.

**Chuyện gì xảy ra:** Agent theo dõi việc đang chạy bằng một Monitor nền: mỗi khi trạng thái hoặc comment đổi, agent nhận thông báo, không cần hỏi lại hay chờ bằng sleep.
**Góc người ngoài:** cách làm phổ biến là Người dùng thường tự bấm refresh, hoặc bảo AI chạy vòng lặp sleep rồi hỏi lại trạng thái, hoặc chờ đến khi có kết quả cuối mới xem; ở đây khác ở Người dùng không phải nhắc, agent vẫn làm việc khác trong lúc chờ và được báo khi có sự kiện thật. Người đọc sẽ hỏi làm sao để agent 'tự để mắt' đến một tiến trình dài.
