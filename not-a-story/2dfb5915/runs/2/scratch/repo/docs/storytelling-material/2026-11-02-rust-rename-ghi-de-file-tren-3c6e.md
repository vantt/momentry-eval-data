---
id: 2026-11-02-rust-rename-ghi-de-file-tren-3c6e
code: M-BHTW
aliases: [M-BHTW]
date: 2026-11-02
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L229"]
hook: "Rust rename ghi đè file trên Windows, Python thì không"
tension: tuong_ma_hoa_ra
sides: ["Tưởng rename của hai ngôn ngữ cùng hành vi", "Rust trên Windows ghi đè đích, Python thì không, nên phải gọi MoveFileExW"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Rust rename ghi đè file trên Windows, Python thì không

**Bối cảnh:** Module platform cần di chuyển file an toàn giống bản Python.
**Chuyện gì xảy ra:** std::fs::rename của Rust trên Windows ghi đè đích, còn os.rename của Python thì không. Trên Windows, agent gọi trực tiếp MoveFileExW không có cờ thay thế, kèm hỗ trợ đường dẫn dài. Bộ test có 15 ca, và 19 ca của Python được đánh giá riêng.
**Bài học:** Hai ngôn ngữ cùng gọi một thao tác tên giống nhau nhưng có ngữ nghĩa khác trên một nền tảng. Đọc tài liệu từng nền.
