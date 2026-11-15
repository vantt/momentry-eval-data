---
id: 2026-10-29-multica-de-danh-tinh-agent-openclaw
date: 2026-10-29
repo: repo
status: raw
signals: [ràng buộc thiết kế, nguyên nhân bất ngờ]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L2104", "claude:0faf0bb2#L2107", "claude:0faf0bb2#L2111", "claude:0faf0bb2#L2126", "claude:0faf0bb2#L2336", "claude:0faf0bb2#L2410"]
hook: "Chế độ local mất danh tính agent, chế độ gateway có thể mất token"
tension: khac
sides: ["Local: mất SOUL.md và MEMORY.md", "Gateway: giữ danh tính nhưng token có thể không tới"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Multica đè danh tính agent OpenClaw: SOUL và MEMORY bị loại khi chạy ở chế độ local

**Bối cảnh:** Câu hỏi là Multica có định nghĩa agent giống AICoworker không. Khi đọc daemon, phát hiện một đoạn code cố ý loại bỏ file danh tính của agent.
**Chuyện gì xảy ra:** Trước mỗi lượt chạy, Multica đặt workspace của agent OpenClaw thành thư mục riêng của task, và comment trong code ghi rõ SOUL.md và MEMORY.md của workspace gốc bị loại trừ. Ở chế độ gateway thì ngược lại, agent chạy trong gateway nên giữ được danh tính, nhưng biến môi trường token có thể không tới được. Chỉ có hai chế độ, mỗi chế độ mất một thứ khác nhau.
**Bài học:** Trước khi nối một bên điều phối vào một runtime có danh tính, đọc các chỗ code 'cố ý bỏ' của bên điều phối. Đó thường là nơi ranh giới thật nằm.
**Artefact:** Bảng hai chế độ local và gateway, cột 'mất' và 'còn'.
