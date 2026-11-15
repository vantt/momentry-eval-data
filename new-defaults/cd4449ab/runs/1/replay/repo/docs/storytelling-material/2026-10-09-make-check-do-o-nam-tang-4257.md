---
id: 2026-10-09-make-check-do-o-nam-tang-4257
code: M-QMY2
aliases: [M-QMY2]
date: 2026-10-09
repo: repo
status: raw
signals: []
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest, outsider]
lines: ["omp:cd4449ab#L1314", "omp:cd4449ab#L1320", "omp:cd4449ab#L1335", "omp:cd4449ab#L1842", "omp:cd4449ab#L2094", "omp:cd4449ab#L2267", "omp:cd4449ab#L2812", "omp:cd4449ab#L2818", "omp:cd4449ab#L2827", "omp:cd4449ab#L2941", "omp:cd4449ab#L3118", "omp:cd4449ab#L3124", "omp:cd4449ab#L3151", "omp:cd4449ab#L3166", "omp:cd4449ab#L3175", "omp:cd4449ab#L3935", "omp:cd4449ab#L3941"]
hook: "make check đỏ 17 lần, mỗi lần một tầng lỗi khác"
tension: none
sides: []
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# make check đỏ ở năm tầng khác nhau, 17 lần trong một phiên

**Bối cảnh:** Gate của dự án gồm fmt-check, vet, golangci-lint và go test. Mỗi commit phải xanh trước khi đi tiếp.
**Chuyện gì xảy ra:** Lỗi đỏ luân phiên: fmt, lint, test, vet, rồi lint. Phần lớn lỗi fmt sửa bằng make fmt. Lint chỉ báo issue mới so với origin/main. Test đỏ thường do fixture chưa cập nhật. Đếm được 17 lần make check đỏ trước khi các commit xanh.
**Bài học:** Chạy gofmt và go vet nhanh trước khi chạy gate đầy đủ để rút ngắn vòng sửa.
**Artefact:** Biểu đồ tầng lỗi theo thứ tự thời gian (fmt, lint, test, vet). Không cần che.
**Góc người ngoài:** cách làm phổ biến là Hầu hết người làm một mình sửa khi thấy lỗi, không ghi nhận hàng loạt lỗi như vậy; ở đây khác ở Ghi chú này chưa đủ để nói là bất thường. Điểm đáng chú ý là nhiều lần chạy dài và không có công cụ nào ngăn lỗi lan. Hướng mà người đọc có thể quan tâm là cách rút gọn lượt chạy này.
