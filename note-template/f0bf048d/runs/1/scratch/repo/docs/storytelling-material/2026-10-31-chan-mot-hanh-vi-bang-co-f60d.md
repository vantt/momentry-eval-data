---
id: 2026-10-31-chan-mot-hanh-vi-bang-co-f60d
code: M-JX95
aliases: [M-JX95]
date: 2026-10-31
repo: repo
status: raw
signals: []
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:f0bf048d#L2284", "claude:f0bf048d#L3327", "claude:f0bf048d#L3340"]
hook: "Chặn agent bằng quyền Unix, không bằng lời dặn trong prompt"
tension: cam_ma_van_lot
sides: ["Viết quy tắc vào prompt và tin agent tuân theo", "Chỉ cơ chế như quyền hệ thống mới chặn thật"]
strength: 2
stakes: 2
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Chặn một hành vi bằng cơ chế (quyền Unix, quyền tài khoản, mạng) thay vì dựa vào lời dặn trong prompt, và giải thích rõ với người dùng về điều này.

**Chuyện gì xảy ra:** Chặn một hành vi bằng cơ chế (quyền Unix, quyền tài khoản, mạng) thay vì dựa vào lời dặn trong prompt, và giải thích rõ với người dùng về điều này.
**Góc người ngoài:** cách làm phổ biến là Nhiều người viết quy tắc vào prompt và tin agent sẽ tuân theo; ở đây khác ở Phiên từ chối 'đừng push lên main' vì lời dặn có thể bị phớt lờ, và thay bằng quyền chỉ đọc. Người đọc muốn biết vì sao nguyên tắc này quan trọng khi có agent tự chạy.
