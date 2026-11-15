---
id: 2026-10-09-phase-3-bat-dau-tu-file
date: 2026-10-09
repo: repo
status: raw
signals: [khác]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["omp:cd4449ab#L2378", "omp:cd4449ab#L2384", "omp:cd4449ab#L2414", "omp:cd4449ab#L2416", "omp:cd4449ab#L2456", "omp:cd4449ab#L2458", "omp:cd4449ab#L2461", "omp:cd4449ab#L2492", "omp:cd4449ab#L2513", "omp:cd4449ab#L2515", "omp:cd4449ab#L2521", "omp:cd4449ab#L2527"]
hook: "File 1184 dòng, 42 lessons: agent resolve từng trong 77 SHA"
tension: none
sides: []
strength: 0
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Phase 3 bắt đầu từ file distill thật: 1184 dòng, 42 lessons, 77 SHA rút gọn

**Bối cảnh:** Phase 3 phải chuyển file .meta/distill.yaml Phase 0 của hub đang chạy. File gốc không được sửa.
**Chuyện gì xảy ra:** File dài 1184 dòng, khoảng 46 KB, có 42 lessons và 2 cursor. Có 77 mục commit rút gọn, agent resolve từng SHA bằng git rev-parse trong mirror. Trạng thái lessons là 39 candidate và 3 planned. Coverage của một nguồn là 15 read và 7 not_read, nguồn kia là 6 read và 4 not_read. Một số đường dẫn đoán sai như distill.go và insight.go làm chậm vài lượt.
**Bài học:** Dữ liệu migration thật phức tạp hơn trí nhớ. Hãy đếm và resolve từng khoá trước khi viết schema.
**Artefact:** Bảng thống kê: số lessons, số SHA, trạng thái. Không đưa câu hỏi hay nội dung lesson.
**Góc người ngoài:** cách làm phổ biến là Viết converter theo schema trên giấy rồi sửa khi gặp lỗi lúc chạy; ở đây khác ở Khảo sát dữ liệu trước (profiling) cho biết sớm mọi trường hợp lệch như 77 SHA ngắn, rồi chứng minh được chúng giải quyết được. Người đọc có thể áp dụng cho mọi lần migrate dữ liệu cũ.
