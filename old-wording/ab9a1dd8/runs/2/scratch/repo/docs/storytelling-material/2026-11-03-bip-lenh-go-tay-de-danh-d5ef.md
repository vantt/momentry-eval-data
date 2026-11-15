---
id: 2026-11-03-bip-lenh-go-tay-de-danh-d5ef
code: M-962P
aliases: [M-962P]
date: 2026-11-03
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L315", "claude:ab9a1dd8#L332"]
hook: "Một lệnh /bip, và Codex làm mất dấu nó"
tension: none
sides: []
strength: 0
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# /bip: lệnh gõ tay để đánh dấu 'chỗ này đáng kể' ngay lúc đang làm việc

**Bối cảnh:** Hook gom sau phiên chỉ thấy vết trong transcript. Người biết khoảnh khắc đáng kể thì chưa có cách đánh dấu.
**Chuyện gì xảy ra:** Lệnh /bip là prompt mẫu, yêu cầu agent viết 2 đến 4 câu rồi gọi momentry add --by human. Trên Claude Code, dòng /bip còn nằm trong transcript nên lần gom sau chấm điểm kỹ hơn. Codex bung prompt thành chữ nên không còn dấu /bip, chỉ còn đường add.
**Bài học:** Cần cả máy gom rộng lẫn người đánh dấu chính xác. Công cụ tự động không biết điều gì đáng kể với người đang làm.
**Artefact:** Ảnh terminal khi gõ /bip và dòng xác nhận id chuyện. Che nội dung ghi chú.
