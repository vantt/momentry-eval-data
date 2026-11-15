---
id: 2026-11-02-full-build-rust-21-2-ms
date: 2026-11-02
repo: repo
status: raw
signals: [số trước sau]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L941"]
hook: "Full build Rust nhanh gấp gần 3 lần, build không đổi thì ngang nhau"
tension: khac
sides: ["Full build: Rust 21,2 ms, Python 58,6 ms", "Build không đổi: 2,1 ms so với 2,4 ms"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Full build: Rust 21,2 ms so với Python 58,6 ms

**Bối cảnh:** Index adapter e11 và validate, so sánh trên vault mẫu với release build.
**Chuyện gì xảy ra:** Full build Rust 21,2 ms, Python 58,6 ms. Build không đổi: Rust 2,1 ms, Python 2,4 ms. Các bảng SQL và rowid khớp, trừ thứ tự rowid của schema_field và schema_link do Python dùng set nên đổi mỗi lần chạy.
**Bài học:** Ghi rõ khác biệt không ảnh hưởng nội dung để không báo lệch giả.
**Artefact:** Bảng 2x2 thời gian build.
