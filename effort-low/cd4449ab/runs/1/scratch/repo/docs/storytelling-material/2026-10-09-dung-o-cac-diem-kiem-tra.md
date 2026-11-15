---
id: 2026-10-09-dung-o-cac-diem-kiem-tra
date: 2026-10-09
repo: repo
status: raw
signals: []
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [outsider]
lines: ["omp:cd4449ab#L2122", "omp:cd4449ab#L2344", "omp:cd4449ab#L2373", "omp:cd4449ab#L2374"]
hook: "Agent dừng ở mỗi điểm kiểm tra, báo hash rồi chờ"
tension: none
sides: []
strength: 0
stakes: 1
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Dừng ở các điểm kiểm tra do người điều phối đặt ra, báo hash commit, rồi chờ xác nhận trước khi làm bước tiếp.

**Chuyện gì xảy ra:** Dừng ở các điểm kiểm tra do người điều phối đặt ra, báo hash commit, rồi chờ xác nhận trước khi làm bước tiếp.
**Góc người ngoài:** cách làm phổ biến là Agent thường tự chạy tiếp đến hết nhiệm vụ, chỉ dừng khi gặp lỗi; ở đây khác ở Ở mỗi checkpoint, agent dừng, báo hash và trạng thái guard, rồi chờ người điều phối merge. Sau đó mới rebase lên main và làm tiếp. Người đọc sẽ hỏi cách chia công việc nhiều agent song song mà không đụng nhau như vậy.
