---
id: 2026-11-02-don-21g-lam-viec-tam-sau
date: 2026-11-02
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L3955", "claude:c4caee3c#L3966", "claude:c4caee3c#L3973", "claude:c4caee3c#L3997"]
hook: "Dọn 21G xuống 6,4G mà không xoá dữ liệu phiên khác"
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

# Dọn 21G làm việc tạm sau khi các agent xong

**Bối cảnh:** Thư mục làm việc tạm đã tích 21G qua nhiều worktree, node_modules và dữ liệu eval.
**Chuyện gì xảy ra:** Xoá worktree đã merge, nhánh nháp, dữ liệu eval tạm, artefact CI đã đọc; giữ lại thứ agent còn dùng. Giảm xuống 6,4G, không xoá dữ liệu của phiên khác.
**Bài học:** Dọn theo từng phần khi agent xong, và giữ lại những gì còn cần.
**Artefact:** Không cần.
