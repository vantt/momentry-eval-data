---
id: 2026-10-09-truoc-khi-dua-ra-ket-luan-4257
code: M-Y60R
aliases: [M-Y60R]
date: 2026-10-09
repo: repo
status: raw
signals: []
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [outsider]
lines: ["omp:cd4449ab#L1713", "omp:cd4449ab#L1828", "omp:cd4449ab#L1870", "omp:cd4449ab#L1885", "omp:cd4449ab#L1888", "omp:cd4449ab#L1890"]
hook: "Chạy binary cũ và mới trên cùng dữ liệu, rồi diff từng trường"
tension: tuong_ma_hoa_ra
sides: ["tin test đã viết là đủ", "diff hai binary mới lộ chỗ lệch"]
strength: 2
stakes: 1
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Trước khi đưa ra kết luận, agent đối chiếu hai thứ: đầu ra của binary cũ (từ main) và binary mới trên cùng một bản sao dữ liệu, rồi diff từng trường như name, description, status.

**Chuyện gì xảy ra:** Trước khi đưa ra kết luận, agent đối chiếu hai thứ: đầu ra của binary cũ (từ main) và binary mới trên cùng một bản sao dữ liệu, rồi diff từng trường như name, description, status.
**Góc người ngoài:** cách làm phổ biến là Người ta thường chỉ chạy binary mới và kiểm tra vài trường mong đợi, hoặc tin vào test đã viết; ở đây khác ở Đối chiếu trước/sau trên đầu ra thật bắt được lỗi hồi quy mà test không thấy. Người đọc sẽ hỏi cách làm này có áp dụng được cho việc của họ không.
