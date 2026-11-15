---
id: 2026-10-09-xoa-revision-package-noi-validation-cho
date: 2026-10-09
repo: repo
status: raw
signals: []
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [harvest]
lines: ["omp:cd4449ab#L3233", "omp:cd4449ab#L3235", "omp:cd4449ab#L3239", "omp:cd4449ab#L3248", "omp:cd4449ab#L3257", "omp:cd4449ab#L3266", "omp:cd4449ab#L3274", "omp:cd4449ab#L3283", "omp:cd4449ab#L3287", "omp:cd4449ab#L3289", "omp:cd4449ab#L3350", "omp:cd4449ab#L3352", "omp:cd4449ab#L3355"]
hook: "Test xanh sau khi nới validation 18 dòng thêm, 51 dòng xoá"
tension: giup_ma_hai
sides: ["Nới từng điều kiện để test qua", "Guard mới có thể che luôn lỗi thật"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Xoá revision package: nới validation cho tới khi test xanh

**Bối cảnh:** Xoá revision package và intake; ValidateWorkspace vẫn kiểm run và observation của tính năng đã xoá.
**Chuyện gì xảy ra:** Test TestDistillGeneratesRemovalTombstoneAndMarksComparisonStale đỏ qua nhiều lượt khi nới từng điều kiện. So với main, workspace_validation.go còn 18 dòng thêm và 51 dòng xoá. Kết quả cuối có guard hasDistillation để bỏ qua kiểm tra khi không có distillation. Test xanh, nhưng đây là nới validation để test qua, cần xem guard có che lỗi thật không.
**Bài học:** Khi xoá tính năng, xoá luôn kiểm tra của nó; mỗi guard thêm vào là nợ phải kiểm tra lại.
**Artefact:** Diff hàm ValidateWorkspace trước và sau.
