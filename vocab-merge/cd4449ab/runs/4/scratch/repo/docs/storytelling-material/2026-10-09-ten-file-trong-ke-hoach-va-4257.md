---
id: 2026-10-09-ten-file-trong-ke-hoach-va-4257
code: M-PBXJ
aliases: [M-PBXJ]
date: 2026-10-09
repo: repo
status: raw
signals: [khác]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L276", "omp:cd4449ab#L2380", "omp:cd4449ab#L2401", "omp:cd4449ab#L2419", "omp:cd4449ab#L2470", "omp:cd4449ab#L3457"]
hook: "Kế hoạch ghi tên file, nhưng 4 file đều không tồn tại"
tension: tuong_ma_hoa_ra
sides: ["kế hoạch ghi rõ tên file", "4 tên đều sai, phải glob mới thấy"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Tên file trong kế hoạch và trong đầu agent đều sai

**Bối cảnh:** Kế hoạch Phase 3 nhắc các file cần xoá hoặc sửa, nhiều file không còn ở đường dẫn đó.
**Chuyện gì xảy ra:** Nhiều lần đọc file theo tên trong kế hoạch hoặc đoán đều thất bại: apply.go, distill.go, insight/insight.go, curation_run_tools.go. Phải dùng glob để tìm tên thật. Thư mục sources/intake và runtime/sources cũng không có trên hub. Mỗi lần sai mất một lượt đọc.
**Bài học:** Với kế hoạch lâu đời, glob đường dẫn trước khi tin tên file. Coi kế hoạch là gợi ý, không phải danh sách file tồn tại.
**Artefact:** Bảng so sánh kế hoạch nói gì với repo thật. Không cần ảnh.
