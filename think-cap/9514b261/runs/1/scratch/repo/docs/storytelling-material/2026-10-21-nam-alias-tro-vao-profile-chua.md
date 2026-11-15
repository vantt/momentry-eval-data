---
id: 2026-10-21-nam-alias-tro-vao-profile-chua
date: 2026-10-21
repo: repo
status: raw
signals: [artefact nhìn được, số trước/sau]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L3550", "claude:9514b261#L3570", "claude:9514b261#L3600"]
hook: "Năm alias trỏ vào thư mục chưa tồn tại, sáu tài khoản chỉ có alias"
tension: khac
sides: ["Alias zsh trông như tài khoản đã sẵn sàng", "Khoảng sáu alias trỏ vào chỗ trống, chưa có profile"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Năm alias trỏ vào profile chưa có, và sáu tài khoản chỉ có alias zsh

**Bối cảnh:** Người dùng yêu cầu liệt kê toàn bộ alias của các tài khoản LLM trên máy, đọc từ shell tương tác để chắc alias đang có hiệu lực.
**Chuyện gì xảy ra:** Có alias cho codex, pi, omp và agy. Khoảng sáu alias trỏ vào thư mục chưa tồn tại. Agent tạo khung profile cho bốn alias omp theo người dùng chọn và không sửa zshrc. Còn một alias trỏ vào chỗ trống.
**Bài học:** Alias không đồng nghĩa với profile tồn tại; kiểm đồng loạt cả alias lẫn thư mục đích.
**Artefact:** Bảng alias → thư mục → trạng thái (có, chưa có) với tên tài khoản đã che.
