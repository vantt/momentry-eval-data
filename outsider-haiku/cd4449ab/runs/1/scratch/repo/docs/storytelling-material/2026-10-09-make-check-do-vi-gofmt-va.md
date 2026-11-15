---
id: 2026-10-09-make-check-do-vi-gofmt-va
date: 2026-10-09
repo: repo
status: raw
signals: [khác]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L1312", "omp:cd4449ab#L1314", "omp:cd4449ab#L1315", "omp:cd4449ab#L1317", "omp:cd4449ab#L1320", "omp:cd4449ab#L1335", "omp:cd4449ab#L1338", "omp:cd4449ab#L2092", "omp:cd4449ab#L2094", "omp:cd4449ab#L2097", "omp:cd4449ab#L2810", "omp:cd4449ab#L2812", "omp:cd4449ab#L2815", "omp:cd4449ab#L3118", "omp:cd4449ab#L3121", "omp:cd4449ab#L3151", "omp:cd4449ab#L3935", "omp:cd4449ab#L3941"]
hook: "Hơn 20 lần make check đỏ, nhưng không phải vì test"
tension: tuong_ma_hoa_ra
sides: ["tưởng build đỏ là do test hỏng", "thật ra chỉ là gofmt và lint"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# make check đỏ vì gofmt và lint: chạy fmt trước rồi mới kiểm

**Bối cảnh:** make check gồm fmt-check, vet, lint và test. Lint dùng golangci-lint với --new-from-rev origin/main.
**Chuyện gì xảy ra:** Phần lớn các lần make check đỏ là do gofmt hoặc lint, không phải test. Agent chạy make fmt rồi kiểm lại, lặp hơn 20 lần trong phiên. Lint chỉ bắt lỗi trong phần diff so với origin/main.
**Bài học:** Chạy fmt trước khi chạy gate. Đọc dòng lỗi đầu tiên để biết cổng nào đang đỏ.
**Artefact:** Không cần chụp. Mô tả bốn cổng của make check là đủ.
