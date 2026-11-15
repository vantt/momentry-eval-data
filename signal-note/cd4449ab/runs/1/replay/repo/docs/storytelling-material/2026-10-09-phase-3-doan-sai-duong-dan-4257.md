---
id: 2026-10-09-phase-3-doan-sai-duong-dan-4257
code: M-4FT8
aliases: [M-4FT8]
date: 2026-10-09
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L2378", "omp:cd4449ab#L2380", "omp:cd4449ab#L2381", "omp:cd4449ab#L2383", "omp:cd4449ab#L2386", "omp:cd4449ab#L2399", "omp:cd4449ab#L2401", "omp:cd4449ab#L2417", "omp:cd4449ab#L2419", "omp:cd4449ab#L2420", "omp:cd4449ab#L2444", "omp:cd4449ab#L2446", "omp:cd4449ab#L2470", "omp:cd4449ab#L2471", "omp:cd4449ab#L2473"]
hook: "File ghi do script sinh ra, nhưng script đó không có trong repo"
tension: tuong_ma_hoa_ra
sides: ["header nói file do distill.py sinh ra", "grep không thấy script, nguồn nằm ngoài repo"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Phase 3: đoán sai đường dẫn, script sinh file không có trong repo

**Bối cảnh:** Phase 3 cần file .meta/distill.yaml của hub thật. Agent bắt đầu bằng đường dẫn đoán trước.
**Chuyện gì xảy ra:** Đường dẫn đoán skills/testing/test-audit không tồn tại; glob cho thấy file nằm ở skills/default/test-audit. Header file ghi 'Written by distill-lab/scripts/distill.py', nhưng grep trong repo không thấy script này, và thư mục runtime/sources không có trên hub. Nguồn dữ liệu nằm ngoài repo.
**Bài học:** Trước khi viết code đọc dữ liệu thật, glob đường dẫn và đọc header 'ai sinh ra file' để biết nó có trong repo không.
**Artefact:** Dòng header của file, che nội dung.
