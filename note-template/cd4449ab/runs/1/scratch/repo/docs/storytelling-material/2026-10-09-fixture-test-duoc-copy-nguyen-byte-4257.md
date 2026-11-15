---
id: 2026-10-09-fixture-test-duoc-copy-nguyen-byte-4257
code: M-FC23
aliases: [M-FC23]
date: 2026-10-09
repo: repo
status: raw
signals: []
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [outsider]
lines: ["omp:cd4449ab#L1462", "omp:cd4449ab#L1679", "omp:cd4449ab#L1828", "omp:cd4449ab#L1837"]
hook: "Fixture copy nguyên byte từ hub thật, không viết tay cho gọn"
tension: tuong_ma_hoa_ra
sides: ["Viết mẫu tay cho gọn, đoán cấu trúc dữ liệu", "Copy nguyên byte dữ liệu thật để test đúng thực tế"]
strength: 1
stakes: 2
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Fixture test được copy nguyên byte từ file dữ liệu thật của hub (chỉ đọc, trong thư mục scratch), thay vì viết tay một mẫu đơn giản.

**Chuyện gì xảy ra:** Fixture test được copy nguyên byte từ file dữ liệu thật của hub (chỉ đọc, trong thư mục scratch), thay vì viết tay một mẫu đơn giản.
**Góc người ngoài:** cách làm phổ biến là Viết fixture tay cho gọn, đoán cấu trúc dữ liệu thật rồi test trên đó; ở đây khác ở Fixture viết tay đã làm test qua mà hub thật vẫn hỏng. Bản copy thật buộc test phải đi qua đúng định dạng người dùng đang có. Người đọc sẽ hỏi cách copy an toàn: không ghi vào nguồn, không chạy migrate lên dữ liệu gốc.
