---
id: 2026-10-09-file-distill-1184-dong-that-42-4257
code: M-9ZJ9
aliases: [M-9ZJ9]
date: 2026-10-09
repo: repo
status: raw
signals: []
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L2414", "omp:cd4449ab#L2416", "omp:cd4449ab#L2419", "omp:cd4449ab#L2440", "omp:cd4449ab#L2456", "omp:cd4449ab#L2458", "omp:cd4449ab#L2461", "omp:cd4449ab#L2491", "omp:cd4449ab#L2513", "omp:cd4449ab#L2515", "omp:cd4449ab#L2518", "omp:cd4449ab#L2521", "omp:cd4449ab#L2524", "omp:cd4449ab#L2527"]
hook: "File 1184 dòng: 77 SHA rút gọn, nở đủ 40 ký tự"
tension: none
sides: []
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# File distill 1184 dòng thật: 42 lesson, 77 SHA rút gọn

**Bối cảnh:** Trước khi viết converter Phase 0 sang D7 cho distill, phải hiểu dữ liệu thật của hub.
**Chuyện gì xảy ra:** File có 1184 dòng, 46161 byte, 42 lesson và 2 cursor, với 5 và 7 commit mỗi repo. Có 77 mục where dùng SHA rút gọn 7 đến 12 ký tự, và đã nở ra đủ 40 ký tự qua git rev-parse trên mirror. Không có key lỗi, không trùng key, nhưng 39 lesson ở trạng thái candidate và 3 ở planned. Thư mục runtime/sources không có trên hub, dữ liệu nguồn nằm ở mirror của distill-lab.
**Bài học:** Kiểm tra invariant trên dữ liệu thật trước khi viết converter: khóa trùng, SHA rút gọn, trạng thái.
**Artefact:** Bảng đếm lesson theo trạng thái và SHA rút gọn trước và sau khi nở. Che nội dung lesson.
