---
id: 2026-10-21-alias-tro-vao-thu-muc-chua
date: 2026-10-21
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L3531", "claude:9514b261#L3546", "claude:9514b261#L3570", "claude:9514b261#L3591"]
hook: "Tám alias, bốn cái trỏ vào thư mục không tồn tại"
tension: cam_ma_van_lot
sides: ["Alias trông đã cấu hình xong", "Bốn profile chưa hề có thư mục"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Alias trỏ vào thư mục chưa tồn tại

**Bối cảnh:** Máy có nhiều alias cho nhiều tài khoản của các CLI.
**Chuyện gì xảy ra:** Liệt kê alias bằng shell tương tác cho thấy tám alias omp trỏ vào profile, trong đó bốn profile chưa có thư mục. Agent tạo khung profile chỉ có cấu hình, không có đăng nhập, để alias và công tắc chạy được. Không alias nào bị xoá.
**Bài học:** Alias tồn tại không có nghĩa là profile tồn tại. Kiểm bằng lệnh chạy thật thay vì chỉ grep file rc.
**Artefact:** Bảng alias | profile | có hay không đăng nhập. Không ghi tên tài khoản.
