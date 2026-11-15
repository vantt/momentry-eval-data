---
id: 2026-11-03-zsh-cua-agent-khong-tach-bien
date: 2026-11-03
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:ab9a1dd8#L101", "claude:ab9a1dd8#L105", "claude:ab9a1dd8#L1199", "claude:ab9a1dd8#L1226", "claude:ab9a1dd8#L3770", "claude:ab9a1dd8#L3777"]
hook: "Bốn lần lệnh kiểm chết ngay từ đầu vì zsh, phải gọi bash -c"
tension: nho_ma_to
sides: ["khác biệt nhỏ giữa zsh và bash", "ít nhất bốn lệnh kiểm chết trước khi chạy"]
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# zsh của agent không tách biến và báo no matches khi glob rỗng, khiến lệnh kiểm chết trước khi chạy

**Bối cảnh:** Agent chạy các bước kiểm trong HOME tạm bằng shell mặc định zsh.
**Chuyện gì xảy ra:** Ít nhất bốn lần lệnh chết ngay từ đầu: zsh không tách biến lệnh, không tìm thấy file vì biến không được mở rộng, và glob không khớp báo lỗi thay vì trả về rỗng. Mỗi lần phải chuyển sang bash -c để chạy lại.
**Bài học:** Chạy script kiểm bằng bash -c rõ ràng, đừng dựa vào shell mặc định của agent.
**Artefact:** Thông báo lỗi zsh, không có đường dẫn người dùng.
