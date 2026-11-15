---
id: 2026-11-02-lo-commit-ban-nhap-patch-vao-40f9
code: M-DJ7D
aliases: [M-DJ7D]
date: 2026-11-02
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L1736"]
hook: "Một lệnh git add lỡ cuốn bản nháp của agent khác vào commit"
tension: nho_ma_to
sides: ["Một lệnh git add thông thường", "Gộp cả thư mục đang dở của agent khác, phải dựng lại"]
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
