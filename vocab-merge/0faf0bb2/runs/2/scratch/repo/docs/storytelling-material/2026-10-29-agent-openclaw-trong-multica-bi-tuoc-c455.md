---
id: 2026-10-29-agent-openclaw-trong-multica-bi-tuoc-c455
code: M-N3ZW
aliases: [M-N3ZW]
date: 2026-10-29
repo: repo
status: raw
signals: [ràng buộc định hình thiết kế, số]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:0faf0bb2#L2105", "claude:0faf0bb2#L2111", "claude:0faf0bb2#L2126", "claude:0faf0bb2#L2410"]
hook: "Chạy agent trong Multica, nó mất luôn danh tính và bộ nhớ"
tension: giup_ma_hai
sides: ["Daemon cấp thư mục riêng cho từng task", "SOUL.md và MEMORY.md bị loại, agent mất bản thân"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Agent OpenClaw trong Multica bị tước danh tính: daemon đè workspace bằng thư mục task

**Bối cảnh:** Khi đối chiếu định nghĩa agent của Multica với AICoworker.
**Chuyện gì xảy ra:** Multica chạy OpenClaw ở chế độ local bằng cách đặt workspace thành thư mục riêng của từng task. Comment trong code ghi rõ SOUL.md và MEMORY.md bị loại trừ. Như vậy agent mất danh tính, bộ nhớ và skill của AICoworker. Chế độ gateway có thể giữ được chúng, nhưng biến môi trường token không tới được gateway. Local ghi ngược được, còn gateway giữ được con người của agent.
**Bài học:** Khi ghép hai hệ thống, kiểm tra xem runtime bên trong có ghi đè danh tính không. Một agent có thể mất phần cốt lõi mà vẫn chạy bình thường.
**Artefact:** Comment trong code: 'Host-workspace SOUL.md and MEMORY.md are therefore excluded'. Đường dẫn đã che.
