---
id: 2026-10-09-model-distill-test-reopen-va-go-4257
code: M-HB0Z
aliases: [M-HB0Z]
date: 2026-10-09
repo: repo
status: raw
signals: [khac]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L1972", "omp:cd4449ab#L3083", "omp:cd4449ab#L3085", "omp:cd4449ab#L3133", "omp:cd4449ab#L3137", "omp:cd4449ab#L3238", "omp:cd4449ab#L3262", "omp:cd4449ab#L3316", "omp:cd4449ab#L3346"]
hook: "Xóa một file, test distill đỏ nhiều vòng liền"
tension: nho_ma_to
sides: ["Chỉ xoá revision_package.go và sáu schema cũ", "Test đỏ nhiều vòng, sửa chỗ này lộ chỗ khác"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một dự án hub quản lý skill cho agent đang đơn giản hoá qua các phase. Người làm xoá revision_package.go cùng test, tưởng thế là gọn, nhưng test distill đỏ liên tục qua nhiều vòng sửa validate vì chỗ khác vẫn đọc lớp đó. Ai đang gỡ một lớp dữ liệu nên grep chỗ đọc trước khi xoá để khỏi mất nhiều vòng sửa."
audience: dev đang xoá code cũ trong dự án có nhiều chỗ đọc chung
spine_context: "Một dự án hub quản lý skill cho agent, đang đơn giản hoá qua các phase; người làm đang ở worktree riêng."
spine_context_lines: ["omp:cd4449ab#L6"]
spine_want: Gỡ lớp revision package và đưa model distill mới lên.
spine_want_lines: ["omp:cd4449ab#L3083"]
spine_obstacle: "Sau khi xoá, test distill đỏ liên tục qua nhiều vòng sửa validate."
spine_obstacle_lines: ["omp:cd4449ab#L3088", "omp:cd4449ab#L3262"]
spine_turn: Tưởng xoá revision_package.go cùng test của nó là gọn; hoá ra chỗ khác vẫn đọc lớp đó nên test tombstone vẫn đỏ.
spine_turn_lines: ["omp:cd4449ab#L3083", "omp:cd4449ab#L3088"]
spine_action: "Xoá file và test, thêm nhánh skipRuntimePackages, rồi sửa validate qua nhiều lần chạy test."
spine_action_lines: ["omp:cd4449ab#L3083", "omp:cd4449ab#L3238"]
spine_outcome: "Chưa xanh: go test ./internal/app vẫn FAIL ở lần chạy cuối."
spine_outcome_lines: ["omp:cd4449ab#L3346"]
spine_takeaway: "Trước khi xoá một lớp dữ liệu, grep toàn bộ chỗ đọc nó để biết test nào sẽ đỏ."
spine_takeaway_lines: ["omp:cd4449ab#L3083", "omp:cd4449ab#L3088"]
completeness: 7
---

# Model distill: test reopen và gỡ revision packages đỏ liên tục

**Góc kể:** Một dự án hub quản lý skill cho agent đang đơn giản hoá qua các phase. Người làm xoá revision_package.go cùng test, tưởng thế là gọn, nhưng test distill đỏ liên tục qua nhiều vòng sửa validate vì chỗ khác vẫn đọc lớp đó. Ai đang gỡ một lớp dữ liệu nên grep chỗ đọc trước khi xoá để khỏi mất nhiều vòng sửa.
**Bối cảnh:** Gỡ lớp revision package và đưa model distill mới lên, kèm logic reopen khi có bằng chứng mới.
**Chuyện gì xảy ra:** Xóa revision_package.go và test của nó (L3083-3085). Gỡ thêm sáu schema JSON cũ. Test distill đỏ nhiều vòng: thêm nhánh skipRuntimePackages (L3238), rồi test tombstone đỏ liên tục qua các lần sửa validate (H3262 đến H3346).
**Bài học:** Trước khi xoá một lớp dữ liệu, grep toàn bộ chỗ đọc nó để biết những test nào sẽ đỏ.
**Artefact:** Danh sách file bị xoá và số lần test tombstone đỏ.
