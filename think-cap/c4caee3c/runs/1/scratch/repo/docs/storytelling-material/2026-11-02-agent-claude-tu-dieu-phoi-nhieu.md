---
id: 2026-11-02-agent-claude-tu-dieu-phoi-nhieu
date: 2026-11-02
repo: repo
status: raw
signals: []
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:c4caee3c#L41", "claude:c4caee3c#L153", "claude:c4caee3c#L412", "claude:c4caee3c#L1076", "claude:c4caee3c#L1082", "claude:c4caee3c#L1084", "claude:c4caee3c#L1322", "claude:c4caee3c#L1323"]
hook: "Một agent điều phối nhiều agent con trên nhiều worktree, tự ghép bản vá"
tension: none
sides: []
strength: 0
stakes: 1
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Agent Claude tự điều phối nhiều agent con chạy song song trên nhiều worktree và nhánh, mỗi agent một việc, rồi tự ghép (merge/cherry-pick) và kiểm chuỗi bản vá theo đúng thứ tự phụ thuộc trước khi push.

**Chuyện gì xảy ra:** Agent Claude tự điều phối nhiều agent con chạy song song trên nhiều worktree và nhánh, mỗi agent một việc, rồi tự ghép (merge/cherry-pick) và kiểm chuỗi bản vá theo đúng thứ tự phụ thuộc trước khi push.
**Góc người ngoài:** cách làm phổ biến là Phần lớn dev dùng AI theo kiểu một phiên, một việc, làm tuần tự; khi việc lớn thì tự chia nhỏ rồi chờ từng phần xong mới làm tiếp, hoặc dùng một nhánh duy nhất cho mọi thay đổi; ở đây khác ở Ở đây nhiều việc chạy đồng thời, mỗi việc cô lập trong worktree riêng, và lead kiểm lại thứ tự ghép (áp P00→P01→P02… trên tag gốc) trước khi đẩy. Người đọc sẽ muốn biết cách tránh xung đột giữa các agent cùng sửa một file và cách giữ thứ tự phụ thuộc.
