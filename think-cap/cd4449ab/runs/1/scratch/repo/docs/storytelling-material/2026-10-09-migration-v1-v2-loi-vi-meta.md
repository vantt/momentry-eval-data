---
id: 2026-10-09-migration-v1-v2-loi-vi-meta
date: 2026-10-09
repo: repo
status: raw
signals: []
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [harvest]
lines: ["omp:cd4449ab#L1462", "omp:cd4449ab#L1481", "omp:cd4449ab#L1496", "omp:cd4449ab#L1523", "omp:cd4449ab#L1529", "omp:cd4449ab#L1609"]
hook: "Bước validate đã kiểm, nhưng lỗi nằm ở migrate"
tension: cam_ma_van_lot
sides: ["Agent đã kiểm bước validate", "Lỗi nằm ở migrate, coi thư mục .meta là entity thật"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Migration v1→v2 lỗi vì .meta/ bị coi là entity canonical

**Bối cảnh:** Lead chạy dry-run migrate v1→v2→v3 trên bản clone của hub thật và báo lỗi.
**Chuyện gì xảy ra:** Validator báo 'canonical entity is missing an ID' cho file .meta/skill.yaml. Gốc là validator coi mọi thứ dưới .meta/ là canonical entity, trong khi ở workspace v1/v2 thư mục này là metadata do hub quản lý (IsHubMeta). Sửa: đọc schema version từ .skillhub/schema-version, khi nhỏ hơn 3 thì loại .meta/** khỏi canonical validation và catalog input. Lỗi nằm ở migrate chứ không ở bước validate mà agent đã kiểm.
**Bài học:** Metadata do hệ thống quản lý phải được loại khỏi validator theo version của workspace, đừng để validator quét theo đường dẫn.
**Artefact:** Dòng lỗi migrate, che tên skill và đường dẫn tuyệt đối.
