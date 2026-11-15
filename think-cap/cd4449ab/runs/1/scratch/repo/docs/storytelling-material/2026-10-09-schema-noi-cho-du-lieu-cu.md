---
id: 2026-10-09-schema-noi-cho-du-lieu-cu
date: 2026-10-09
repo: repo
status: raw
signals: []
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [harvest]
lines: ["omp:cd4449ab#L1961", "omp:cd4449ab#L2507", "omp:cd4449ab#L3656", "omp:cd4449ab#L3966", "omp:cd4449ab#L3968"]
hook: "Nới schema cho 77 dòng cũ, lead đòi giữ chặt cho dòng mới"
tension: giup_ma_hai
sides: ["Nới schema để dữ liệu cũ migrate được", "Lesson mới cũng lọt dạng lỏng nếu không giữ chặt"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Schema nới cho dữ liệu cũ, rồi lead yêu cầu giữ chặt cho lesson mới

**Bối cảnh:** Quy định evidence của distill quá chặt so với dữ liệu cũ dùng dạng repo@sha không có path.
**Chuyện gì xảy ra:** Để migration qua được, agent nới EvidencePattern và distill.schema.json cho phép repo@sha không có :path. Lead yêu cầu giữ schema chặt cho lesson mới (repo@40-hex:path), chỉ chấp nhận dạng rút gọn trong migration v4 và ghi sai lệch vào phase-03. Dữ liệu thật có 77 mục bị ảnh hưởng.
**Bài học:** Nới schema để đọc dữ liệu cũ là được, nhưng giới hạn việc nới trong đường migration; đường ghi mới phải chặt.
**Artefact:** Diff phần evidence pattern của schema, trước và sau.
