---
id: 2026-10-31-daemon-agent-dang-nhap-bang-pat
date: 2026-10-31
repo: repo
status: raw
signals: ["3", "2", "5"]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L1875", "claude:f0bf048d#L1878", "claude:f0bf048d#L1966", "claude:f0bf048d#L2105", "claude:f0bf048d#L2536", "claude:f0bf048d#L2550", "claude:f0bf048d#L2578"]
hook: "Daemon agent chạy bằng PAT của chủ, và grep ra đúng 3 bản sao"
tension: cam_ma_van_lot
sides: ["Agent chỉ phục vụ 2 workspace", "Nhưng mang PAT của chủ, copy ở 3 chỗ"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Daemon agent đăng nhập bằng PAT của chủ, và cách cắt

**Bối cảnh:** Daemon chạy agent nghiệp vụ trên Multica đăng nhập bằng PAT của chủ workspace, nên agent có thể mạo danh chủ.
**Chuyện gì xảy ra:** Bản phản biện chỉ ra máy có mã đăng nhập dev 6 ký tự trong .env và daemon agent dùng PAT chủ. Grep trong home tìm thấy đúng 3 bản sao PAT. Tạo PAT mới, kiểm PAT mới chạy được rồi mới thu hồi PAT cũ (HTTP 204). Sau đó tạo user agents-opc chỉ là member của 2 workspace, chuyển daemon sang user này.
**Bài học:** Đừng để daemon agent đăng nhập bằng token của chủ; tạo user riêng cho agent và grep bản sao token trước khi thu hồi.
**Artefact:** Bảng 3 vị trí PAT (đã che giá trị) và kết quả: cũ 204, mới hoạt động.
