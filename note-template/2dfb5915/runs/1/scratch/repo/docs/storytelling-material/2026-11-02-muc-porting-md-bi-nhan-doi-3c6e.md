---
id: 2026-11-02-muc-porting-md-bi-nhan-doi-3c6e
code: M-FM7T
aliases: [M-FM7T]
date: 2026-11-02
repo: repo
status: raw
signals: [khac]
signal_note: "Lỗi quy trình lặp lại ba lần: mỗi lần merge hai nhánh cùng viết một mục, phải xoá tay."
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L1599", "claude:2dfb5915#L1696", "claude:2dfb5915#L1715"]
hook: "Mỗi lần merge, một mục tài liệu lại tự nhân đôi"
tension: none
sides: []
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Mục PORTING.md bị nhân đôi sau mỗi lần merge nhánh

**Bối cảnh:** Nhiều agent cùng ghi vào một file tài liệu chung.
**Chuyện gì xảy ra:** Mục MCP server xuất hiện hai lần sau merge, rồi mục query lại bị nhân đôi ở lần merge khác. Agent phải tìm bằng grep và xoá bản cũ. Không có lỗi code nhưng mất vài vòng kiểm.
**Bài học:** File tài liệu chung cần một người giữ, hoặc tách mỗi agent một file.
