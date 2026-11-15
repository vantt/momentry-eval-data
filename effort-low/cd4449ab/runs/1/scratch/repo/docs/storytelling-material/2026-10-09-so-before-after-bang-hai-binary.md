---
id: 2026-10-09-so-before-after-bang-hai-binary
date: 2026-10-09
repo: repo
status: raw
signals: [ràng buộc định hình, nguyên nhân bất ngờ]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L1870", "omp:cd4449ab#L1872", "omp:cd4449ab#L1881", "omp:cd4449ab#L1885", "omp:cd4449ab#L1888", "omp:cd4449ab#L1890"]
hook: "So hai binary, nhưng clone thiếu một file nên cả hai đều hỏng"
tension: tuong_ma_hoa_ra
sides: ["tưởng binary cũ có lỗi", "lỗi nằm ở clone thiếu runtime"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# So before/after bằng hai binary: lỗi do clone thiếu runtime

**Bối cảnh:** Yêu cầu so sánh skill show --json trước và sau migration bằng binary cũ và mới trên cùng một clone.
**Chuyện gì xảy ra:** Binary cũ báo 'Resolve or read the skill again' vì clone không có runtime/catalog/pointer.json. Migrate ngược về v2 cũng thất bại với lỗi FIX. Cách chạy là rebuild catalog trên bản clone trước khi so, rồi so name, description, status. Chỉ còn một skill để so trong lần chạy đầu.
**Bài học:** Để so trước và sau, phải build catalog cho cả hai bản; clone thô không có catalog nên mọi lệnh đọc sẽ lỗi.
**Artefact:** Bảng so sánh name/description/status cho các skill (che tên skill).
