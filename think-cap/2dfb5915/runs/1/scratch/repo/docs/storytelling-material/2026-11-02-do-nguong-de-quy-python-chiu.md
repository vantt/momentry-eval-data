---
id: 2026-11-02-do-nguong-de-quy-python-chiu
date: 2026-11-02
repo: repo
status: raw
signals: [số trước sau]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L833"]
hook: "Python chịu dict 3000 tầng, nhưng list lồng nhau chết ở tầng 997"
tension: tuong_ma_hoa_ra
sides: ["Dict sâu 3000 tầng vẫn chạy", "List chỉ sâu 996 tầng là lỗi"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đo ngưỡng đệ quy: Python chịu dict 3000 tầng, list chỉ tới 996

**Bối cảnh:** Parser Rust ban đầu giới hạn độ sâu 1000 nên từ chối dict lồng sâu mà Python parse được.
**Chuyện gì xảy ra:** Sau sửa, in dict bằng vòng lặp thay vì đệ quy và bỏ giới hạn parser. Ranh giới đo trực tiếp bằng Python 3.14 với PyYAML: list 996 chạy, 997 lỗi RecursionError; dict tới 3000 khớp output. Qua build index đầy đủ, Python lỗi sớm hơn vài tầng, nên ranh giới khác khi gọi thẳng.
**Bài học:** Đo ngưỡng ở đúng tầng gọi, vì ranh giới đo trực tiếp có thể khác ranh giới qua pipeline.
**Artefact:** Bảng ranh giới các độ sâu 990, 996, 997, 999, 1000, 3000.
