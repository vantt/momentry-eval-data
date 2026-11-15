---
id: 2026-11-05-skill-frontend-co-tren-dia-nhung
date: 2026-11-05
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:6a207191#L1525", "claude:6a207191#L1526", "claude:6a207191#L1545", "claude:6a207191#L1566", "claude:6a207191#L1567", "claude:6a207191#L1579", "claude:6a207191#L1585", "claude:6a207191#L1592"]
hook: "Skill nằm ngay trên đĩa, nhưng phiên vẫn báo 'unknown skill'"
tension: tuong_ma_hoa_ra
sides: ["File skill có thật trong thư mục dự án", "Phiên đang chạy không nạp nó, gọi hai lần đều unknown"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Skill frontend có trên đĩa nhưng phiên chưa nạp: unknown skill

**Bối cảnh:** User yêu cầu dùng skill ak-frontend-development để làm web UI.
**Chuyện gì xảy ra:** Gọi skill báo unknown hai lần, và hub cũng báo not_found. Agent tìm và thấy skill nằm trong thư mục .claude/skills của dự án, nhưng phiên hiện tại chưa nạp nó. Agent đọc thẳng file SKILL.md rồi làm theo, và ghi rõ điều đó trong báo cáo.
**Bài học:** File skill có trên đĩa không có nghĩa là phiên đã nạp skill. Hãy reload skill, hoặc đọc trực tiếp và báo rõ đã làm như vậy.
**Artefact:** Terminal output của lỗi unknown skill.
