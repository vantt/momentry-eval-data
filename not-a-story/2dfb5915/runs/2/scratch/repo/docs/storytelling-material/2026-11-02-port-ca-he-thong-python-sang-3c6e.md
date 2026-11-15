---
id: 2026-11-02-port-ca-he-thong-python-sang-3c6e
code: M-2AKR
aliases: [M-2AKR]
date: 2026-11-02
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L11", "claude:2dfb5915#L62", "claude:2dfb5915#L120", "claude:2dfb5915#L163", "claude:2dfb5915#L172"]
hook: "Port cả hệ thống Python sang Rust: 14 phase, 7 agent chạy song song"
tension: none
sides: []
strength: 1
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Port cả hệ thống Python sang Rust bằng 14 phase, chạy nhiều agent song song

**Bối cảnh:** Repo có sẵn một plan 14 phase (sau này thành 17) để port lõi Python sang Rust. Agent chính được giao điều phối các agent con.
**Chuyện gì xảy ra:** Phase 01 (khung workspace) chạy một mình làm nền, xong mới mở 7 phase song song, mỗi phase một worktree. Sau mỗi phase, agent kiểm tra, merge, push và đợi CI xanh trên Linux, macOS và Windows. Đợt đầu có 5 phase xong mà CI vẫn xanh trên cả ba nền.
**Bài học:** Dựng xong phần nền một mình rồi mới chia việc song song, và mỗi nhánh phải có CI riêng trên đủ các nền tảng.
**Artefact:** Bảng phase và trạng thái CI (chụp, không lộ đường dẫn máy).
