---
id: 2026-10-09-fixture-distill-that-1184-dong-42
date: 2026-10-09
repo: repo
status: raw
signals: []
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L2380", "omp:cd4449ab#L2414", "omp:cd4449ab#L2416", "omp:cd4449ab#L2419", "omp:cd4449ab#L2440", "omp:cd4449ab#L2456", "omp:cd4449ab#L2458", "omp:cd4449ab#L2459", "omp:cd4449ab#L2461", "omp:cd4449ab#L2491", "omp:cd4449ab#L2513", "omp:cd4449ab#L2515", "omp:cd4449ab#L2518", "omp:cd4449ab#L2521", "omp:cd4449ab#L2524", "omp:cd4449ab#L2527"]
hook: "Fixture thật: 1184 dòng, 42 lesson, 77 SHA bị cắt ngắn"
tension: none
sides: []
strength: 0
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Fixture distill thật: 1184 dòng, 42 lesson, 77 SHA rút gọn

**Bối cảnh:** File distill Phase 0 của một skill trên hub thật, cần chuyển sang định dạng v4 mà không mất dữ liệu.
**Chuyện gì xảy ra:** File có 1184 dòng, 46161 byte, 42 lesson và cursor cho hai nguồn. Đếm được 77 mục 'where' dùng SHA rút gọn. git rev-parse trong mirror cho ra SHA đầy đủ tương ứng. Kiểm tra không có key trùng, không có key sai pattern; 39 lesson ở trạng thái candidate và 3 ở planned.
**Bài học:** Dữ liệu cũ hay có SHA rút gọn; quy đổi bằng git rev-parse trên mirror trước khi đặt validator chặt.
**Artefact:** Bảng đếm lesson theo trạng thái và số SHA rút gọn, không đưa nội dung lesson.
