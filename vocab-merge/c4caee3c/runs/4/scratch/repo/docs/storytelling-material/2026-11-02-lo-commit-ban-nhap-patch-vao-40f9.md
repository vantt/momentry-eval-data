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
hook: "Lệnh git add gộp cả thư mục dở, bản nháp lọt vào commit khác"
tension: nho_ma_to
sides: ["một lệnh git add tiện tay", "bản nháp dở dang nằm nhầm trong commit của việc khác"]
strength: 2
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
