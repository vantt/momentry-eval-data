---
id: 2026-10-31-doi-danh-tinh-daemon-sang-agents-f60d
code: M-9A43
aliases: [M-9A43]
date: 2026-10-31
repo: repo
status: raw
signals: [so_truoc_so_sau, rang_buoc_thiet_ke]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:f0bf048d#L1983", "claude:f0bf048d#L1987", "claude:f0bf048d#L2400", "claude:f0bf048d#L2409", "claude:f0bf048d#L2435", "claude:f0bf048d#L2436", "claude:f0bf048d#L2457", "claude:f0bf048d#L2543", "claude:f0bf048d#L2550", "claude:f0bf048d#L2569"]
hook: "Tìm thấy PAT của chủ ở 3 chỗ trong home, thu hồi rồi chuyển 12 agent"
tension: nho_ma_to
sides: ["Chỉ là một token, vậy mà nằm rải ở 3 chỗ trong home", "Phải tạo token mới, kiểm dùng được, thu hồi cũ rồi chuyển 12 agent sang danh tính mới"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đổi danh tính daemon sang agents-opc: thu hồi PAT chủ, chuyển 12 agent

**Bối cảnh:** Daemon chạy agent khách đăng nhập bằng PAT chủ. Cần đổi sang user Multica riêng mà không làm gián đoạn agent.
**Chuyện gì xảy ra:** Lệnh sudo lần hai báo lỗi vì file PAT đã bị lệnh lần đầu xoá sau khi dùng. Agent tạo user agents-opc, chia sẻ runtime mới cho chủ, chuyển 12 agent và hai agent của workspace khác sang runtime mới. Tìm thấy PAT chủ ở 3 chỗ trong home, tạo PAT mới, kiểm PAT mới dùng được, rồi thu hồi PAT cũ (trả về 204). Daemon spike là unit tạm nên không có lệnh bật lại.
**Bài học:** Tạo token mới và kiểm nó dùng được trước khi thu hồi token cũ. Ghi lại mọi chỗ token được lưu.
**Artefact:** Bảng số agent và runtime trước và sau chuyển, đã che id.
