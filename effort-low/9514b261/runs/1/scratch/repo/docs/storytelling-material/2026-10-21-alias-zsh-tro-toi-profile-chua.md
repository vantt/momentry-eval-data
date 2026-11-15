---
id: 2026-10-21-alias-zsh-tro-toi-profile-chua
date: 2026-10-21
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, artefact nhìn được]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L3531", "claude:9514b261#L3546", "claude:9514b261#L3600"]
hook: "9 alias omp, 4 cái trỏ vào thư mục không tồn tại"
tension: cam_ma_van_lot
sides: ["Grep file rc nhìn thấy alias có vẻ ổn", "Shell thật liệt kê 9 alias, 4 cái trỏ tới profile chưa có"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Alias zsh trỏ tới profile chưa tồn tại, grep rc file không thấy đủ

**Bối cảnh:** Người dùng muốn danh sách alias của tài khoản LLM. Agent đọc file rc trước, rồi đổi sang shell tương tác để lấy alias thật có hiệu lực.
**Chuyện gì xảy ra:** Shell tương tác liệt kê alias khác với grep file rc. Có 9 alias omp, trong đó 4 trỏ tới profile chưa có thư mục. Agent tạo khung profile cho 4 alias và để alias tự lưu đăng nhập sau.
**Bài học:** Đọc alias từ shell tương tác thật, không grep file cấu hình. Alias trỏ đến thư mục trống chỉ lộ ra khi chạy.
**Artefact:** Bảng alias theo CLI, có cột đăng nhập và cột profile tồn tại (che giá trị bí mật).
