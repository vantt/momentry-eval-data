---
id: 2026-10-09-distill-model-reopen-chi-khi-co
date: 2026-10-09
repo: repo
status: raw
signals: [khác]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L1961", "omp:cd4449ab#L1964", "omp:cd4449ab#L1967", "omp:cd4449ab#L1972", "omp:cd4449ab#L1973", "omp:cd4449ab#L1979", "omp:cd4449ab#L1984", "omp:cd4449ab#L2002"]
hook: "Commit f0266c7 thêm 578 dòng: chỉ mở lại khi có bằng chứng mới"
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

# distill_model: reopen chỉ khi có bằng chứng mới

**Bối cảnh:** Mô hình distill: một lesson đã đóng có thể mở lại nếu có bằng chứng mới.
**Chuyện gì xảy ra:** Agent viết distill_model.go và test đầu tiên fail. Sửa điều kiện Decision.Status rỗng và kiểm ValidateLesson trước khi ghi. Commit f0266c7 thêm 578 dòng.
**Bài học:** Reopen phải dựa trên bằng chứng chưa từng thấy, không dựa trên thời gian đã trôi qua.
**Artefact:** Bảng trạng thái lesson: đóng, rồi mở lại khi có bằng chứng mới. Không đưa nội dung lesson.
