---
id: 2026-10-09-test-meta-khong-tu-duyet-do-4257
code: M-0J4J
aliases: [M-0J4J]
date: 2026-10-09
repo: repo
status: raw
signals: []
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L532", "omp:cd4449ab#L534", "omp:cd4449ab#L541", "omp:cd4449ab#L543", "omp:cd4449ab#L550", "omp:cd4449ab#L552", "omp:cd4449ab#L559", "omp:cd4449ab#L561", "omp:cd4449ab#L574", "omp:cd4449ab#L576", "omp:cd4449ab#L607", "omp:cd4449ab#L609", "omp:cd4449ab#L610", "omp:cd4449ab#L612"]
hook: "Test 'meta không tự duyệt' đỏ sáu lần, lỗi không nằm ở bước duyệt"
tension: tuong_ma_hoa_ra
sides: ["tưởng lỗi nằm ở bước approve", "hoá ra lỗi ở hàm đọc skill đang theo dõi"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Test 'meta không tự duyệt' đỏ sáu lần vì hàm đọc tracked skill

**Bối cảnh:** Invariant: upstream update không được tự duyệt nội dung đến từ meta. Test này tìm ra đường đọc provenance chưa đúng.
**Chuyện gì xảy ra:** Test đỏ sáu lần. Nguyên nhân nằm ở hàm đọc tracked skill, không nằm ở bước approve. Sửa qua nhiều lượt, gồm thêm test song song và đổi cách đọc meta. Test xanh khi nguồn được đọc đúng thay vì tin vào nội dung meta.
**Bài học:** Test invariant bảo mật thường bắt lỗi ở tầng đọc dữ liệu, không phải tầng quyết định.
**Artefact:** Không cần.
