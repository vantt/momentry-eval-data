---
id: 2026-11-03-test-sinh-tai-lieu-do-moi-d5ef
code: M-X1WT
aliases: [M-X1WT]
date: 2026-11-03
repo: repo
status: raw
signals: [khac]
signal_note: "Chuyện vặt, nhưng là cơ chế giữ tài liệu CLI khớp với code; đáng ghi thành một mẹo."
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L1670", "claude:ab9a1dd8#L3388", "claude:ab9a1dd8#L3397"]
hook: "Đổi bảng lệnh là test sinh tài liệu đỏ, sinh lại là xong"
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

# Test sinh tài liệu đỏ mỗi khi đổi bảng lệnh: cli-reference phải sinh lại

**Bối cảnh:** Sau khi thêm lệnh quarantine vào bảng lệnh.
**Chuyện gì xảy ra:** Test kiểm cli-reference khớp với bảng lệnh đỏ. Agent chạy scripts/gen-cli-reference.mjs để sinh lại, rồi toàn bộ test về 235 pass.
**Bài học:** Sinh tài liệu từ bảng lệnh và đặt test so khớp. Đổi lệnh là đổi tài liệu cùng lúc.
**Artefact:** Không có artefact đáng chụp.
