---
id: 2026-10-09-profile-du-lieu-that-bang-script
date: 2026-10-09
repo: repo
status: raw
signals: []
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [outsider]
lines: ["omp:cd4449ab#L2414", "omp:cd4449ab#L2416", "omp:cd4449ab#L2456", "omp:cd4449ab#L2458", "omp:cd4449ab#L2513", "omp:cd4449ab#L2516", "omp:cd4449ab#L2519", "omp:cd4449ab#L2522", "omp:cd4449ab#L2525", "omp:cd4449ab#L2527"]
hook: "Đếm dữ liệu thật trước, rồi mới viết dòng migration đầu tiên"
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

# Profile dữ liệu thật bằng script trước khi viết code migration: đếm số bài học, kiểm tra regex key, trùng key, trường rỗng, phân bố trạng thái, độ phủ theo nguồn.

**Chuyện gì xảy ra:** Profile dữ liệu thật bằng script trước khi viết code migration: đếm số bài học, kiểm tra regex key, trùng key, trường rỗng, phân bố trạng thái, độ phủ theo nguồn.
**Góc người ngoài:** cách làm phổ biến là Dev thường đọc vài dòng đầu của file, đoán cấu trúc, rồi sửa khi test đỏ; ở đây khác ở Agent đo file 1184 dòng bằng vài lệnh Python ngắn để biết trước dữ liệu có bao nhiêu trường hợp lạ. Cách này cho ra số liệu (42 bài học, 39 ở trạng thái candidate, 0 key lỗi) để quyết định thiết kế. Người đọc muốn biết cách tự làm tương tự với dữ liệu của mình.
