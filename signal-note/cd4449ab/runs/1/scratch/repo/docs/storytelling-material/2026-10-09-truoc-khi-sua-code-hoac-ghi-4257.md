---
id: 2026-10-09-truoc-khi-sua-code-hoac-ghi-4257
code: M-P837
aliases: [M-P837]
date: 2026-10-09
repo: repo
status: raw
signals: []
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [outsider]
lines: ["omp:cd4449ab#L2414", "omp:cd4449ab#L2416", "omp:cd4449ab#L2456", "omp:cd4449ab#L2513", "omp:cd4449ab#L2516", "omp:cd4449ab#L2519", "omp:cd4449ab#L2522", "omp:cd4449ab#L2525"]
hook: "Trước khi viết một dòng code, agent đếm key sai và key trùng"
tension: it_ma_nhieu
sides: ["người ta đọc mẫu bằng mắt rồi đoán", "một script đếm dữ liệu thật trước khi thiết kế"]
strength: 2
stakes: 1
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Trước khi sửa code hoặc ghi migration, agent kiểm tra dữ liệu thật bằng script: parse YAML, đếm key sai và key trùng, kiểm tra trường rỗng, đếm read/not_read theo nguồn, rồi mới thiết kế schema.

**Chuyện gì xảy ra:** Trước khi sửa code hoặc ghi migration, agent kiểm tra dữ liệu thật bằng script: parse YAML, đếm key sai và key trùng, kiểm tra trường rỗng, đếm read/not_read theo nguồn, rồi mới thiết kế schema.
**Góc người ngoài:** cách làm phổ biến là Đa số người đọc file mẫu bằng mắt hoặc suy đoán cấu trúc từ tài liệu, rồi viết code theo giả định đó; ở đây khác ở Giả định về dữ liệu được đo trên dữ liệu thật trước khi viết, nên các lỗi cấu trúc được phát hiện sớm thay vì sau khi migrate.
