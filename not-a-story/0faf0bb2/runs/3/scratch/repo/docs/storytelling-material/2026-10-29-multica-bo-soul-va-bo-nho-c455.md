---
id: 2026-10-29-multica-bo-soul-va-bo-nho-c455
code: M-DRMX
aliases: [M-DRMX]
date: 2026-10-29
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo, rang_buoc_thiet_ke]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L2105", "claude:0faf0bb2#L2126", "claude:0faf0bb2#L2336"]
hook: "Ghép hai agent lại, agent mất luôn 'con người' và trí nhớ của nó"
tension: hop_ma_tan
sides: ["Ghép Multica với AICoworker để có điều phối và agent sẵn có", "Workspace bị thay, SOUL.md và MEMORY.md của agent bị loại, mất danh tính"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Multica bỏ SOUL và bộ nhớ của agent OpenClaw: mất 'con người' của agent khi ghép với AICoworker

**Bối cảnh:** Câu hỏi: Multica có định nghĩa agent như AICoworker không. Đọc code thì thấy Multica cố ý đổi workspace OpenClaw thành thư mục của từng task.
**Chuyện gì xảy ra:** Trong openclaw_config.go, Multica đặt workspace của mọi agent OpenClaw thành thư mục task và ghi rõ SOUL.md và MEMORY.md của host bị loại trừ. Multica không có bộ nhớ dài hạn; chỉ nối lại được session theo cặp (agent, issue). Ở chế độ gateway thì có thể giữ được danh tính nhưng chưa kiểm chứng.
**Bài học:** Trước khi ghép hai hệ thống agent, tìm xem lớp điều phối có ghi đè không gian làm việc của agent hay không.
**Artefact:** Trích dẫn comment trong code 'Host-workspace SOUL.md and MEMORY.md are therefore excluded' (không kèm đường dẫn máy).
