---
id: 2026-11-03-sua-settings-json-an-toan-kiem-d5ef
code: M-C8R2
aliases: [M-C8R2]
date: 2026-11-03
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L1028", "claude:ab9a1dd8#L2063", "claude:ab9a1dd8#L2102"]
hook: "Ghi settings.json an toàn: sao lưu, file tạm, kiểm đổi, xử lý symlink"
tension: none
sides: []
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Sửa settings.json an toàn: kiểm file có đổi giữa lúc đọc và ghi, xử lý symlink theo review

**Bối cảnh:** Hook phải ghi vào ~/.claude/settings.json, file của người dùng và của các phiên khác.
**Chuyện gì xảy ra:** Agent ghi có sao lưu, từ chối file hỏng, ghi qua file tạm rồi đổi tên, và kiểm lại file có đổi sau khi đọc không. Review yêu cầu thêm xử lý file dạng symlink; agent thêm test cho symlink và cho khoá hooks sai kiểu.
**Bài học:** Ghi file cấu hình của người khác cần ba thứ: sao lưu, kiểm thay đổi giữa đọc và ghi, và test cho file hỏng.
**Artefact:** Không có artefact đáng chụp.
