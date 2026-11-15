---
id: 2026-11-02-don-thu-muc-lam-viec-tu-40f9
code: M-YJ1G
aliases: [M-YJ1G]
date: 2026-11-02
repo: repo
status: raw
signals: [khac, rang_buoc_thiet_ke]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L3955", "claude:c4caee3c#L3966", "claude:c4caee3c#L3973", "claude:c4caee3c#L3997"]
hook: "Dọn từ 21 GB còn 6,4 GB mà không đụng agent đang chạy"
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

# Dọn thư mục làm việc: từ 21 GB xuống 6,4 GB, giữ phần agent còn dùng

**Bối cảnh:** Thư mục tạm ohs-wt chứa worktree, bản dựng và cache của các agent. Nhiều nhánh nháp đã merge xong.
**Chuyện gì xảy ra:** Lead xoá 5 worktree đã merge, 20 nhánh nháp (nội dung đã nằm trong master), dữ liệu eval tạm và artifact CI đã đọc xong. Giữ lại worktree của agent còn chạy cho đến khi agent xong. Không động vào thư mục của một phiên Claude khác trên cùng máy.
**Bài học:** Dọn theo trạng thái: xoá cái đã merge, giữ cái agent còn đọc, và ghi quy ước 'xong thì chuyển đi'.
**Artefact:** Kết quả du -sh trước và sau, không kèm đường dẫn.
