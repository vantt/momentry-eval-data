---
id: 2026-11-03-loi-cai-dat-windows-thu-muc
date: 2026-11-03
repo: repo
status: raw
signals: [nguyên nhân bất ngờ]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L2039", "claude:ab9a1dd8#L2044", "claude:ab9a1dd8#L2049", "claude:ab9a1dd8#L2058", "claude:ab9a1dd8#L2152"]
hook: "Lệnh gỡ cài hứa giữ dữ liệu, nhưng xoá luôn cache"
tension: giup_ma_hai
sides: ["lệnh gỡ cài hứa giữ dữ liệu người dùng", "cache nằm trong thư mục cài nên bị rmdir cùng"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Lỗi cài đặt Windows: thư mục cache nằm trong thư mục cài nên gỡ cài sẽ xoá dữ liệu người dùng

**Bối cảnh:** Trên Windows, đường dẫn cache mặc định nằm trong thư mục app do installer tạo. Lệnh uninstall chỉ giữ cache trên Linux, nơi cache và cài tách nhau.
**Chuyện gì xảy ra:** Reviewer độc lập phát hiện uninstall trên Windows sẽ rmdir cả cache, tức là xoá dữ liệu mà lệnh hứa giữ lại. Agent tách thư mục gốc cài khỏi cache, và thêm kiểm tra tên thư mục cha trước khi xoá. Test lifecycle sau đó xác nhận dữ liệu còn nguyên.
**Bài học:** Khi uninstall xoá theo thư mục cha, hãy kiểm chỗ dữ liệu người dùng thực sự nằm, đặc biệt khi hai thư mục nằm lồng nhau trên một hệ điều hành.
**Artefact:** Sơ đồ thư mục cài và cache trên Windows, với đường dẫn che tên người dùng.
