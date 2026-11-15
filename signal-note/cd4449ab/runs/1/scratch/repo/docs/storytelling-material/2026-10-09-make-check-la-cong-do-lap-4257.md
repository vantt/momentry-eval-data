---
id: 2026-10-09-make-check-la-cong-do-lap-4257
code: M-YVWJ
aliases: [M-YVWJ]
date: 2026-10-09
repo: repo
status: raw
signals: [khac]
signal_note: "Sự cố vặt lặp lại ở mỗi đợt commit, nhưng cho thấy nhịp làm việc có cổng kiểm tra; có thể dùng làm bài về kỷ luật xanh trước commit."
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L1314", "omp:cd4449ab#L1315", "omp:cd4449ab#L1320", "omp:cd4449ab#L1335", "omp:cd4449ab#L1338", "omp:cd4449ab#L1341", "omp:cd4449ab#L1842", "omp:cd4449ab#L2094", "omp:cd4449ab#L2097", "omp:cd4449ab#L2267", "omp:cd4449ab#L2812", "omp:cd4449ab#L2813", "omp:cd4449ab#L2818", "omp:cd4449ab#L2827", "omp:cd4449ab#L2941", "omp:cd4449ab#L3118", "omp:cd4449ab#L3121", "omp:cd4449ab#L3124", "omp:cd4449ab#L3151", "omp:cd4449ab#L3166", "omp:cd4449ab#L3175", "omp:cd4449ab#L3433", "omp:cd4449ab#L3935", "omp:cd4449ab#L3938", "omp:cd4449ab#L3941"]
hook: "Cổng kiểm tra đỏ 15 lần, không bỏ qua lần nào"
tension: chon_mot_mat_mot
sides: ["15 lần đỏ làm chậm tiến độ", "không bước nào bị bỏ qua"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# make check là cổng: đỏ lặp lại

**Bối cảnh:** Mỗi commit đều chạy make check: gofmt, go vet, golangci-lint qua go run, và go test.
**Chuyện gì xảy ra:** Trong các đợt commit, make check đỏ khoảng 15 lần: fmt đỏ 6 lần (sửa bằng make fmt), lint và vet mỗi loại vài lần, test vài lần. Lint chỉ báo lỗi trên code mới so với origin/main. Mỗi lần đỏ đều sửa rồi chạy lại, không bỏ qua bước nào.
**Bài học:** Với cổng nhiều bước, nên chạy bước rẻ nhất trước (fmt) để không chờ lint mới biết sai.
**Artefact:** Bảng đếm lỗi theo bước của make check qua các lần chạy.
