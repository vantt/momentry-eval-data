---
id: 2026-10-09-truoc-khi-them-truong-moi-vao-4257
code: M-SER4
aliases: [M-SER4]
date: 2026-10-09
repo: repo
status: raw
signals: []
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [outsider]
lines: ["omp:cd4449ab#L2124", "omp:cd4449ab#L2319", "omp:cd4449ab#L2321"]
hook: "Trước khi thêm trường mới, grep hết mọi chỗ còn ghi file cũ"
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

# Trước khi thêm trường mới vào schema hay migration, agent đọc toàn bộ grep và struct liên quan, rồi tìm kiếm có hệ thống các điểm ghi file cũ bằng grep theo tên file, loại trừ test và các đường đọc fallback.

**Chuyện gì xảy ra:** Trước khi thêm trường mới vào schema hay migration, agent đọc toàn bộ grep và struct liên quan, rồi tìm kiếm có hệ thống các điểm ghi file cũ bằng grep theo tên file, loại trừ test và các đường đọc fallback.
**Góc người ngoài:** cách làm phổ biến là Người ta hay sửa theo những chỗ nhớ được hoặc chỉ tìm trong file đang mở; ở đây khác ở Lệnh grep sweep kiểu `grep -rn ... | grep -v _test` là cách kiểm tra xem còn chỗ nào ghi định dạng cũ hay không. Người đọc sẽ muốn biết cách nhận diện và khoanh vùng từng chỗ ghi đó.
