---
id: 2026-11-03-subagent-rut-gon-8-cho-agent-d5ef
code: M-CHG4
aliases: [M-CHG4]
date: 2026-11-03
repo: repo
status: raw
signals: [khac]
signal_note: "Bước rút gọn do agent con làm kèm kiểm lại: 232/232 test giữ nguyên, cách kiểm này đáng để biết."
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L2174", "claude:ab9a1dd8#L2190", "claude:ab9a1dd8#L2199"]
hook: "Subagent báo rút gọn 8 chỗ, agent vẫn chạy lại 232 test"
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

# Subagent rút gọn 8 chỗ, agent chạy lại toàn bộ kiểm trước khi tin

**Bối cảnh:** Sau khi các module mới chạy được, một bước rút gọn code được giao cho subagent.
**Chuyện gì xảy ra:** Subagent báo đã rút gọn 8 chỗ trong 7 file, như helper bullets, một hàm backup chung, và repoRootOf. Agent không chỉ tin báo cáo mà chạy lại node test, lifecycle installer và vòng agent, kết quả 232/232 vẫn qua và đầu ra không đổi.
**Bài học:** Sau khi agent con rút gọn code, chạy lại toàn bộ kiểm; báo cáo của agent con không phải bằng chứng.
