---
id: 2026-10-09-cong-cu-sua-file-neo-dong-4257
code: M-R8V5
aliases: [M-R8V5]
date: 2026-10-09
repo: repo
status: raw
signals: [khac]
signal_note: "Công cụ sửa file từ chối vì số dòng neo không khớp hơn chục lần, mỗi lần phải đọc lại đoạn file."
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L240", "omp:cd4449ab#L657", "omp:cd4449ab#L885", "omp:cd4449ab#L1005", "omp:cd4449ab#L1110", "omp:cd4449ab#L1167", "omp:cd4449ab#L1579", "omp:cd4449ab#L1951", "omp:cd4449ab#L2192", "omp:cd4449ab#L2644", "omp:cd4449ab#L2668", "omp:cd4449ab#L2678", "omp:cd4449ab#L3130", "omp:cd4449ab#L3725", "omp:cd4449ab#L3818"]
hook: "15 lần lệnh sửa file bị từ chối vì neo lệch một dòng"
tension: nho_ma_to
sides: ["Chỉ lệch neo dòng, một chi tiết rất nhỏ", "Khoảng 15 lần lệnh bị từ chối, phải đọc lại file"]
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Công cụ sửa file neo dòng sai, phải đọc lại

**Bối cảnh:** Công cụ sửa file yêu cầu neo đúng dòng hiện tại của file, mà file đã đổi sau nhiều lần sửa.
**Chuyện gì xảy ra:** Khoảng 15 lần lệnh sửa bị từ chối do neo dòng không khớp. Mỗi lần agent phải đọc lại đoạn file rồi phát hành lại lệnh sửa với neo mới.
**Bài học:** Đọc đúng đoạn cần sửa ngay trước khi sửa; neo dòng cũ là nguồn lỗi lặp lại.
**Artefact:** Không có artefact đáng chụp.
