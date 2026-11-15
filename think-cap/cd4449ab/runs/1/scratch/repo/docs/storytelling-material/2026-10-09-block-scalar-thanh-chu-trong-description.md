---
id: 2026-10-09-block-scalar-thanh-chu-trong-description
date: 2026-10-09
repo: repo
status: raw
signals: []
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [harvest]
lines: ["omp:cd4449ab#L1713", "omp:cd4449ab#L1861", "omp:cd4449ab#L1863"]
hook: "Mô tả skill sau migrate chỉ còn đúng hai ký tự '>-'"
tension: nho_ma_to
sides: ["Trust và status vẫn đúng", "Mô tả thành '>-' làm hỏng việc định tuyến skill"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Block scalar '>-' thành chữ '>-' trong description

**Bối cảnh:** SKILL.md của một skill dùng frontmatter với 'description: >-' và đoạn văn thụt lề bên dưới.
**Chuyện gì xảy ra:** Sau migrate, description của skill herdr-cook-plan thành đúng chuỗi '>-'. Parser frontmatter đọc từng dòng nên không hiểu block scalar. Resolver dùng description để routing, nên đây là hồi quy routing dù trust và status vẫn đúng. Sửa: parse bằng YAML parser có sẵn trong codebase.
**Bài học:** Đừng tự parse YAML bằng tay: block scalar '>-' và '|' là chỗ parser tự viết hay hỏng âm thầm.
**Artefact:** Cột description trước/sau trong skill show --json, che tên skill.
