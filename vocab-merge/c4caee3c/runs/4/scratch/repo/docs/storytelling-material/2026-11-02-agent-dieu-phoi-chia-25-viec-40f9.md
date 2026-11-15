---
id: 2026-11-02-agent-dieu-phoi-chia-25-viec-40f9
code: M-EQAZ
aliases: [M-EQAZ]
date: 2026-11-02
repo: repo
status: raw
signals: []
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:c4caee3c#L87", "claude:c4caee3c#L98", "claude:c4caee3c#L153", "claude:c4caee3c#L171", "claude:c4caee3c#L412", "claude:c4caee3c#L474", "claude:c4caee3c#L1043", "claude:c4caee3c#L1058", "claude:c4caee3c#L2964", "claude:c4caee3c#L2971"]
hook: "Một agent điều phối chia hơn 25 việc cho agent chạy song song"
tension: it_ma_nhieu
sides: ["một agent trung tâm giao việc", "25+ việc song song, mỗi việc một worktree, ghép đúng thứ tự"]
strength: 2
stakes: 2
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Agent điều phối chia 25+ việc thành các agent chạy nền song song (mỗi việc một worktree riêng), rồi ghép từng kết quả vào chuỗi bản vá theo đúng thứ tự phụ thuộc.

**Chuyện gì xảy ra:** Agent điều phối chia 25+ việc thành các agent chạy nền song song (mỗi việc một worktree riêng), rồi ghép từng kết quả vào chuỗi bản vá theo đúng thứ tự phụ thuộc.
**Góc người ngoài:** cách làm phổ biến là Hầu hết người dùng AI coding làm tuần tự trong một phiên, hoặc nhiều lắm mở vài cửa sổ chat tự quản lý; ít ai có một agent trung tâm giao việc, theo dõi, và merge kết quả của nhiều agent; ở đây khác ở Người đọc sẽ thắc mắc vì sao có thể chạy hàng chục việc cùng lúc mà không dẫm chân nhau, và làm sao các thay đổi chồng lấn trên cùng file được ghép lại đúng thứ tự.
