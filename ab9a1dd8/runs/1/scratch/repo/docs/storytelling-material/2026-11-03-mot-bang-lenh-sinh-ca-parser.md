---
id: 2026-11-03-mot-bang-lenh-sinh-ca-parser
date: 2026-11-03
repo: repo
status: raw
signals: [artefact]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L959", "claude:ab9a1dd8#L1424", "claude:ab9a1dd8#L1663", "claude:ab9a1dd8#L2230"]
hook: "Một bảng lệnh sinh cả parser, help và tài liệu"
tension: it_ma_nhieu
sides: ["Chỉ viết một bảng lệnh", "Ra parser, --help và tài liệu, quên sinh lại là test đỏ"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Một bảng lệnh sinh cả parser, --help và tài liệu tham chiếu

**Bối cảnh:** Trước đó --help chỉ in một dòng cú pháp, init --help không có mô tả hay ví dụ.
**Chuyện gì xảy ra:** Một bảng lệnh định nghĩa cờ, mô tả, ví dụ và mã thoát. Parser và help đọc từ bảng đó. Tài liệu docs/cli-reference.md được sinh từ bảng và có test kiểm tra độ lệch, nên quên sinh lại là test đỏ.
**Bài học:** Một nguồn sự thật cho lệnh giúp help, tài liệu và parser không lệch nhau; hãy thêm test kiểm độ lệch.
**Artefact:** Đoạn --help trước và sau khi có bảng lệnh.
