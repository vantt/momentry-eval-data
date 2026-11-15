---
id: 2026-10-21-agent-kiem-tra-khoa-api-ma-fd46
code: M-N6M6
aliases: [M-N6M6]
date: 2026-10-21
repo: repo
status: raw
signals: []
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:9514b261#L3366", "claude:9514b261#L3531", "claude:9514b261#L3895", "claude:9514b261#L3899", "claude:9514b261#L3944"]
hook: "Agent kiểm tra khoá API mà không in ra: chỉ đếm độ dài và loại ký tự"
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

# Agent kiểm tra khoá API mà không in giá trị ra. Nó chỉ đếm độ dài và loại ký tự, và che giá trị bằng regex khi đưa các alias lên màn hình.

**Chuyện gì xảy ra:** Agent kiểm tra khoá API mà không in giá trị ra. Nó chỉ đếm độ dài và loại ký tự, và che giá trị bằng regex khi đưa các alias lên màn hình.
**Góc người ngoài:** cách làm phổ biến là Cat file hoặc dán khoá vào chat để xem, hoặc hiển thị nguyên cấu hình chứa bí mật; ở đây khác ở Khoá không lộ vào lịch sử hội thoại hay màn hình, nhưng vẫn đủ thông tin để chẩn đoán lỗi như ký tự thừa. Người đọc sẽ muốn học cách hỏi trạng thái của một bí mật mà không đọc ra nó.
