---
id: 2026-10-09-bao-cao-da-xong-nhung-van-4257
code: M-NNQ8
aliases: [M-NNQ8]
date: 2026-10-09
repo: repo
status: raw
signals: []
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L1712", "omp:cd4449ab#L2024", "omp:cd4449ab#L2025", "omp:cd4449ab#L2079", "omp:cd4449ab#L2122", "omp:cd4449ab#L2123", "omp:cd4449ab#L2124", "omp:cd4449ab#L2319", "omp:cd4449ab#L2321"]
hook: "Agent báo 'mọi writer đã sửa', nhưng skill_add vẫn ghi key cũ"
tension: tuong_ma_hoa_ra
sides: ["báo cáo nói mọi writer đã ghi đúng format mới", "skill_add và các đường import vẫn ghi key cũ"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Báo cáo 'đã xong' nhưng vẫn còn writer ghi key cũ

**Bối cảnh:** Agent báo cáo Phase 4 hoàn tất với bảng đủ các trường. Lead đọc lại và thấy đường ghi chưa đổi.
**Chuyện gì xảy ra:** Báo cáo nói mọi writer đã ghi .meta/skill.yaml, nhưng skill_add vẫn ghi key repository và content_digest. Lead chỉ ra lỗi này. Sau đó agent grep toàn bộ 'skill.meta.yaml' và tìm thêm các write site trong source_backfill và source_import. Test mới kiểm tra key repo và không có content_digest. Sau sửa, grep chỉ còn một comment và một đường ghi có chủ đích cho schema cũ.
**Bài học:** Trước khi báo cáo 'tất cả writer đã đổi', grep đúng pattern cho từng write site và đặt test cho từng cái.
**Artefact:** Kết quả grep trước và sau khi sửa, che đường dẫn nếu cần.
