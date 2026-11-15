---
id: 2026-11-02-routing-song-tren-hub-may-gui
date: 2026-11-02
repo: repo
status: raw
signals: [ràng buộc định hình thiết kế, người duyệt]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:6a207191#L1040", "claude:6a207191#L1060", "claude:6a207191#L1183", "claude:6a207191#L1315", "claude:6a207191#L1346", "claude:6a207191#L1396", "claude:6a207191#L1417", "claude:6a207191#L1441", "claude:6a207191#L1555"]
hook: "Agent bảo skill không có routing, thực ra có sẵn trong mã nguồn"
tension: tuong_ma_hoa_ra
sides: ["Agent khẳng định skill không có routing", "Năm trường routing nằm trong mã nguồn, máy gửi không thấy"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Routing sống trên hub: máy gửi không thấy metadata, phải đọc mã nguồn để biết trường skill.yaml

**Bối cảnh:** Skill được gửi tới một hub chạy trên máy khác. Routing (trigger, example, not_for) do người duyệt đặt trên hub, còn máy gửi không chạy được curator.
**Chuyện gì xảy ra:** skill_get chỉ trả về trigger, example và not_for. skill show --verbose bị từ chối vì phải chạy trên máy hub. Lint báo hub chưa kiểm tra routing vì hub chạy bản cũ. Agent ban đầu nói skill không có routing, người dùng phải sửa lại. Các trường operations, topics, technologies, min_scope và counter_examples chỉ tìm được khi đọc mã nguồn skillstation. Người dùng cũng phàn nàn skillstation-send không quản lý được routing, và agent thừa nhận.
**Bài học:** Khi hub ở xa, giữ skill.yaml trong repo làm nguồn sự thật rồi đẩy đi. Đừng để routing chỉ tồn tại trên hub.
**Artefact:** Bảng hai cột: routing đang có trên hub và trường cần thêm vào skill.yaml.
