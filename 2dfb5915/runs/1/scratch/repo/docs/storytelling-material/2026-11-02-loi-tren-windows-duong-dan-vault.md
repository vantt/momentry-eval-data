---
id: 2026-11-02-loi-tren-windows-duong-dan-vault
date: 2026-11-02
repo: repo
status: raw
signals: [Nguyên nhân bất ngờ, artefact]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:2dfb5915#L1849", "claude:2dfb5915#L1873", "claude:2dfb5915#L1929", "claude:2dfb5915#L3340"]
hook: "Che đường dẫn vault rồi mà trên Windows vẫn lộ qua dấu \\\\"
tension: cam_ma_van_lot
sides: ["đường dẫn vault đã được che", "trên Windows dạng escape \\\\ vẫn lọt ra"]
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
**Góc người ngoài:** cách làm phổ biến là Chạy lại job, hoặc sửa theo log đầu tiên thấy, hoặc đoán là flaky; ở đây khác ở Phân biệt được lỗi thật (basename Windows) với lỗi hạ tầng (cache, runner không có máy, job bị huỷ). Với job bị huỷ do chờ runner thì chỉ chạy lại job đó. Người đọc hay mất giờ vì cứ đoán nên muốn quy trình này.
