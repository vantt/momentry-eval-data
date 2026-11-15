---
id: 2026-11-02-hai-lech-chi-thay-tren-windows
date: 2026-11-02
repo: repo
status: raw
signals: [nguyên nhân bất ngờ]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L1820", "claude:2dfb5915#L1873", "claude:2dfb5915#L3242"]
hook: "Linux sạch sẽ, Windows lộ đường dẫn vault vì hai dấu gạch"
tension: cam_ma_van_lot
sides: ["hàm Scrub đã che đường dẫn vault", "dạng escape hai gạch chéo vẫn lọt ra đầu ra"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Hai lệch chỉ thấy trên Windows: đường dẫn escape trong JSON

**Bối cảnh:** Bộ so khớp xanh trên Linux nhưng đỏ trên Windows ở phần CLI.
**Chuyện gì xảy ra:** Đường dẫn Windows trong JSON có dấu gạch chéo ngược bị escape thành hai dấu. Hàm Scrub chỉ che dạng thường, nên đường dẫn vault lộ trong đầu ra. Trên Linux hai dạng giống nhau nên không lộ. Sửa Scrub để che cả dạng escape, ưu tiên chuỗi dài nhất. Golden không đổi.
**Bài học:** Đầu ra JSON có dạng escape riêng cho Windows. Test che dữ liệu phải mô phỏng đường dẫn Windows trên mọi OS.
**Artefact:** Không có.
