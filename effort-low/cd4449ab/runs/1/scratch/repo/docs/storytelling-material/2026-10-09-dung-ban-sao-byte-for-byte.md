---
id: 2026-10-09-dung-ban-sao-byte-for-byte
date: 2026-10-09
repo: repo
status: raw
signals: []
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [outsider]
lines: ["omp:cd4449ab#L1463", "omp:cd4449ab#L1493", "omp:cd4449ab#L1495", "omp:cd4449ab#L1613"]
hook: "Fixture là bản sao nguyên byte của hub đang chạy, không tự bịa"
tension: none
sides: []
strength: 0
stakes: 2
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Dùng bản sao byte-for-byte của dữ liệu thật từ hub đang chạy làm fixture test, thay vì tự viết fixture giả.

**Chuyện gì xảy ra:** Dùng bản sao byte-for-byte của dữ liệu thật từ hub đang chạy làm fixture test, thay vì tự viết fixture giả.
**Góc người ngoài:** cách làm phổ biến là Hầu hết dev tự viết fixture nhỏ, gọn cho test, rồi chỉ kiểm tra dữ liệu thật lúc chạy thử thủ công; ở đây khác ở Agent chép đúng các file thật (chỉ đọc, không chép file không cần) rồi viết test chạy toàn bộ đường v1→v2→v3 trên đó. Nhờ vậy lỗi chỉ lộ ra với dữ liệu thật mới bị bắt trong test, không phải lúc lead chạy thử. Người đọc sẽ hỏi: làm sao biết file nào cần chép, và có an toàn khi copy dữ liệu sản xuất vào repo không?.
