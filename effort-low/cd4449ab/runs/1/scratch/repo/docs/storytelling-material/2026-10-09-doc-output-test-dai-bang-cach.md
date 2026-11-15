---
id: 2026-10-09-doc-output-test-dai-bang-cach
date: 2026-10-09
repo: repo
status: raw
signals: []
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [outsider]
lines: ["omp:cd4449ab#L1816", "omp:cd4449ab#L2714", "omp:cd4449ab#L2726", "omp:cd4449ab#L2732", "omp:cd4449ab#L2734"]
hook: "Output test dài thì mở theo khoảng dòng, không chạy lại"
tension: none
sides: []
strength: 0
stakes: 0
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đọc output test dài bằng cách mở artifact theo khoảng dòng hoặc theo phần raw, thay vì chạy lại lệnh hay pipe qua grep.

**Chuyện gì xảy ra:** Đọc output test dài bằng cách mở artifact theo khoảng dòng hoặc theo phần raw, thay vì chạy lại lệnh hay pipe qua grep.
**Góc người ngoài:** cách làm phổ biến là Dev thường chạy lại test với grep/tail, hoặc ghi output ra file rồi mở bằng editor; ở đây khác ở Agent đọc các khoảng dòng cụ thể của artifact đầu ra (raw 1-80, 20-40, 21-180) để tìm nguyên nhân lỗi YAML, không tốn lần chạy lại. Người đọc muốn biết công cụ này có sẵn không, hay phải tự lưu log.
