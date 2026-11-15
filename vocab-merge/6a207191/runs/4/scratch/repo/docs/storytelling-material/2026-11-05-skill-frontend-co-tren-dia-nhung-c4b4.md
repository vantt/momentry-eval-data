---
id: 2026-11-05-skill-frontend-co-tren-dia-nhung-c4b4
code: M-5C5Y
aliases: [M-5C5Y]
date: 2026-11-05
repo: repo
status: raw
signals: [ràng buộc thiết kế, khác]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:6a207191#L1525", "claude:6a207191#L1532", "claude:6a207191#L1534", "claude:6a207191#L1555", "claude:6a207191#L1573", "claude:6a207191#L1592"]
hook: "Hub xếp việc frontend vào skill packaging, agent từ chối và tự đọc"
tension: nguoi_dung_may_sai
sides: ["Hub trả cs-packaging-distribution, độ tin cậy medium", "Agent từ chối kết quả sai và đọc thẳng SKILL.md frontend"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Skill frontend có trên đĩa nhưng không nạp vào phiên; routing kéo việc frontend sang skill packaging

**Bối cảnh:** Người dùng yêu cầu dùng skill ak:frontend-development để sửa web UI của skillstation.
**Chuyện gì xảy ra:** Skill nằm trong .claude/skills của dự án nhưng chưa được nạp vào phiên nên các lần gọi bằng tên đều báo không tìm thấy. Khi hỏi skill_resolve cho việc frontend, hub trả về cs-packaging-distribution với độ tin cậy medium, tức là chọn sai vì việc này không liên quan đến packaging. Agent từ chối kết quả đó và đọc thẳng SKILL.md của ak-frontend-development để làm theo.
**Bài học:** Các việc gần giống nhau (frontend và packaging) cần not_for để tránh routing sai; nếu không, một từ khóa như install hay release sẽ kéo nhầm skill.
**Artefact:** Đoạn kết quả skill_resolve với độ tin cậy medium. Cần che snapshot id nếu có.
