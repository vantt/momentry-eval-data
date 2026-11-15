---
id: 2026-11-02-basename-chi-tach-dau-nen-tren
date: 2026-11-02
repo: repo
status: raw
signals: [nguyên nhân bất ngờ]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L1364"]
hook: "Python và Rust cùng một code, trên Windows tên vault thành cả đường dẫn"
tension: tuong_ma_hoa_ra
sides: ["Hai bản port giống hệt nhau", "Rust chỉ tách dấu slash, Windows dùng backslash"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# basename chỉ tách dấu / nên trên Windows tên vault thành cả đường dẫn

**Bối cảnh:** Tên vault xuất hiện trong instructions của MCP và trong link obsidian.
**Chuyện gì xảy ra:** Python dùng ntpath.basename, tách cả backslash và bỏ ổ đĩa. Rust chỉ tách dấu slash nên trên Windows tên vault thành cả đường dẫn. Hai test Windows fail, và chỉ CI Windows bắt được. Sửa để tách theo cả hai dấu.
**Bài học:** Mã xử lý đường dẫn cần test trên cả ba OS; test trên Linux không đủ.
**Artefact:** Không có.
