---
id: 2026-10-09-doan-sai-duong-dan-va-lenh
date: 2026-10-09
repo: repo
status: raw
signals: [khác]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L276", "omp:cd4449ab#L2380", "omp:cd4449ab#L2401", "omp:cd4449ab#L2419", "omp:cd4449ab#L2470", "omp:cd4449ab#L2722"]
hook: "Agent đoán sai đường dẫn file nhiều lần, mỗi lần mất một lượt"
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

# Đoán sai đường dẫn và lệnh: lỗi vặt của agent trong lúc khảo sát

**Bối cảnh:** Khảo sát code và dữ liệu thật trước khi viết.
**Chuyện gì xảy ra:** Agent đoán sai đường dẫn nhiều lần, ví dụ apply.go, distill.go, insight.go và thư mục runtime/sources của hub, và chạy go run -e với cú pháp sai. Mỗi lỗi chỉ tốn một lượt nhưng làm chậm nhịp làm việc.
**Bài học:** Dùng glob và grep để tìm tên trước khi đọc. Trong repo lớn, đừng đoán đường dẫn.
**Artefact:** Không cần chụp.
