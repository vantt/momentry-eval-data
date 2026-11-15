---
id: 2026-11-02-don-21-gb-worktree-sau-khi-40f9
code: M-09YV
aliases: [M-09YV]
date: 2026-11-02
repo: repo
status: raw
signals: [so_truoc_so_sau]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L3955", "claude:c4caee3c#L3966", "claude:c4caee3c#L3973", "claude:c4caee3c#L3997"]
hook: "Dọn worktree đã merge: ổ đĩa từ 21 GB còn 6,4 GB"
tension: it_ma_nhieu
sides: ["Chỉ xoá phần đã xong", "Thu lại hơn 14 GB"]
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Dọn 21 GB worktree sau khi các nhánh đã merge

**Bối cảnh:** Thư mục làm việc tạm chứa worktree, node_modules, log và dữ liệu eval của nhiều agent.
**Chuyện gì xảy ra:** Chủ dự án yêu cầu dọn những gì đã xong. Agent xoá năm worktree đã merge, 20 nhánh nháp đã có nội dung trong master, dữ liệu eval tạm, cache và log. Thư mục giảm từ 21 GB xuống 7,8 GB, rồi 6,4 GB. Phần của các agent còn chạy được giữ lại.
**Bài học:** Dọn theo trạng thái: đã merge và không còn agent dùng thì xoá, còn lại giữ đến khi agent kết thúc.
