---
id: 2026-10-09-make-check-do-17-lan-trong
date: 2026-10-09
repo: repo
status: raw
signals: []
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L1314", "omp:cd4449ab#L1320", "omp:cd4449ab#L1335", "omp:cd4449ab#L1842", "omp:cd4449ab#L2094", "omp:cd4449ab#L2267", "omp:cd4449ab#L2812", "omp:cd4449ab#L2818", "omp:cd4449ab#L2827", "omp:cd4449ab#L2941", "omp:cd4449ab#L3118", "omp:cd4449ab#L3124", "omp:cd4449ab#L3151", "omp:cd4449ab#L3166", "omp:cd4449ab#L3175", "omp:cd4449ab#L3935", "omp:cd4449ab#L3941"]
hook: "Cổng chặn lỗi chặn 17 lần, phần lớn chỉ vì thiếu format"
tension: nho_ma_to
sides: ["Cổng kiểm tra bắt lỗi commit", "Phần lớn chỉ là lỗi định dạng, tốn thêm vòng"]
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# make check đỏ 17 lần trong một wave

**Bối cảnh:** make check chạy fmt-check, vet, lint và test; là cổng xanh bắt buộc trước mỗi commit.
**Chuyện gì xảy ra:** Trong wave có 17 lần make check thoát khác 0: 6 lần fmt-check, 4 lần lint, 2 lần vet, 3 lần test, 2 lần chưa rõ loại. Phần lớn sửa bằng make fmt rồi chạy lại. Cổng này chặn được commit lỗi nhưng mỗi vòng thêm thời gian.
**Bài học:** Chạy make fmt trước make check, và đếm loại lỗi để thấy lỗi lặp lại ở đâu.
**Artefact:** Bảng 17 lần đỏ theo loại (fmt, lint, vet, test).
