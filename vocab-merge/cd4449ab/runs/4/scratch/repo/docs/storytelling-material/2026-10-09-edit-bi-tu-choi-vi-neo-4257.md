---
id: 2026-10-09-edit-bi-tu-choi-vi-neo-4257
code: M-Q6BM
aliases: [M-Q6BM]
date: 2026-10-09
repo: repo
status: raw
signals: [khác]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L240", "omp:cd4449ab#L657", "omp:cd4449ab#L885", "omp:cd4449ab#L1005", "omp:cd4449ab#L1110", "omp:cd4449ab#L1167", "omp:cd4449ab#L1579", "omp:cd4449ab#L1951", "omp:cd4449ab#L2192", "omp:cd4449ab#L2642", "omp:cd4449ab#L2668", "omp:cd4449ab#L2678", "omp:cd4449ab#L2680", "omp:cd4449ab#L3130", "omp:cd4449ab#L3725", "omp:cd4449ab#L3818"]
hook: "15 lần edit bị từ chối, không lần nào phải đổi logic"
tension: none
sides: []
strength: 0
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Edit bị từ chối vì neo dòng cũ: khoảng 15 lần phải đọc lại

**Bối cảnh:** Công cụ edit yêu cầu neo theo số dòng và tag path. Sau mỗi lần sửa, số dòng đổi nên neo cũ không còn khớp.
**Chuyện gì xảy ra:** Khoảng 15 lần edit bị từ chối: sai cú pháp PUT, neo dòng không khớp nội dung đã hiển thị, hoặc thiếu boundary row. Cách xử lý ổn định là đọc lại đúng vùng rồi issue lại với neo mới. Không lần nào phải đổi logic để vượt qua.
**Bài học:** Đọc lại vùng cần sửa ngay trước khi edit, vì neo dòng sống rất ngắn khi file đang đổi nhiều.
**Artefact:** Không cần ảnh. Có thể viết ví dụ một lỗi neo và cách sửa.
