---
id: 2026-11-03-hook-chan-lenh-bash-co-chuoi-d5ef
code: M-RAMH
aliases: [M-RAMH]
date: 2026-11-03
repo: repo
status: raw
signals: [khac]
signal_note: "Cùng một kiểu chặn xuất hiện ba lần, và mỗi lần agent phải đổi cách làm."
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:ab9a1dd8#L1388", "claude:ab9a1dd8#L1604", "claude:ab9a1dd8#L1613", "claude:ab9a1dd8#L3367", "claude:ab9a1dd8#L3369"]
hook: "Hook chặn lệnh vì có chuỗi dist hay .git, agent phải đổi công cụ"
tension: giup_ma_hai
sides: ["Hook chặn lệnh nguy hiểm để bảo vệ", "Cũng chặn lệnh vô hại chỉ vì có chuỗi nhạy"]
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Hook chặn lệnh bash có chuỗi nhạy: dist, .git và xoá biến rỗng

**Bối cảnh:** Hook và sandbox của Claude Code chặn một số lệnh bash dựa trên mẫu chuỗi.
**Chuyện gì xảy ra:** Lần đầu: lệnh xoá thư mục tạm bằng biến shell bị chặn vì có thể thành xoá gốc khi biến rỗng. Lần hai: lệnh có chuỗi dist bị chặn khi tạo workflow, agent chuyển sang công cụ Write. Lần ba: lệnh sửa test có chuỗi .git bị chặn, agent đổi sang Edit.
**Bài học:** Tên thư mục build hay .git dễ bị chặn oan. Ghi file bằng công cụ Write hoặc Edit để không phụ thuộc vào mẫu chuỗi của lệnh bash.
