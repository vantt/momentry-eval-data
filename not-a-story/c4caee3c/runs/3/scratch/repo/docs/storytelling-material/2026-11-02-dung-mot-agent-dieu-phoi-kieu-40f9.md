---
id: 2026-11-02-dung-mot-agent-dieu-phoi-kieu-40f9
code: M-R2D5
aliases: [M-R2D5]
date: 2026-11-02
repo: repo
status: raw
signals: []
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:c4caee3c#L11", "claude:c4caee3c#L30", "claude:c4caee3c#L87", "claude:c4caee3c#L153", "claude:c4caee3c#L171", "claude:c4caee3c#L358", "claude:c4caee3c#L458", "claude:c4caee3c#L463", "claude:c4caee3c#L1570", "claude:c4caee3c#L1964"]
hook: "Một agent làm lead, nhiều agent con chạy song song trên worktree riêng"
tension: it_ma_nhieu
sides: ["Dev một mình thường chạy một phiên AI tuần tự", "Một lead điều phối nhiều agent, ghép từng việc khi xong"]
strength: 2
stakes: 2
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Dùng một agent điều phối kiểu lead: tách plan thành nhiều phase, mở nhiều agent con chạy song song trên các git worktree riêng, rồi ghép từng việc khi agent báo xong.

**Chuyện gì xảy ra:** Dùng một agent điều phối kiểu lead: tách plan thành nhiều phase, mở nhiều agent con chạy song song trên các git worktree riêng, rồi ghép từng việc khi agent báo xong.
**Góc người ngoài:** cách làm phổ biến là Hầu hết người làm một mình chạy một phiên AI tuần tự trong một thư mục, mỗi lần một việc, và tự merge bằng tay khi xong; ở đây khác ở Ở đây 25 việc chạy song song, mỗi việc có nhánh và thư mục riêng, lead chỉ ghép khi phụ thuộc đã xong. Người đọc sẽ hỏi làm sao chia việc mà không đụng file nhau, và khi nào nên dừng song song.
