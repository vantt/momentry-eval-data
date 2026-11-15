---
id: 2026-10-09-clone-hub-khong-co-runtime-catalog
date: 2026-10-09
repo: repo
status: raw
signals: []
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L1872", "omp:cd4449ab#L1873", "omp:cd4449ab#L1875", "omp:cd4449ab#L1876", "omp:cd4449ab#L1878", "omp:cd4449ab#L1879", "omp:cd4449ab#L1881", "omp:cd4449ab#L1882", "omp:cd4449ab#L1884", "omp:cd4449ab#L1885", "omp:cd4449ab#L1888"]
hook: "Clone dữ liệu thật thiếu đúng một file, lệnh đọc chết ngay"
tension: nho_ma_to
sides: ["Bản clone thiếu một file con trỏ", "Lệnh show không chạy được, phải dựng workspace tay"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Clone hub không có runtime catalog nên diff skill show chết lúc đầu

**Bối cảnh:** Để diff skill show trước và sau migrate, cần chạy binary cũ và binary mới trên hai bản clone.
**Chuyện gì xảy ra:** skill show trên bản clone báo lỗi 'read from the active catalog snapshot'. File runtime/catalog/pointer.json không có trong bản clone. Phải chạy rebuild trên bản sao trước khi đọc. Lần thử migrate ngược về v2 cũng lỗi, nên phải dựng workspace v2 bằng tay.
**Bài học:** Một clone git của hub không phải workspace đầy đủ. Runtime được sinh lại bằng rebuild trước khi so sánh.
**Artefact:** Đoạn output lỗi và bước rebuild. Không cần ảnh.
