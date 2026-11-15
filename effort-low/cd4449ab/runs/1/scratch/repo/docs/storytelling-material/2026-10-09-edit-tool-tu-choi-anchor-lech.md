---
id: 2026-10-09-edit-tool-tu-choi-anchor-lech
date: 2026-10-09
repo: repo
status: raw
signals: [số trước sau]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L240", "omp:cd4449ab#L657", "omp:cd4449ab#L1005", "omp:cd4449ab#L1110", "omp:cd4449ab#L1167", "omp:cd4449ab#L1579", "omp:cd4449ab#L1951", "omp:cd4449ab#L2192", "omp:cd4449ab#L2644", "omp:cd4449ab#L2668", "omp:cd4449ab#L2680", "omp:cd4449ab#L3130", "omp:cd4449ab#L3725", "omp:cd4449ab#L3818"]
hook: "Edit bị từ chối 15 lần chỉ vì số dòng lệch"
tension: nho_ma_to
sides: ["anchor lệch vài dòng", "15 lần đọc lại rồi gửi lại"]
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Edit tool từ chối anchor lệch 15 lần, mỗi lần đọc lại

**Bối cảnh:** Công cụ edit yêu cầu anchor khớp đúng nội dung đã đọc gần nhất.
**Chuyện gì xảy ra:** Ít nhất 14 lần edit bị từ chối vì số dòng hoặc anchor lệch sau khi file đổi. Mỗi lần agent phải đọc lại vùng liên quan rồi gửi lại edit. Hầu hết đều thành công ở lần thứ hai.
**Bài học:** Sau mỗi lần sửa nhiều chỗ trong một file, đọc lại đúng vùng trước khi edit tiếp để giảm vòng lặp.
**Artefact:** Bảng số lần edit bị từ chối theo file.
