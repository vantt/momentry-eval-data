---
id: 2026-10-09-migration-v3-v4-receipt-yaml-va
date: 2026-10-09
repo: repo
status: raw
signals: [khác]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L2555", "omp:cd4449ab#L2584", "omp:cd4449ab#L2593", "omp:cd4449ab#L2602", "omp:cd4449ab#L2608", "omp:cd4449ab#L2651", "omp:cd4449ab#L2689", "omp:cd4449ab#L2713", "omp:cd4449ab#L2720", "omp:cd4449ab#L2741", "omp:cd4449ab#L2744", "omp:cd4449ab#L2761", "omp:cd4449ab#L2770", "omp:cd4449ab#L2800", "omp:cd4449ab#L2809"]
hook: "Migration đỏ nhiều lượt vì một block YAML lệch thụt lề"
tension: nho_ma_to
sides: ["Một block scalar YAML lệch thụt lề", "Mutation báo invalid, migration đỏ nhiều lượt"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Migration v3→v4: receipt YAML và validator mutation từ chối change

**Bối cảnh:** Migration v3→v4 ghi receipt bằng YAML và đi qua validator mutation.
**Chuyện gì xảy ra:** Test migration v3→v4 đỏ nhiều lượt. Lỗi đầu là receipt thiếu field, sau đó mutation báo 'proposed mutation is invalid'. Nguyên nhân là validator đọc các file distill/ như canonical, và một block scalar YAML bị lệch thụt lề. Agent đối chiếu bằng Python yaml và Go yaml.v3, sửa thụt lề '|' thì decode được.
**Bài học:** Khi validator từ chối, đọc luật của validator trước rồi mới sửa dữ liệu. Đừng sửa dữ liệu cho qua khi chưa biết validator đang áp dụng gì.
**Artefact:** Thông báo 'proposed mutation is invalid' kèm tên file gây lỗi, đã che nội dung.
