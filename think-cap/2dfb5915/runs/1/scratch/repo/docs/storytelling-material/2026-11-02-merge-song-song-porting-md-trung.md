---
id: 2026-11-02-merge-song-song-porting-md-trung
date: 2026-11-02
repo: repo
status: raw
signals: [sự cố vặt, quy trình]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:2dfb5915#L411", "claude:2dfb5915#L719", "claude:2dfb5915#L957", "claude:2dfb5915#L1599"]
hook: "Merge song song lặp section MCP hai lần, nhưng không mất dòng code nào"
tension: none
sides: []
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Merge song song: PORTING.md trùng section, Cargo.lock xung đột

**Bối cảnh:** Nhiều agent làm trong worktree riêng, rồi merge vào main theo từng đợt.
**Chuyện gì xảy ra:** Xung đột lặp lại ở Cargo.lock và spec/PORTING.md. Cách xử lý: lấy bản một bên, chạy lại generate-lockfile, giữ cả hai đoạn Markdown. Có lần section MCP bị lặp hai lần do merge, phải xoá bản cũ. Không mất code nào.
**Bài học:** Tách file ghi chung để mỗi agent có file riêng, giảm xung đột.
**Artefact:** Không có.
