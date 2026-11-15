---
id: 2026-10-09-hai-ban-curator-skill-md-phai-4257
code: M-NK81
aliases: [M-NK81]
date: 2026-10-09
repo: repo
status: raw
signals: []
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L1933", "omp:cd4449ab#L1945", "omp:cd4449ab#L2374", "omp:cd4449ab#L3593", "omp:cd4449ab#L3596", "omp:cd4449ab#L3598", "omp:cd4449ab#L3611", "omp:cd4449ab#L3614", "omp:cd4449ab#L3616", "omp:cd4449ab#L3617", "omp:cd4449ab#L3620"]
hook: "Sửa một file SKILL.md, bản sao thứ hai bắt lệch"
tension: nho_ma_to
sides: ["sửa một file hướng dẫn", "bản sao lệch là test boundary đỏ"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Hai bản curator SKILL.md phải giống hệt và boundary test bắt lệch

**Bối cảnh:** Lead yêu cầu thêm dòng O8 từ worktree D vào thân curator. Có hai bản SKILL.md: system-skills và internal/systemskills. Boundary test phải xanh.
**Chuyện gì xảy ra:** Sau khi sửa bản gốc, cp sang bản thứ hai để hai file giống hệt. Test embed kiểm tra danh sách compatible tools phải khớp CuratorMetadata. Danh sách này phải cập nhật cùng commit vì curation_tools.go bị xoá. Boundary test đỏ hai lần trước khi xanh.
**Bài học:** Bản sao của một tài nguyên nhúng nên được sinh bằng script và có test so sánh bằng nhau.
**Artefact:** Diff hai file SKILL.md sau cp, kết quả rỗng. Không cần ảnh.
