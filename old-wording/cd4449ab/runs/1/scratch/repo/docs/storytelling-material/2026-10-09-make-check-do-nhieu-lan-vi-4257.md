---
id: 2026-10-09-make-check-do-nhieu-lan-vi-4257
code: M-09TA
aliases: [M-09TA]
date: 2026-10-09
repo: repo
status: raw
signals: [khac]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L1312", "omp:cd4449ab#L1314", "omp:cd4449ab#L1315", "omp:cd4449ab#L1318", "omp:cd4449ab#L1320", "omp:cd4449ab#L1335", "omp:cd4449ab#L1336", "omp:cd4449ab#L2092", "omp:cd4449ab#L2094", "omp:cd4449ab#L2812", "omp:cd4449ab#L2813", "omp:cd4449ab#L3935", "omp:cd4449ab#L3936"]
hook: "Sáu lần check đỏ chỉ vì quên chạy make fmt"
tension: nho_ma_to
sides: ["Lỗi chỉ là định dạng code", "Làm check đỏ khoảng sáu lần"]
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# make check đỏ nhiều lần vì gofmt và lint, phải chạy make fmt trước

**Bối cảnh:** make check là cổng bắt buộc trước khi commit. Nó đỏ nhiều lần ở bước fmt-check và một vài lần ở bước lint.
**Chuyện gì xảy ra:** Mỗi lần thêm file hoặc sửa struct, gofmt lại không được chạy. Phần lớn lần đỏ ở fmt-check, sửa bằng make fmt rồi mới sang lint. Lint chạy với --new-from-rev=origin/main nên chỉ bắt lỗi trong code mới. Tổng cộng khoảng sáu lần fmt-check đỏ.
**Bài học:** Chạy formatter trước khi chạy cổng, và đặt make fmt là bước đầu của vòng lặp.
**Artefact:** Không có.
