---
id: 2026-11-02-commit-nham-ban-nhap-cua-agent-40f9
code: M-MVD5
aliases: [M-MVD5]
date: 2026-11-02
repo: repo
status: raw
signals: [khac]
signal_note: "Một lệnh git add gom nhầm file nháp của tiến trình khác, và lỗi được phát hiện sau khi đã commit."
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L1716", "claude:c4caee3c#L1736", "claude:c4caee3c#L1745"]
hook: "Commit bản vá P01, kéo nhầm bản nháp của agent khác"
tension: nho_ma_to
sides: ["Chỉ commit một bản cập nhật P01", "Kéo theo bản nháp sẽ bị ghi đè"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Commit nhầm bản nháp của agent khác vào bản vá P01

**Bối cảnh:** Hai agent cùng sửa một cây làm việc chung.
**Chuyện gì xảy ra:** Lần commit cập nhật P01 kéo theo bản nháp 0007-index-events của agent khác. Bản nháp không nằm trong series.toml nên catchup không áp, và được ghi đè khi agent kia xong. Agent báo cáo việc này trong tin nhắn.
**Bài học:** Dùng git add theo đường dẫn cụ thể, và kiểm git status trước khi commit khi có nhiều agent.
