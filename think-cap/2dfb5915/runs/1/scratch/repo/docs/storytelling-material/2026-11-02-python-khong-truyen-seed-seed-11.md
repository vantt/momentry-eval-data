---
id: 2026-11-02-python-khong-truyen-seed-seed-11
date: 2026-11-02
repo: repo
status: raw
signals: [nguyên nhân bất ngờ]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L474"]
hook: "Test không truyền --seed, nhưng seed 11 vẫn nằm sẵn trong preset"
tension: none
sides: []
strength: 0
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Python không truyền --seed: seed 11 nằm trong preset của fixture

**Bối cảnh:** Cần ghim seed để fixture sinh giống nhau giữa hai bên.
**Chuyện gì xảy ra:** Test Python không truyền --seed. Giá trị mặc định của preset fixture là 11, và tài liệu benchmark cũng ghi 11. Agent đọc preset rồi ghim 11 trong spec.lock.
**Bài học:** Khi test không truyền cờ, tìm default ở nguồn gốc thay vì đoán.
**Artefact:** Không có.
