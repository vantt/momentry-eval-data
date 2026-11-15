---
id: 2026-11-02-merge-lap-lai-tren-file-chung
date: 2026-11-02
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, khác]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:2dfb5915#L407", "claude:2dfb5915#L411", "claude:2dfb5915#L719", "claude:2dfb5915#L957", "claude:2dfb5915#L1599", "claude:2dfb5915#L1696"]
hook: "Merge hai lần, mục MCP trong tài liệu xuất hiện hai lần"
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

# Merge lặp lại trên file chung: Cargo.lock xung đột, mục MCP bị nhân đôi

**Bối cảnh:** Mỗi agent làm trên worktree riêng rồi merge vào main. Các file chung như Cargo.lock và spec/PORTING.md xung đột liên tục.
**Chuyện gì xảy ra:** Cargo.lock được sinh lại bằng cargo update -w sau khi chọn bản của main. Mục MCP server trong PORTING xuất hiện hai lần sau hai lần merge, phải xoá bản cũ. Mỗi lần đều phải chạy lại clippy và test trước khi push.
**Bài học:** Mỗi agent nên có một file riêng, hoặc tách tài liệu theo phase để tránh xung đột trên file chung.
**Artefact:** Không.
