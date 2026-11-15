---
id: 2026-10-09-trust-gate-metadata-upstream-khong-duoc
date: 2026-10-09
repo: repo
status: raw
signals: []
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L532", "omp:cd4449ab#L543", "omp:cd4449ab#L552", "omp:cd4449ab#L561", "omp:cd4449ab#L576", "omp:cd4449ab#L607", "omp:cd4449ab#L609"]
hook: "Cổng tin cậy không cho skill tự duyệt chính mình"
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

# Trust gate: metadata upstream không được tự duyệt chính nó

**Bối cảnh:** Test TestUpstreamMetaCannotSelfApproveOnImportAndUpstreamUpdate kiểm rằng metadata upstream trong skill không được tự duyệt khi import hoặc update.
**Chuyện gì xảy ra:** Test đỏ sáu lượt trước khi xanh. Các lần đỏ chủ yếu do đường dẫn metadata và trạng thái upstream chưa có khi test chạy, không phải lỗi trong logic duyệt. Cổng tin cậy quyết định verdict nên metadata do skill viết không được tự duyệt.
**Bài học:** Test cho cổng tin cậy phải xác nhận cả việc metadata không tự duyệt được, không chỉ đường đi đúng.
**Artefact:** Tên test và kết quả pass, không kèm nội dung skill.
