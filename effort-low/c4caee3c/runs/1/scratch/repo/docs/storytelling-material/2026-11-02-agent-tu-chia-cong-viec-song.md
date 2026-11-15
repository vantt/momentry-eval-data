---
id: 2026-11-02-agent-tu-chia-cong-viec-song
date: 2026-11-02
repo: repo
status: raw
signals: []
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:c4caee3c#L87", "claude:c4caee3c#L92", "claude:c4caee3c#L97", "claude:c4caee3c#L154", "claude:c4caee3c#L163", "claude:c4caee3c#L412", "claude:c4caee3c#L423", "claude:c4caee3c#L1199", "claude:c4caee3c#L1221", "claude:c4caee3c#L1250", "claude:c4caee3c#L1570", "claude:c4caee3c#L2138", "claude:c4caee3c#L2143", "claude:c4caee3c#L3798"]
hook: "Nhiều agent làm song song trên worktree riêng, lead ghép lại đúng thứ tự"
tension: none
sides: []
strength: 1
stakes: 1
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Agent tự chia công việc song song cho nhiều subagent, mỗi agent làm trên worktree riêng, rồi lead ghép lại theo đúng thứ tự phụ thuộc (chuỗi bản vá)

**Chuyện gì xảy ra:** Agent tự chia công việc song song cho nhiều subagent, mỗi agent làm trên worktree riêng, rồi lead ghép lại theo đúng thứ tự phụ thuộc (chuỗi bản vá)
**Góc người ngoài:** cách làm phổ biến là Thường một người hoặc một agent làm tuần tự trên một nhánh; ghép nhiều nhánh song song thường là xung đột và sửa tay; ở đây khác ở Phiên này chạy hơn chục agent cùng lúc, mỗi cái một worktree, rồi lead dựng lại chuỗi bản vá từ đầu mỗi khi có thay đổi ở đầu chuỗi. Người đọc sẽ hỏi làm sao tránh được việc các agent giẫm lên nhau.
