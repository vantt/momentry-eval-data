---
id: 2026-11-03-du-lieu-nam-trong-thu-muc
date: 2026-11-03
repo: repo
status: raw
signals: ["2"]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L2026", "claude:ab9a1dd8#L2049", "claude:ab9a1dd8#L2151"]
hook: "Uninstall hứa giữ dữ liệu, nhưng xoá luôn cache cùng thư mục cài"
tension: giup_ma_hai
sides: ["uninstall hứa giữ lại dữ liệu người dùng", "cache nằm chung thư mục cài nên bị xoá theo"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Dữ liệu nằm trong thư mục cài trên Windows: uninstall sẽ xoá cache

**Bối cảnh:** Trên Windows, thư mục cache của momentry nằm bên trong thư mục cài đặt. Uninstall giữ cache nhưng lại lập lịch xoá thư mục cha.
**Chuyện gì xảy ra:** Reviewer phát hiện rằng uninstall hứa giữ dữ liệu nhưng thực tế sẽ xoá cache cùng thư mục cài. Agent tách thư mục chương trình và thư mục dữ liệu, rồi thêm kiểm tra chủ sở hữu trước khi xoá, kèm điều kiện cho --purge.
**Bài học:** Tách thư mục chương trình và thư mục dữ liệu ngay từ đầu. Uninstall chỉ được xoá thứ mình tạo ra, và phải kiểm chủ sở hữu trước.
**Artefact:** Sơ đồ thư mục trên Windows trước và sau khi tách.
