---
id: 2026-10-09-so-sanh-dau-ra-that-cua-4257
code: M-GKR1
aliases: [M-GKR1]
date: 2026-10-09
repo: repo
status: raw
signals: []
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, outsider]
lines: ["omp:cd4449ab#L1713", "omp:cd4449ab#L1870", "omp:cd4449ab#L1879", "omp:cd4449ab#L1888", "omp:cd4449ab#L1890"]
hook: "Chạy cả binary cũ lẫn mới trên dữ liệu thật rồi diff"
tension: none
sides: []
strength: 1
stakes: 2
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# So sánh đầu ra thật của sản phẩm trước và sau thay đổi: chạy binary cũ và binary mới trên hai bản clone mới của dữ liệu thật, rồi diff từng trường của lệnh 'skill show --json'.

**Chuyện gì xảy ra:** So sánh đầu ra thật của sản phẩm trước và sau thay đổi: chạy binary cũ và binary mới trên hai bản clone mới của dữ liệu thật, rồi diff từng trường của lệnh 'skill show --json'.
**Góc người ngoài:** cách làm phổ biến là Chỉ dựa vào unit test và test tích hợp trong repo, không so output thật trên dữ liệu thật; ở đây khác ở Cách này bắt được regression mà test xanh bỏ sót (mô tả bị thành '>-', tên đổi thứ tự). Người đọc sẽ muốn có kiểu kiểm tra 'before/after trên dữ liệu thật' cho các thay đổi làm đổi đầu ra cho người dùng.
