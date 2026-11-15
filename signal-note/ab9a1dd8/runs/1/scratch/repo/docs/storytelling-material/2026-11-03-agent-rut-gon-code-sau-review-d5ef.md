---
id: 2026-11-03-agent-rut-gon-code-sau-review-d5ef
code: M-M96T
aliases: [M-M96T]
date: 2026-11-03
repo: repo
status: raw
signals: [khac]
signal_note: "Quy trình kiểm: subagent báo đã xong nhưng agent vẫn chạy lại test và installer trước khi báo cáo."
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L2174", "claude:ab9a1dd8#L2190", "claude:ab9a1dd8#L2198", "claude:ab9a1dd8#L2199", "claude:ab9a1dd8#L2200"]
hook: "Subagent báo sửa 8 chỗ, agent vẫn tự chạy lại 232 test"
tension: tuong_ma_hoa_ra
sides: ["Subagent báo đã sửa xong, không đổi đầu ra", "Agent không tin, tự chạy lại toàn bộ test"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Agent rút gọn code sau review: 8 chỗ, không đổi đầu ra, rồi tự chạy lại test thay vì tin báo cáo

**Bối cảnh:** Sau bước review và sửa lỗi, một subagent được giao rút gọn code mới.
**Chuyện gì xảy ra:** Subagent sửa 8 chỗ trên 7 file. Agent tự chạy lại toàn bộ test, installer lifecycle và vòng agent: 232/232 pass.
**Bài học:** Báo cáo của subagent là lời khai. Kiểm lại bằng lệnh trước khi ghi vào plan.
**Artefact:** Không có artefact đáng chụp.
