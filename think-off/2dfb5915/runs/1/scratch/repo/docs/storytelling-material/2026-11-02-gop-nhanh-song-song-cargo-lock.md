---
id: 2026-11-02-gop-nhanh-song-song-cargo-lock
date: 2026-11-02
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:2dfb5915#L411", "claude:2dfb5915#L719", "claude:2dfb5915#L957", "claude:2dfb5915#L1599", "claude:2dfb5915#L1696"]
hook: "Mỗi lần gộp nhánh, cùng một xung đột lại quay về"
tension: none
sides: []
strength: 0
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Gộp nhánh song song: Cargo.lock và đoạn PORTING lặp lại

**Bối cảnh:** Nhiều nhánh worktree cùng sửa Cargo.lock và spec/PORTING.md.
**Chuyện gì xảy ra:** Mỗi lần merge, xung đột Cargo.lock được giải bằng cách tạo lại lockfile. Sau một lần merge, spec/PORTING.md có một mục MCP server bị lặp, phải xoá hai lần. Các nhánh cùng sửa một file tổng hợp nên xung đột lặp lại ở mỗi đợt.
**Bài học:** File dùng chung như lockfile hay bảng tổng hợp gây xung đột mỗi lần merge. Nên tách ra file theo từng phase.
**Artefact:** Không có.
