---
id: 2026-10-09-dry-run-tren-ban-clone-hub
date: 2026-10-09
repo: repo
status: raw
signals: ["2"]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [harvest]
lines: ["omp:cd4449ab#L1462", "omp:cd4449ab#L1463", "omp:cd4449ab#L1483", "omp:cd4449ab#L1592", "omp:cd4449ab#L1616", "omp:cd4449ab#L1657", "omp:cd4449ab#L1679"]
hook: "Fixture tự viết toàn xanh, bản clone hub thật lòi ra hai lỗi"
tension: tuong_ma_hoa_ra
sides: ["fixture tự viết đều xanh, tưởng migration ổn", "chạy trên hub thật lòi ngay hai lỗi"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Dry run trên bản clone hub thật bắt lỗi mà fixture tự viết bỏ sót

**Bối cảnh:** Phase 4 phải migrate v1→v2→v3 trên hub đang chạy. Fixture ban đầu do agent viết tay.
**Chuyện gì xảy ra:** Lead chạy dry run trên bản clone của hub, migration v1→v2 lỗi 'canonical entity is missing an ID' ở file meta của test-audit. Nguyên nhân là .meta/** trong workspace v1/v2 bị validate như canonical entity. Sau đó lỗi tiếp theo là 'unknown field repo'. Fixture viết tay vẫn xanh nên không lộ lỗi nào trong hai lỗi này. Agent thay bằng bản copy byte-for-byte của 3 skill và .skillhub/schema-version, rồi gate theo schema-version (dưới 3 thì .meta là hub-meta).
**Bài học:** Fixture viết tay chỉ kiểm được những gì bạn đã nghĩ tới; chạy migration trên bản copy dữ liệu thật trước khi báo xong.
**Artefact:** Output migrate preview trước và sau khi sửa, kèm thông báo lỗi. Che tên skill nội bộ và đường dẫn bản clone.
