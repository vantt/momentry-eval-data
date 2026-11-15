---
id: 2026-10-09-xoa-revision-package-va-schema-test-4257
code: M-QA0Z
aliases: [M-QA0Z]
date: 2026-10-09
repo: repo
status: raw
signals: [dao_quyet_dinh, khac, rang_buoc_thiet_ke]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L3056", "omp:cd4449ab#L3058", "omp:cd4449ab#L3083", "omp:cd4449ab#L3085", "omp:cd4449ab#L3088", "omp:cd4449ab#L3289", "omp:cd4449ab#L3290", "omp:cd4449ab#L3292", "omp:cd4449ab#L3355"]
hook: "Xoá sáu schema, test validation đỏ hơn 10 lần"
tension: nho_ma_to
sides: ["Chỉ xoá sáu schema và hai file revision package", "Validation vẫn đọc runtime packages nên test đỏ hơn 10 lần, phải lần theo git log"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án mcp-skill-hub là một công cụ Go đang được rút gọn qua nhiều phase, và người làm đang ở Phase 3: bỏ lớp revision package cùng các schema liên quan. Người làm tin rằng xoá sáu schema và hai file là xong, vì grep không thấy tên schema nào còn được dùng. Hoá ra phần validation vẫn đọc runtime package, nên test distill đỏ nhiều lần và phải lần ngược git log mới hiểu một test đang bảo vệ hành vi cũ. Ai đang dọn code có nhiều lớp phụ thuộc nên liệt kê mọi nơi đọc thứ sắp xoá trước khi xoá."
audience: "dev dọn code có nhiều lớp phụ thuộc, nhất là khi dùng AI để xoá hàng loạt"
spine_context: Một dự án Go tên mcp-skill-hub đang được rút gọn qua nhiều phase; người làm đang ở Phase 3.
spine_context_lines: ["omp:cd4449ab#L6", "omp:cd4449ab#L2374"]
spine_want: Bỏ lớp revision package và các schema liên quan trong Phase 3.
spine_want_lines: ["omp:cd4449ab#L2374"]
spine_obstacle: Validation vẫn đọc runtime package nên test distill đỏ.
spine_obstacle_lines: ["omp:cd4449ab#L3088", "omp:cd4449ab#L3286"]
spine_turn: Tưởng xoá sáu schema và hai file là đủ vì grep không thấy tên schema nào còn được dùng; hoá ra validation vẫn đọc runtime package nên test đỏ.
spine_turn_lines: ["omp:cd4449ab#L3053", "omp:cd4449ab#L3055", "omp:cd4449ab#L3088"]
spine_action: "Git rm sáu schema và hai file revision package, rồi sửa workspace_validation.go để bỏ chỗ đọc chúng."
spine_action_lines: ["omp:cd4449ab#L3056", "omp:cd4449ab#L3080", "omp:cd4449ab#L3083"]
spine_outcome: "Diff workspace_validation.go: thêm 18 dòng, xoá 51 dòng; go test ./internal/app pass. Test distill chưa thấy xanh trong đoạn trích."
spine_outcome_lines: ["omp:cd4449ab#L3289", "omp:cd4449ab#L3355"]
spine_takeaway: "Trước khi xoá, liệt kê mọi nơi còn đọc thứ sắp mất; grep tên không khớp chưa đủ để kết luận là an toàn."
spine_takeaway_lines: ["omp:cd4449ab#L3055", "omp:cd4449ab#L3088"]
completeness: 7
---

# Xoá revision package và schema: test validation đỏ hơn 10 lần

**Góc kể:** Dự án mcp-skill-hub là một công cụ Go đang được rút gọn qua nhiều phase, và người làm đang ở Phase 3: bỏ lớp revision package cùng các schema liên quan. Người làm tin rằng xoá sáu schema và hai file là xong, vì grep không thấy tên schema nào còn được dùng. Hoá ra phần validation vẫn đọc runtime package, nên test distill đỏ nhiều lần và phải lần ngược git log mới hiểu một test đang bảo vệ hành vi cũ. Ai đang dọn code có nhiều lớp phụ thuộc nên liệt kê mọi nơi đọc thứ sắp xoá trước khi xoá.
**Bối cảnh:** Phase 3 bỏ lớp revision package và các schema liên quan. Xoá file xong thì phần validation vẫn gọi tới chúng và test distill đỏ.
**Chuyện gì xảy ra:** Agent git rm sáu schema và hai file revision package. ValidateWorkspace vẫn đọc runtime packages nên test đỏ nhiều lần, agent sửa dần từng chỗ. Một test tombstone đòi hỏi hành vi cũ, nên git log -S được dùng để tìm nguồn gốc của nó. Diff cuối so với main: validation thêm 18 dòng và xoá 51 dòng.
**Bài học:** Trước khi xoá, liệt kê mọi nơi đọc thứ sắp mất. Với test đỏ, đọc lịch sử để biết nó bảo vệ hành vi nào rồi mới quyết định.
**Artefact:** Đầu ra git diff --stat của bước xoá so với main.
