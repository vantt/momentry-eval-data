---
id: 2026-11-02-lo-commit-ban-nhap-patch-vao-40f9
code: M-DJ7D
aliases: [M-DJ7D]
date: 2026-11-02
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L1736"]
hook: "Bản nháp patch lọt vào commit của agent khác vì git add cả thư mục"
tension: nho_ma_to
sides: ["Một lệnh git add gộp cả thư mục đang dở", "Bản nháp nằm lẫn trong commit không liên quan, phải dựng lại"]
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Lỡ commit bản nháp patch vào commit khác

**Bối cảnh:** Một commit tài liệu kéo theo bản nháp patch đang dựng dở.
**Chuyện gì xảy ra:** Bản nháp chưa nằm trong series nên không bị áp dụng. Agent báo và giao agent kia dựng lại trên nhánh mới. Nguyên nhân là git add gộp cả thư mục đang dở.
**Bài học:** git add theo đường dẫn cụ thể, không thêm cả thư mục đang dở.
