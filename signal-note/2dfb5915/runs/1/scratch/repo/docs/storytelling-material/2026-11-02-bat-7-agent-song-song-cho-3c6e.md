---
id: 2026-11-02-bat-7-agent-song-song-cho-3c6e
code: M-V7NJ
aliases: [M-V7NJ]
date: 2026-11-02
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L62", "claude:2dfb5915#L120", "claude:2dfb5915#L152", "claude:2dfb5915#L178", "claude:2dfb5915#L474"]
hook: "Bảy agent chạy song song, sau 1 phase chạy trước một mình"
tension: none
sides: []
strength: 0
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Bật 7 agent song song cho một plan port Rust: phase 01 chạy trước một mình, sau đó dựng 7 phase còn lại cùng lúc

**Bối cảnh:** Plan port lõi sang Rust có 17 phase. Phase nền phải xong trước, các phase còn lại được tách thành các nhánh worktree riêng và merge từng cái khi xong.
**Chuyện gì xảy ra:** Phase 01 (khung workspace) xong và CI xanh trên 3 nền tảng. Sau đó 7 agent chạy song song, mỗi agent một worktree. Tới lúc báo tiến độ, 5 phase đã merge và push, bộ so khớp với bản Python đạt 17 trên 64 mục, không có lệch nào chưa có tên.
**Bài học:** Tách phase nền chạy trước, rồi mới cho các phase độc lập chạy song song trong worktree riêng; mỗi nhánh merge khi có kết quả kiểm chứng.
**Artefact:** Bảng trạng thái phase ở báo cáo tiến độ (L474). Nên che tên đường dẫn và tên repo trước khi đăng.
