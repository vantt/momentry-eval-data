---
id: 2026-11-03-zsh-va-ham-boc-lam-agent-d5ef
code: M-ST1A
aliases: [M-ST1A]
date: 2026-11-03
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:ab9a1dd8#L109", "claude:ab9a1dd8#L1226", "claude:ab9a1dd8#L1235", "claude:ab9a1dd8#L3891"]
hook: "Gõ `pi` mà chạy hàm bọc, không phải binary thật"
tension: none
sides: []
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# zsh và hàm bọc làm agent vấp nhiều lần

**Bối cảnh:** Agent chạy lệnh thử trong HOME tạm, nhưng môi trường là zsh và pi, omp là hàm shell bọc ngoài.
**Chuyện gì xảy ra:** Biến môi trường không tách đúng trong zsh, nên bốn lần lệnh thử phải chạy lại bằng bash. Lệnh `pi` và `omp` thật là hàm bọc, nên agent dùng `type -P` để tìm binary thật.
**Bài học:** Khi script phải chạy trong môi trường người dùng, hãy chạy bằng bash và dùng `type -P` để lấy đúng binary.
**Artefact:** Không có.
