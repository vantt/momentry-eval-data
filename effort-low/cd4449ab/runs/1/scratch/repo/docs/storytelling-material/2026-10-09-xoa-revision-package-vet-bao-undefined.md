---
id: 2026-10-09-xoa-revision-package-vet-bao-undefined
date: 2026-10-09
repo: repo
status: raw
signals: [số trước sau, nguyên nhân bất ngờ]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L3083", "omp:cd4449ab#L3088", "omp:cd4449ab#L3139", "omp:cd4449ab#L3146", "omp:cd4449ab#L3151", "omp:cd4449ab#L3224", "omp:cd4449ab#L3353"]
hook: "Xoá một package, sửa import sót làm test đỏ 17 lần"
tension: nho_ma_to
sides: ["một import bị mất và vài kiểm tra cũ", "17 lần test đỏ mới xanh"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Xoá revision package: vet báo undefined và distill test đỏ 17 lần

**Bối cảnh:** Xoá internal/distill/revision_package và các chỗ dùng nó. Validate workspace vẫn còn gọi nhánh runtime package.
**Chuyện gì xảy ra:** Sau khi xoá, go vet báo 'undefined: context' vì import bị mất khi sửa file. Test distill và app đỏ khoảng 17 lần vì validate còn kiểm tra runtime package và tombstone chưa đúng. Đến lần cuối, go test ./internal/app PASS sau khoảng 18 giây.
**Bài học:** Khi xoá một tầng dữ liệu, kiểm tra lại validator và các nhánh validate trước, vì chúng thường bị bỏ sót.
**Artefact:** Danh sách nhánh validate bị ảnh hưởng trước và sau khi xoá.
