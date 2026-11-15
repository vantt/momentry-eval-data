---
id: 2026-10-09-goi-binary-chua-build-qua-python
date: 2026-10-09
repo: repo
status: raw
signals: [khác]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L1071", "omp:cd4449ab#L1074", "omp:cd4449ab#L1075", "omp:cd4449ab#L1077"]
hook: "Gọi binary chưa build, mất trọn một vòng test"
tension: nho_ma_to
sides: ["Quên build một binary", "Mất cả một vòng test"]
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Gọi binary chưa build qua python eval: FileNotFoundError

**Bối cảnh:** Muốn scan workspace overlay bằng CLI để xem output, agent gọi ./bin/skillhub từ Python.
**Chuyện gì xảy ra:** Binary không tồn tại trong thư mục repo nên subprocess báo FileNotFoundError. Phải build trước, hoặc dùng go run. Lỗi nhỏ nhưng làm mất một vòng test. Sau đó test evaluation chuyển sang gọi hàm Run trực tiếp.
**Bài học:** Trong test, gọi CLI qua hàm Run của package thay vì subprocess tới binary chưa chắc tồn tại.
**Artefact:** Không cần.
