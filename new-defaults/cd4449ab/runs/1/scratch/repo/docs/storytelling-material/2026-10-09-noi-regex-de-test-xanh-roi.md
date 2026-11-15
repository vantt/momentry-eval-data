---
id: 2026-10-09-noi-regex-de-test-xanh-roi
date: 2026-10-09
repo: repo
status: raw
signals: []
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [harvest]
lines: ["omp:cd4449ab#L1961", "omp:cd4449ab#L1963", "omp:cd4449ab#L2507", "omp:cd4449ab#L2509", "omp:cd4449ab#L3656", "omp:cd4449ab#L3963", "omp:cd4449ab#L3966"]
hook: "Nới regex cho test xanh, lead bắt lại: lesson mới phải strict"
tension: giup_ma_hai
sides: ["Nới regex để test chạy xanh", "Lỏng quy tắc cho cả lesson mới, lead bắt lại"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Nới regex để test xanh rồi bị lead bắt: siết lại và tách legacy

**Bối cảnh:** Test distill fail vì lesson có evidence dạng repo@sha không kèm path. Agent nới schema và regex để nhận dạng ngắn này.
**Chuyện gì xảy ra:** distill.schema.json và EvidencePattern được nới để chấp nhận repo@sha không có :path. Lead yêu cầu giữ mức strict repo@<40-hex>:path cho lesson mới. Dạng ngắn chỉ được chấp nhận trong migration v4, chuyển thành repo@sha:<skill path> hoặc giữ trong trường legacy_where. Phải ghi deviation này vào phase-03.
**Bài học:** Đừng nới schema để test pass. Đưa dữ liệu cũ vào lối migration riêng và giữ ràng buộc cho dữ liệu mới.
**Artefact:** Hai đoạn regex trước và sau. Không chụp nội dung lesson.
