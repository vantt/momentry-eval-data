---
id: 2026-11-02-skill-ak-frontend-development-khong-nap
date: 2026-11-02
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:6a207191#L317", "claude:6a207191#L1525", "claude:6a207191#L1532", "claude:6a207191#L1545", "claude:6a207191#L1561", "claude:6a207191#L1573", "claude:6a207191#L1585", "claude:6a207191#L1592", "claude:6a207191#L1593"]
hook: "Skill báo 'chạy được ngay', nhưng gõ tên ra Unknown skill"
tension: tuong_ma_hoa_ra
sides: ["Lời hứa skill chạy được ngay sau khi đổi tên", "Gọi tên thì Unknown skill, phải reload hoặc đọc thẳng file"]
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Skill 'ak:frontend-development' không nạp được: đổi tên và chưa reload, agent đọc thẳng file

**Bối cảnh:** Trước đó agent nói skill chạy được ngay vì đã symlink vào thư mục skill. Sau đó người dùng nhờ dùng ak:frontend-development.
**Chuyện gì xảy ra:** Gọi 'ak:frontend-development' báo Unknown skill, skill_get cũng không thấy. Tìm trên máy thì skill nằm trong thư mục skill của project với tên ak-frontend-development (gạch ngang). Skill chưa được nạp vào phiên, nên agent đọc thẳng SKILL.md và làm theo. Skill mới muốn hiện trong danh sách phải chạy reload-skills, nên lời 'chạy được ngay' lúc đầu không đúng.
**Bài học:** Kiểm tên đúng trong danh sách skill đang nạp. Sau khi thêm skill phải reload. Đọc tay file hướng dẫn là đường lùi, không phải là đã nạp skill.
**Artefact:** Thông báo Unknown skill và tên thư mục skill, không kèm đường dẫn.
