---
id: 2026-10-09-make-check-do-17-lan-vi
date: 2026-10-09
repo: repo
status: raw
signals: [số trước sau, người duyệt]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L1312", "omp:cd4449ab#L1314", "omp:cd4449ab#L1318", "omp:cd4449ab#L1320", "omp:cd4449ab#L1335", "omp:cd4449ab#L2094", "omp:cd4449ab#L2267", "omp:cd4449ab#L3118", "omp:cd4449ab#L3941"]
hook: "make check đỏ 17 lần, phần lớn chỉ vì quên format"
tension: nho_ma_to
sides: ["lỗi format nhỏ xíu", "17 lần đỏ, mất nhiều phút chờ lint"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# make check đỏ 17 lần vì fmt, lint, vet, test

**Bối cảnh:** make check gồm fmt-check, vet, lint và test. Mỗi commit phải xanh trước khi commit.
**Chuyện gì xảy ra:** Trong Phase 4 và 3, make check đỏ khoảng 17 lần: thường là fmt-check (chạy make fmt rồi chạy lại), sau đó là lint, vet và test. Mỗi lần đỏ kéo theo một vòng sửa ngắn nhưng cộng lại thành nhiều phút chờ lint vì golangci-lint được go run lại mỗi lần.
**Bài học:** Chạy make fmt trước mỗi lần make check để loại lỗi định dạng sớm, đừng để nó chiếm một vòng.
**Artefact:** Bảng số lần make check xanh/đỏ theo commit.
