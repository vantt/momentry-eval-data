---
id: 2026-10-09-fixture-v3-v4-va-wal-receipt-4257
code: M-TV3F
aliases: [M-TV3F]
date: 2026-10-09
repo: repo
status: raw
signals: []
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L2557", "omp:cd4449ab#L2584", "omp:cd4449ab#L2593", "omp:cd4449ab#L2602", "omp:cd4449ab#L2608", "omp:cd4449ab#L2644", "omp:cd4449ab#L2653", "omp:cd4449ab#L2668", "omp:cd4449ab#L2677", "omp:cd4449ab#L2689", "omp:cd4449ab#L2713", "omp:cd4449ab#L2717", "omp:cd4449ab#L2722", "omp:cd4449ab#L2740", "omp:cd4449ab#L2746", "omp:cd4449ab#L2750"]
hook: "8 lần test đỏ chỉ vì thụt lề sai một đoạn YAML"
tension: nho_ma_to
sides: ["Một lỗi thụt lề trong fixture", "8 lần test đỏ liên tiếp"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Fixture v3→v4 và WAL receipt: YAML lồng trong YAML, 8 lần đỏ

**Bối cảnh:** Migration v3→v4 ghi WAL receipt có chứa nội dung file bên trong. Test đọc lại receipt bằng yaml thì lỗi.
**Chuyện gì xảy ra:** Lỗi 'did not find expected key' ở dòng 1. Nguyên nhân là before_content được nhúng dạng text thô với thụt lề sai. go run đọc stdin không chạy được, nên agent dùng Python và một chương trình Go nhỏ để kiểm tra từng đoạn. Sửa bằng block scalar | là decode được. Khoảng 8 lần test đỏ trước khi preview chạy ổn.
**Bài học:** Khi nhúng một tài liệu YAML trong YAML, dùng block scalar và decode lại bằng chính parser của hệ thống trong test.
**Artefact:** Đoạn YAML trước và sau khi thêm |. Không dán nội dung receipt thật.
