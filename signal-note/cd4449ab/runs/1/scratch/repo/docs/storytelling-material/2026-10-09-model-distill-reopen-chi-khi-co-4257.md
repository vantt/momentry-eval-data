---
id: 2026-10-09-model-distill-reopen-chi-khi-co-4257
code: M-39GW
aliases: [M-39GW]
date: 2026-10-09
repo: repo
status: raw
signals: [dao_quyet_dinh]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L1961", "omp:cd4449ab#L1964", "omp:cd4449ab#L1966", "omp:cd4449ab#L1969", "omp:cd4449ab#L1970", "omp:cd4449ab#L1972", "omp:cd4449ab#L1982", "omp:cd4449ab#L1984", "omp:cd4449ab#L1987", "omp:cd4449ab#L2000", "omp:cd4449ab#L2002", "omp:cd4449ab#L3551", "omp:cd4449ab#L3553", "omp:cd4449ab#L3589"]
hook: "Xoá hai route cũ, test web đỏ thêm một lần"
tension: khac
sides: ["quy tắc: chỉ mở lại khi có bằng chứng mới", "xoá route làm test web vỡ"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Model distill: reopen chỉ khi có bằng chứng mới

**Bối cảnh:** Model distill mới quy định lesson đã quyết định sẽ không mở lại nếu không có bằng chứng mới.
**Chuyện gì xảy ra:** Viết model mới; test đầu đỏ, sửa phần kiểm tra quyết định cũ. Quy tắc cuối: chỉ mở lại khi có bằng chứng mới chưa có trong SeenWhere. Sau đó xoá routes insights và runs, test web đỏ thêm một lần, rồi viết lại route distill và xanh.
**Bài học:** Quy tắc 'mở lại khi có bằng chứng mới' phải được test cả trường hợp không có bằng chứng mới, không chỉ trường hợp có.
**Artefact:** Bảng quyết định trước/sau cho một lesson mẫu, che nội dung.
