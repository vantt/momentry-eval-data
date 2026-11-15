---
id: 2026-10-30-opc-mjs-nham-skills-x-skill
date: 2026-10-30
repo: repo
status: raw
signals: [nguyên nhân gốc nhỏ]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L498"]
hook: "Skill trùng tên agent bị trình đóng gói tưởng là agent mới"
tension: nho_ma_to
sides: ["một skill đặt trùng tên với agent", "plan báo thêm agent không hề tồn tại"]
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# opc.mjs nhầm skills/X/SKILL.md thành agent khi skill trùng tên agent

**Bối cảnh:** Gói có skill trùng tên với một agent; trình đóng gói đọc nhầm thành agent.
**Chuyện gì xảy ra:** Trình đóng gói quét đường dẫn skills/X/SKILL.md và coi X là agent, nên plan báo thêm agent không tồn tại. Đã sửa khi dựng bộ SEO và ghi vào tóm tắt.
**Bài học:** Khi quét thư mục theo quy ước, phân biệt đường dẫn của từng loại thực thể, đừng suy từ tên.
**Artefact:** Đầu ra plan có dòng agent sai (trước khi sửa).
