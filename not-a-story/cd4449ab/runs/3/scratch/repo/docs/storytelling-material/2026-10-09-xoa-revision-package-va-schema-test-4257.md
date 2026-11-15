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
hook: "Xoá 8 file, test validation đỏ hơn 10 lần"
tension: nho_ma_to
sides: ["Chỉ xoá sáu schema và hai file package", "Validation đỏ hơn 10 lần vì còn chỗ đọc ngầm"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Xoá revision package và schema: test validation đỏ hơn 10 lần

**Bối cảnh:** Phase 3 bỏ lớp revision package và các schema liên quan. Xoá file xong thì phần validation vẫn gọi tới chúng và test distill đỏ.
**Chuyện gì xảy ra:** Agent git rm sáu schema và hai file revision package. ValidateWorkspace vẫn đọc runtime packages nên test đỏ nhiều lần, agent sửa dần từng chỗ. Một test tombstone đòi hỏi hành vi cũ, nên git log -S được dùng để tìm nguồn gốc của nó. Diff cuối so với main: validation thêm 18 dòng và xoá 51 dòng.
**Bài học:** Trước khi xoá, liệt kê mọi nơi đọc thứ sắp mất. Với test đỏ, đọc lịch sử để biết nó bảo vệ hành vi nào rồi mới quyết định.
**Artefact:** Đầu ra git diff --stat của bước xoá so với main.
