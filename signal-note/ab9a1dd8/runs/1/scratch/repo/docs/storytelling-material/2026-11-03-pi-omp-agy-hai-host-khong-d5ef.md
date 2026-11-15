---
id: 2026-11-03-pi-omp-agy-hai-host-khong-d5ef
code: M-6VVB
aliases: [M-6VVB]
date: 2026-11-03
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:ab9a1dd8#L3274", "claude:ab9a1dd8#L3278", "claude:ab9a1dd8#L3287", "claude:ab9a1dd8#L3300", "claude:ab9a1dd8#L3306", "claude:ab9a1dd8#L3410", "claude:ab9a1dd8#L3426", "claude:ab9a1dd8#L3428", "claude:ab9a1dd8#L3433", "claude:ab9a1dd8#L3770", "claude:ab9a1dd8#L3777"]
hook: "Hai host không có hook shell, agy chỉ có Start và Stop"
tension: chon_mot_mat_mot
sides: ["Muốn gom phiên phải viết extension riêng", "User chọn gom agy sau, mở phiên sau"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# pi, omp, agy: hai host không có hook shell, agy chỉ có SessionStart và Stop

**Bối cảnh:** User yêu cầu thêm ba host. Một researcher subagent khảo sát tài liệu và máy thật.
**Chuyện gì xảy ra:** pi và omp không có hook shell như Claude Code, muốn gom phải viết extension TypeScript. agy có SessionStart và Stop; Stop chạy sau mỗi lượt và chặn agent đang chạy, không có sự kiện kết thúc phiên. User chọn gom agy khi mở phiên sau. Lần đọc hooks.json của agy lỗi vì glob không khớp, phải dùng ls.
**Bài học:** Trước khi thiết kế gom tự động, kiểm host có sự kiện kết thúc phiên không. Thiếu nó thì phải gom lúc mở phiên sau.
**Artefact:** Bảng ba host với sự kiện có và thiếu.
