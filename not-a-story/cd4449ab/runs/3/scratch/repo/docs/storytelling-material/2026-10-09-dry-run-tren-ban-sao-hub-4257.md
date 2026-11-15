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
hook: "Chạy thử trên bản sao hub thật, .meta bị coi là entity"
tension: nho_ma_to
sides: ["Thư mục .meta chỉ là metadata của hub", "Validator đọc nó như entity canonical, Phase 4 chưa thể merge"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một hub skill cho AI agent đang chuyển định dạng dữ liệu qua nhiều phiên bản, và người làm muốn bước migrate chạy được trên dữ liệu thật. Test trên dữ liệu mẫu đều qua nên họ tin bước này đã xong. Khi chạy thử trên bản sao hub thật, validator lại coi thư mục .meta (metadata của hub) như một skill chính và chặn migration vì thiếu ID. Ai làm công cụ có bước kiểm tự động theo cấu trúc thư mục nên chạy thử trên dữ liệu thật trước khi tin là xong."
audience: dev làm công cụ có migration hoặc validator đọc cấu trúc thư mục
spine_context: "Một hub skill cho AI agent lưu skill dưới dạng file, đang chuyển định dạng workspace từ v1 sang v3 qua từng phase; người làm đang hoàn thiện Phase 4 (migration)."
spine_context_lines: ["omp:cd4449ab#L6", "omp:cd4449ab#L1713"]
spine_want: Muốn Phase 4 chạy đúng trên hub thật để được merge.
spine_want_lines: ["omp:cd4449ab#L1462"]
spine_obstacle: "Test trên dữ liệu mẫu đều xanh, nhưng dry run trên bản sao hub thật dừng ở bước v1→v2."
spine_obstacle_lines: ["omp:cd4449ab#L1461", "omp:cd4449ab#L1462"]
spine_turn: "Tưởng xong vì test xanh; hoá ra validator đọc .meta như skill chính trong workspace v1/v2, nơi .meta là metadata của hub."
spine_turn_lines: ["omp:cd4449ab#L1461", "omp:cd4449ab#L1462"]
spine_action: "Đọc phiên bản workspace, bỏ .meta khỏi bộ kiểm canonical khi dưới v3, và gộp nguồn theo URL repo đã chuẩn hoá."
spine_action_lines: ["omp:cd4449ab#L1712"]
spine_outcome: "Migration v1→v2→v3 chạy được trên bản sao hub thật; validate pass, trust không đổi."
spine_outcome_lines: ["omp:cd4449ab#L1713"]
spine_takeaway: "Thư mục metadata phải được loại khỏi bộ kiểm theo phiên bản dữ liệu; test trên mẫu tự làm không đủ, cần chạy trên bản sao dữ liệu thật."
spine_takeaway_lines: ["omp:cd4449ab#L1462", "omp:cd4449ab#L1713"]
completeness: 7
---

# Dry run trên bản sao hub thật: thư mục .meta bị coi như entity canonical

**Góc kể:** Một hub skill cho AI agent đang chuyển định dạng dữ liệu qua nhiều phiên bản, và người làm muốn bước migrate chạy được trên dữ liệu thật. Test trên dữ liệu mẫu đều qua nên họ tin bước này đã xong. Khi chạy thử trên bản sao hub thật, validator lại coi thư mục .meta (metadata của hub) như một skill chính và chặn migration vì thiếu ID. Ai làm công cụ có bước kiểm tự động theo cấu trúc thư mục nên chạy thử trên dữ liệu thật trước khi tin là xong.
**Bối cảnh:** Phase 4 đã có test xanh, nhưng lead chạy dry run trên clone hub thật và migration v1 sang v2 dừng với lỗi 'canonical entity is missing an ID'.
**Chuyện gì xảy ra:** Lead đánh dấu Phase 4 chưa mergeable. Nguyên nhân là trong workspace v1 và v2, thư mục .meta vẫn là metadata của hub nhưng validator đọc nó như entity canonical. Agent sửa để đọc .skillhub/schema-version, nếu nhỏ hơn 3 thì loại .meta khỏi canonical và catalog. Sau đó schema-version chạy từ 1 lên 3 và validate pass.
**Bài học:** Metadata mới phải được loại khỏi bộ kiểm canonical theo phiên bản workspace, đừng để việc đó lộ ra khi migrate.
**Artefact:** Log lệnh migrate preview và apply trên bản sao, che đường dẫn.
