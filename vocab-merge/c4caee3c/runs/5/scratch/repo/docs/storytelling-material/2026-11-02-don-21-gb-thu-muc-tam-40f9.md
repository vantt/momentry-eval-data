---
id: 2026-11-02-don-21-gb-thu-muc-tam-40f9
code: M-8253
aliases: [M-8253]
date: 2026-11-02
repo: repo
status: raw
signals: [số trước sau, khác]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L3955", "claude:c4caee3c#L3966", "claude:c4caee3c#L3973", "claude:c4caee3c#L3997"]
hook: "Dọn 21 GB thư mục tạm, /tmp vẫn còn đầy 26%"
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

# Dọn 21 GB thư mục tạm; /tmp còn 26%

**Bối cảnh:** Khi hầu hết agent đã xong, thư mục làm việc tạm chiếm 21 GB.
**Chuyện gì xảy ra:** Xoá worktree đã merge, 20 nhánh nháp (nội dung đã nằm trong master), dữ liệu eval tạm, cache và artifact CI đã đọc xong. Còn lại 6,4 GB, giữ đồ của các agent đang chạy.
**Bài học:** Dọn theo từng agent khi xong thay vì đợi cuối; liệt kê rõ cái giữ và cái xoá.
**Artefact:** Kết quả du -sh trước và sau.
