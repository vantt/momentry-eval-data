---
id: 2026-10-09-dry-run-tren-ban-sao-hub-4257
code: M-XAEC
aliases: [M-XAEC]
date: 2026-10-09
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo, nguoi_duyet_may_soan, khac]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L1462", "omp:cd4449ab#L1481", "omp:cd4449ab#L1490", "omp:cd4449ab#L1496", "omp:cd4449ab#L1523", "omp:cd4449ab#L1544", "omp:cd4449ab#L1712"]
hook: "Dry run trên hub thật: thư mục .meta bị tưởng là dữ liệu chính"
tension: tuong_ma_hoa_ra
sides: ["tưởng .meta là metadata của hub", "validator đọc nó như entity canonical, Phase 4 chưa mergeable"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án skill hub đang chuyển định dạng workspace từ v1 lên v3, và Phase 4 đã có test xanh. Nhưng validator đang coi thư mục .meta/ như một entity canonical, nên khi chạy thử trên bản sao hub thật, migration v1 sang v2 dừng vì thiếu ID. Hoá ra trong workspace v1/v2, .meta/ là metadata của hub và không được kiểm như entity; sửa xong thì migration chạy qua. Ai viết migration hay validator cho dữ liệu có thư mục metadata cần biết: phải loại metadata mới khỏi bộ kiểm theo phiên bản workspace."
audience: dev viết migration hoặc validator cho dữ liệu có thư mục metadata
spine_context: Dự án skill hub đang chuyển định dạng workspace từ v1 lên v3; Phase 4 đã có test xanh nhưng chưa được duyệt merge.
spine_context_lines: ["omp:cd4449ab#L6", "omp:cd4449ab#L1364"]
spine_want: Muốn migration chạy được trên một bản sao của hub thật trước khi merge.
spine_want_lines: ["omp:cd4449ab#L1462"]
spine_obstacle: Migration v1 sang v2 dừng với lỗi 'canonical entity is missing an ID' trên .meta/skill.yaml.
spine_obstacle_lines: ["omp:cd4449ab#L1462"]
spine_turn: "Validator coi .meta/ như một entity canonical; hoá ra trong workspace v1/v2, .meta/ là metadata của hub và không được kiểm như entity."
spine_turn_lines: ["omp:cd4449ab#L1462"]
spine_action: Đọc .skillhub/schema-version; khi version nhỏ hơn 3 thì loại .meta/** khỏi bộ kiểm canonical và catalog.
spine_action_lines: ["omp:cd4449ab#L1495", "omp:cd4449ab#L1712"]
spine_outcome: "Migration v1→v2→v3 chạy được trên bản sao hub thật, validate pass và trust không đổi; vòng review sau vẫn lộ hồi quy về mô tả và tên skill."
spine_outcome_lines: ["omp:cd4449ab#L1713"]
spine_takeaway: "Metadata mới phải được loại khỏi bộ kiểm canonical theo phiên bản workspace, đừng để lộ ra lúc migrate."
spine_takeaway_lines: ["omp:cd4449ab#L1462"]
completeness: 7
---

# Dry run trên bản sao hub thật: thư mục .meta bị coi như entity canonical

**Góc kể:** Dự án skill hub đang chuyển định dạng workspace từ v1 lên v3, và Phase 4 đã có test xanh. Nhưng validator đang coi thư mục .meta/ như một entity canonical, nên khi chạy thử trên bản sao hub thật, migration v1 sang v2 dừng vì thiếu ID. Hoá ra trong workspace v1/v2, .meta/ là metadata của hub và không được kiểm như entity; sửa xong thì migration chạy qua. Ai viết migration hay validator cho dữ liệu có thư mục metadata cần biết: phải loại metadata mới khỏi bộ kiểm theo phiên bản workspace.
**Bối cảnh:** Phase 4 đã có test xanh, nhưng lead chạy dry run trên clone hub thật và migration v1 sang v2 dừng với lỗi 'canonical entity is missing an ID'.
**Chuyện gì xảy ra:** Lead đánh dấu Phase 4 chưa mergeable. Nguyên nhân là trong workspace v1 và v2, thư mục .meta vẫn là metadata của hub nhưng validator đọc nó như entity canonical. Agent sửa để đọc .skillhub/schema-version, nếu nhỏ hơn 3 thì loại .meta khỏi canonical và catalog. Sau đó schema-version chạy từ 1 lên 3 và validate pass.
**Bài học:** Metadata mới phải được loại khỏi bộ kiểm canonical theo phiên bản workspace, đừng để việc đó lộ ra khi migrate.
**Artefact:** Log lệnh migrate preview và apply trên bản sao, che đường dẫn.
