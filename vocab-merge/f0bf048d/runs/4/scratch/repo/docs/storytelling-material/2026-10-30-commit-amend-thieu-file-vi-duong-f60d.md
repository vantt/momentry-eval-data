---
id: 2026-10-30-commit-amend-thieu-file-vi-duong-f60d
code: M-NW7A
aliases: [M-NW7A]
date: 2026-10-30
repo: repo
status: raw
signals: [nguyên nhân gốc nhỏ]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L1265", "claude:f0bf048d#L1272"]
hook: "Commit --amend lặng lẽ thiếu file vì đường dẫn cũ đã đổi tên"
tension: nho_ma_to
sides: ["Lệnh add và amend trông như đã xong", "Đường dẫn cũ báo lỗi nên commit có thể thiếu file"]
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Commit --amend thiếu file vì đường dẫn cũ đã đổi tên

**Bối cảnh:** Sửa tài liệu rồi amend commit, trong lúc một file đã đổi tên.
**Chuyện gì xảy ra:** Lệnh git add dùng đường dẫn file cũ nên báo fatal pathspec, và commit có thể thiếu file. Kiểm lại bằng git show --stat rồi add đúng đường dẫn mới và amend.
**Bài học:** Trước khi amend, xem lại danh sách file trong commit để tránh bỏ sót file đổi tên.
**Artefact:** Đầu ra git show --stat HEAD.
