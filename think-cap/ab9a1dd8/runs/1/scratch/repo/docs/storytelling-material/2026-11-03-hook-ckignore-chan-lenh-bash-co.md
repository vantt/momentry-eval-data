---
id: 2026-11-03-hook-ckignore-chan-lenh-bash-co
date: 2026-11-03
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:ab9a1dd8#L1604", "claude:ab9a1dd8#L1613", "claude:ab9a1dd8#L3367", "claude:ab9a1dd8#L3369"]
hook: "Hook chặn cả lệnh tạo CI vì chứa chữ 'dist'"
tension: nho_ma_to
sides: ["chỉ một chuỗi 'dist' hay '.git' trong lệnh", "cả lệnh bash bị chặn, phải đổi công cụ"]
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Hook .ckignore chặn lệnh bash có chuỗi dist và .git

**Bối cảnh:** Hook an toàn trong môi trường agent chặn lệnh bash chứa một số chuỗi, trong đó có dist và .git.
**Chuyện gì xảy ra:** Lần đầu, lệnh tạo file workflow CI bị chặn vì chứa dist. Agent chuyển sang công cụ ghi file. Lần hai, khi viết test, lệnh bash chứa .git cũng bị chặn, và agent đọc file bằng công cụ khác.
**Bài học:** Các chuỗi như tên thư mục build có thể kích hoạt chặn. Dùng công cụ ghi file thay cho lệnh bash khi chỉ cần tạo file.
**Artefact:** Thông báo chặn của hook, không có đường dẫn người dùng.
