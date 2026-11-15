---
id: 2026-10-09-cong-cu-sua-file-tu-choi-4257
code: M-TYN9
aliases: [M-TYN9]
date: 2026-10-09
repo: repo
status: raw
signals: [khac]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L240", "omp:cd4449ab#L657", "omp:cd4449ab#L885", "omp:cd4449ab#L1110", "omp:cd4449ab#L1579", "omp:cd4449ab#L1951", "omp:cd4449ab#L2192", "omp:cd4449ab#L2680", "omp:cd4449ab#L3725", "omp:cd4449ab#L3818"]
hook: "Công cụ sửa file từ chối khoảng 15 lần vì lệch số dòng"
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

# Công cụ sửa file từ chối khoảng 15 lần vì số dòng không khớp

**Bối cảnh:** Công cụ sửa file yêu cầu đúng path và tag cùng số dòng vừa đọc. Khi file đã đổi do lần sửa trước, lệnh bị từ chối.
**Chuyện gì xảy ra:** Đa số lỗi là dòng không hiển thị hoặc neo không khớp. Thông báo gợi ý đọc lại đúng vùng rồi gửi lại. Mỗi lỗi tốn thêm một lượt đọc, và cả phiên có khoảng 15 lần như vậy.
**Bài học:** Khi công cụ sửa theo số dòng, hãy đọc lại đúng vùng ngay trước khi sửa thay vì dựa vào lần đọc cũ.
**Artefact:** Không có.
