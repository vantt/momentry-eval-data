---
id: 2026-10-09-kiem-chung-migration-tren-mot-ban-4257
code: M-0MCH
aliases: [M-0MCH]
date: 2026-10-09
repo: repo
status: raw
signals: []
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [outsider]
lines: ["omp:cd4449ab#L1463", "omp:cd4449ab#L1828", "omp:cd4449ab#L1870", "omp:cd4449ab#L1882", "omp:cd4449ab#L1885", "omp:cd4449ab#L1888", "omp:cd4449ab#L1891"]
hook: "Chạy binary cũ và mới trên bản clone hub thật rồi diff JSON"
tension: none
sides: []
strength: 0
stakes: 3
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Kiểm chứng migration trên một bản clone của dữ liệu hub thật, chạy binary cũ và binary mới, rồi diff output JSON của `skill show` trước và sau. Sau đó xoá thư mục tạm.

**Chuyện gì xảy ra:** Kiểm chứng migration trên một bản clone của dữ liệu hub thật, chạy binary cũ và binary mới, rồi diff output JSON của `skill show` trước và sau. Sau đó xoá thư mục tạm.
**Góc người ngoài:** cách làm phổ biến là Thường người ta chỉ chạy test với fixture tự viết, hoặc xem bằng mắt xem output có vẻ đúng không; ở đây khác ở So sánh hai binary trên cùng một dữ liệu thật bằng diff cấu trúc là cách bắt được hồi quy âm thầm, như mô tả sai description hay đổi thứ tự name. Người đọc muốn biết cách làm và cách dọn sau đó.
