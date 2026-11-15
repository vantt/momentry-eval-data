---
id: 2026-10-09-migrate-hub-that-vo-meta-bi
date: 2026-10-09
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, người duyệt]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L1462", "omp:cd4449ab#L1481", "omp:cd4449ab#L1496", "omp:cd4449ab#L1523", "omp:cd4449ab#L1529", "omp:cd4449ab#L1594", "omp:cd4449ab#L1616", "omp:cd4449ab#L1657"]
hook: "Test xanh hết, nhưng migrate hub thật vỡ vì thư mục .meta"
tension: tuong_ma_hoa_ra
sides: ["test qua trên fixture", "hub thật vỡ vì .meta bị coi là entity"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Migrate hub thật vỡ: .meta/ bị coi là canonical entity

**Bối cảnh:** Workspace hub v1 có thư mục .meta/ chứa metadata giai đoạn 0. Validator của v1/v2 coi mọi file trong .meta/ là canonical entity.
**Chuyện gì xảy ra:** Dry-run migrate trên bản clone của hub thật báo lỗi 'canonical entity is missing an ID' ở v1→v2. Lead chặn merge và yêu cầu coi .meta/** là hub-meta khi schema < 3. Sau khi đổi, go test ./internal/app ./internal/canonical vẫn FAIL một lần rồi PASS ở lần kế tiếp. Commit d348319 đưa vào bản sửa.
**Bài học:** Khi định dạng dữ liệu thay đổi theo phiên bản, parser phải biết version trước khi validate, không validate theo schema mới cho dữ liệu cũ.
**Artefact:** Thông báo lỗi validator trước và sau khi thêm điều kiện schema < 3 (che tên skill và đường dẫn).
