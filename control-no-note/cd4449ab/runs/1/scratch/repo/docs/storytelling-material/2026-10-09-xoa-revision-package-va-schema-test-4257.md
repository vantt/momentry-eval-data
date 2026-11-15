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
sides: ["Chỉ xoá vài file schema và revision package", "Validation vẫn đọc chúng nên test đỏ hơn 10 lần"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án là công cụ MCP skill hub đang được đơn giản hoá qua từng phase, và người làm đang gỡ lớp revision package cùng các schema cũ. Họ tưởng xoá file là đủ, vì grep tên schema không ra kết quả nào. Nhưng validation vẫn đọc các package đó qua struct, nên test distill đỏ nhiều lần khi file đã mất. Ai dọn code có phụ thuộc ngầm nên liệt kê mọi chỗ đọc trước khi xoá."
audience: dev dọn code hoặc xoá tính năng cũ có phụ thuộc ngầm
spine_context: Dự án là công cụ MCP skill hub đang được đơn giản hoá qua từng phase; người làm đang ở phase 3.
spine_context_lines: ["omp:cd4449ab#L2374"]
spine_want: Gỡ lớp revision package và các schema cũ theo kế hoạch phase 3.
spine_want_lines: ["omp:cd4449ab#L2374"]
spine_obstacle: "Validation vẫn đọc các package đó, nên xoá xong test distill đỏ."
spine_obstacle_lines: ["omp:cd4449ab#L3061", "omp:cd4449ab#L3088"]
spine_turn: Tưởng xoá file là đủ vì grep tên schema không ra kết quả nào; hoá ra validation vẫn đọc runtime packages qua struct.
spine_turn_lines: ["omp:cd4449ab#L3055", "omp:cd4449ab#L3056", "omp:cd4449ab#L3061"]
spine_action: "Xoá sáu schema và hai file revision package, rồi sửa validation để nó thôi đọc chúng."
spine_action_lines: ["omp:cd4449ab#L3056", "omp:cd4449ab#L3080", "omp:cd4449ab#L3083"]
spine_outcome: Test app xanh; diff validation là 18 dòng thêm và 51 dòng xoá.
spine_outcome_lines: ["omp:cd4449ab#L3289", "omp:cd4449ab#L3355"]
spine_takeaway: Grep tên cũ trả rỗng vẫn có thể sót chỗ đọc qua struct; liệt kê mọi nơi đọc trước khi xoá.
spine_takeaway_lines: ["omp:cd4449ab#L3055", "omp:cd4449ab#L3061"]
completeness: 7
---

# Xoá revision package và schema: test validation đỏ hơn 10 lần

**Góc kể:** Dự án là công cụ MCP skill hub đang được đơn giản hoá qua từng phase, và người làm đang gỡ lớp revision package cùng các schema cũ. Họ tưởng xoá file là đủ, vì grep tên schema không ra kết quả nào. Nhưng validation vẫn đọc các package đó qua struct, nên test distill đỏ nhiều lần khi file đã mất. Ai dọn code có phụ thuộc ngầm nên liệt kê mọi chỗ đọc trước khi xoá.
**Bối cảnh:** Phase 3 bỏ lớp revision package và các schema liên quan. Xoá file xong thì phần validation vẫn gọi tới chúng và test distill đỏ.
**Chuyện gì xảy ra:** Agent git rm sáu schema và hai file revision package. ValidateWorkspace vẫn đọc runtime packages nên test đỏ nhiều lần, agent sửa dần từng chỗ. Một test tombstone đòi hỏi hành vi cũ, nên git log -S được dùng để tìm nguồn gốc của nó. Diff cuối so với main: validation thêm 18 dòng và xoá 51 dòng.
**Bài học:** Trước khi xoá, liệt kê mọi nơi đọc thứ sắp mất. Với test đỏ, đọc lịch sử để biết nó bảo vệ hành vi nào rồi mới quyết định.
**Artefact:** Đầu ra git diff --stat của bước xoá so với main.
