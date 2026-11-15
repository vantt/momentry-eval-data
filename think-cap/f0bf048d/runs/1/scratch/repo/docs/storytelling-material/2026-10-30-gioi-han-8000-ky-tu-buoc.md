---
id: 2026-10-30-gioi-han-8000-ky-tu-buoc
date: 2026-10-30
repo: repo
status: raw
signals: ["5"]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L498"]
hook: "Giới hạn 8000 ký tự lại giúp giữ nguyên văn mọi vai trò"
tension: giup_ma_hai
sides: ["Giới hạn ký tự bó buộc, tưởng phải cắt bớt nội dung", "Tách thành skill nên giữ được nguyên văn gốc"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Giới hạn 8000 ký tự buộc tách vai trò thành skill

**Bối cảnh:** Hai vai trò gốc từ kho cộng đồng dài 14-15k ký tự, vượt giới hạn instructions của agent trên Multica.
**Chuyện gì xảy ra:** Giữ nguyên văn mỗi vai trò thành một skill kèm file LICENSE, còn AGENTS.md chỉ chứa phần gắn vai trò vào công ty. Cách này giữ được nội dung gốc mà không vượt giới hạn.
**Bài học:** Khi giới hạn độ dài instructions, đưa phần dài vào skill và giữ AGENTS.md ngắn.
