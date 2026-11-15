---
id: 2026-11-02-khi-hub-tu-choi-gui-skill-c4b4
code: M-10FV
aliases: [M-10FV]
date: 2026-11-02
repo: repo
status: raw
signals: []
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:6a207191#L1007", "claude:6a207191#L1068", "claude:6a207191#L1073"]
hook: "Hub từ chối gửi, agent không lách mà đưa lệnh cho người dùng"
tension: cam_ma_van_lot
sides: ["Thêm cờ bỏ xác nhận là xong việc ngay", "Agent chọn dừng, đưa lệnh để người dùng tự chạy"]
strength: 2
stakes: 0
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Khi hub từ chối gửi skill vì cờ `--yes` cần tin cậy, agent không tìm cách lách. Nó dừng, giải thích lý do và đưa lệnh để người dùng tự chạy trong prompt có dấu `!`.

**Chuyện gì xảy ra:** Khi hub từ chối gửi skill vì cờ `--yes` cần tin cậy, agent không tìm cách lách. Nó dừng, giải thích lý do và đưa lệnh để người dùng tự chạy trong prompt có dấu `!`.
**Góc người ngoài:** cách làm phổ biến là Nhiều agent sẽ thêm cờ bỏ xác nhận để hoàn thành việc, hoặc chạy thẳng lệnh có quyền ghi token ra ngoài; ở đây khác ở Đây là ranh giới rõ giữa việc agent làm được và việc cần người xác nhận khi có gửi dữ liệu ra ngoài. Người đọc sẽ hỏi làm sao agent biết nên dừng ở đó.
