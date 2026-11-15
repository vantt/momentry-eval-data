---
id: 2026-10-09-noi-regex-bang-chung-de-test
date: 2026-10-09
repo: repo
status: raw
signals: [đảo quyết định có lý do, người duyệt]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [harvest]
lines: ["omp:cd4449ab#L2507", "omp:cd4449ab#L3656", "omp:cd4449ab#L3966"]
hook: "Test không qua thì nới regex, lead bắt siết lại"
tension: giup_ma_hai
sides: ["nới schema để test xanh", "bằng chứng lỏng lẻo lọt vào bài học mới"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Nới regex bằng chứng để test qua, lead yêu cầu siết lại

**Bối cảnh:** Evidence pattern ban đầu yêu cầu repo@sha:path. Migration gặp dạng ngắn repo@sha không có path nên agent nới pattern và schema.
**Chuyện gì xảy ra:** Agent nới EvidencePattern và distill.schema.json để chấp nhận repo@sha không có path. Lead phát hiện và yêu cầu giữ schema chặt cho lesson mới (repo@<40 hex>:path). Dạng ngắn chỉ được chấp nhận trong migration v4, hoặc giữ trong field legacy_where, và phải ghi vào phase-03.
**Bài học:** Khi test fail vì dữ liệu cũ, đừng nới schema toàn cục; xử lý dữ liệu cũ trong migration và giữ schema mới chặt.
**Artefact:** Diff schema trước và sau, chỉ phần pattern evidence.
