---
id: 2026-10-29-multica-che-do-local-thay-workspace-c455
code: M-S813
aliases: [M-S813]
date: 2026-10-29
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo, rang_buoc_thiet_ke]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:0faf0bb2#L2099", "claude:0faf0bb2#L2105", "claude:0faf0bb2#L2111", "claude:0faf0bb2#L2126", "claude:0faf0bb2#L2392", "claude:0faf0bb2#L2410"]
hook: "Chế độ local của Multica thay workspace, mất luôn SOUL và bộ nhớ agent"
tension: giup_ma_hai
sides: ["Multica chạy agent OpenClaw thuận tiện", "Workspace bị thay, agent mất SOUL.md và MEMORY.md"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Multica chế độ local thay workspace OpenClaw, mất SOUL và bộ nhớ của agent

**Bối cảnh:** Cần biết agent OpenClaw chạy qua Multica có giữ danh tính của AICoworker không.
**Chuyện gì xảy ra:** openclaw_config.go đặt workspace của mọi agent OpenClaw thành thư mục của task, và comment trong code ghi rõ SOUL.md và MEMORY.md bị loại. Chế độ gateway có thể giữ được danh tính, nhưng chưa chạy thử; ở chế độ đó token có thể không tới được agent vì nằm trong tiến trình CLI.
**Bài học:** Đọc code tích hợp trước khi tin vào câu 'dùng được cả hai'.
**Artefact:** Đoạn comment trong code, trích ngắn.
