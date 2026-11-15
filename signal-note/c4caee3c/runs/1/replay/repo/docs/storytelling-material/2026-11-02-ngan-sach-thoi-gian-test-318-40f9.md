---
id: 2026-11-02-ngan-sach-thoi-gian-test-318-40f9
code: M-3VQJ
aliases: [M-3VQJ]
date: 2026-11-02
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L1801", "claude:c4caee3c#L1820", "claude:c4caee3c#L1857"]
hook: "Test chạy 318 ms trên CI, ngưỡng 200 ms: nhân ngưỡng chứ không nới"
tension: chon_mot_mat_mot
sides: ["Giữ ngưỡng 200 ms nghiêm ngặt", "Runner chậm làm test đỏ giả"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Ngân sách thời gian test: 318 ms trên runner so với ngưỡng 200 ms

**Bối cảnh:** Test hiệu năng 1 MB của gói tiếng Việt có ngưỡng 200 ms, đo trên máy phát triển.
**Chuyện gì xảy ra:** Trên runner GitHub, test đo được 318 ms. Thay vì nới ngưỡng, agent thêm biến OHS_PERF_FACTOR nhân ngưỡng khi chạy CI (đặt bằng 3), còn trên máy thật vẫn kiểm đúng 200 ms.
**Bài học:** Ngưỡng hiệu năng nên tách giữa máy thật và CI, và ghi rõ hệ số khi nới.
**Artefact:** Số đo 318 ms và ngưỡng 200 ms.
