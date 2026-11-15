---
id: 2026-10-09-yaml-receipt-python-doc-duoc-go-4257
code: M-AFMZ
aliases: [M-AFMZ]
date: 2026-10-09
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo, khac]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L2555", "omp:cd4449ab#L2557", "omp:cd4449ab#L2582", "omp:cd4449ab#L2584", "omp:cd4449ab#L2593", "omp:cd4449ab#L2602", "omp:cd4449ab#L2608", "omp:cd4449ab#L2653", "omp:cd4449ab#L2689", "omp:cd4449ab#L2713", "omp:cd4449ab#L2717", "omp:cd4449ab#L2719", "omp:cd4449ab#L2722", "omp:cd4449ab#L2725", "omp:cd4449ab#L2740", "omp:cd4449ab#L2741", "omp:cd4449ab#L2743", "omp:cd4449ab#L2744", "omp:cd4449ab#L2746", "omp:cd4449ab#L2770", "omp:cd4449ab#L2800", "omp:cd4449ab#L2809"]
hook: "Python đọc được file YAML, Go thì báo lỗi thụt lề"
tension: tuong_ma_hoa_ra
sides: ["Python đọc được nên nghi lỗi ở Go", "file sai thụt lề, Go mới đúng"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# YAML receipt: Python đọc được, Go yaml.v3 lỗi vì thụt lề

**Bối cảnh:** Test migration v3→v4 ghi receipt chứa before_content nhiều dòng, rồi đọc lại.
**Chuyện gì xảy ra:** Python yaml.safe_load đọc được nội dung nên agent nghi lỗi ở Go. Chương trình Go nhỏ cho lỗi 'did not find expected key' khi block literal thụt lề sai. Sau khi đổi sang block literal đúng, giải mã thành công và go test ./internal/migration xanh.
**Bài học:** Hai bộ parse YAML có thể khác nhau về thụt lề; khi nghi ngờ, parse bằng đúng bộ mà code thật dùng.
**Artefact:** Đoạn YAML lỗi và đoạn đã sửa, rút gọn, không lộ dữ liệu.
