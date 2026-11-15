---
id: 2026-11-02-loi-tren-windows-duong-dan-vault
date: 2026-11-02
repo: repo
status: raw
signals: [Nguyên nhân bất ngờ, artefact]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L1849", "claude:2dfb5915#L1873", "claude:2dfb5915#L1929", "claude:2dfb5915#L3340"]
hook: "Che đường dẫn vault xong vẫn lộ, vì Windows viết dấu gạch ngược thành hai"
tension: cam_ma_van_lot
sides: ["Đường dẫn đã được che trong bản so khớp", "Dạng `\\\\` escape của Windows không bị che, vẫn lọt ra"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Lỗi trên Windows: đường dẫn vault bị lộ dạng JSON-escape trong bản so khớp

**Bối cảnh:** Bộ so khớp dump đầu ra CLI của cả hai bản và che đường dẫn vault bằng placeholder.
**Chuyện gì xảy ra:** Trên Linux che đường dẫn là đủ, nhưng trên Windows dấu `\` trong JSON được escape thành `\\`, nên đường dẫn ở dạng escape không bị che. CI Windows đỏ ở đúng bước này; sửa bằng cách che cả dạng escape, dài nhất trước. Máy Windows thật của người dùng phát hiện thêm lỗi UTF-8 khi in tiếng Việt qua pipe và lỗi PyYAML không thấy trong `--user` site (do cờ `-I`).
**Bài học:** Che dữ liệu nhạy cảm trong JSON phải tính tới dạng escape; cờ `-I` của Python ẩn luôn site-packages người dùng.
**Artefact:** Đoạn log CI đỏ rồi xanh (che tên vault).
