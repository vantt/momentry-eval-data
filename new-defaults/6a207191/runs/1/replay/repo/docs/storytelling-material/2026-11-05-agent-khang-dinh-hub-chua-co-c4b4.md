---
id: 2026-11-05-agent-khang-dinh-hub-chua-co-c4b4
code: M-TNKJ
aliases: [M-TNKJ]
date: 2026-11-05
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:6a207191#L1396", "claude:6a207191#L1406", "claude:6a207191#L1417", "claude:6a207191#L1426", "claude:6a207191#L1441"]
hook: "Agent khẳng định hub chưa có routing; thực tế hub có 9 trigger"
tension: tuong_ma_hoa_ra
sides: ["Thư mục local không có skill.yaml nên tưởng hub trống", "Hub đã có 9 trigger, 5 example, 5 not_for"]
strength: 3
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Agent khẳng định hub chưa có routing sau khi chỉ xem thư mục local

**Bối cảnh:** Agent muốn thêm topics, operations và technologies vào skill.yaml, nên kiểm tra xem routing hiện có ở đâu.
**Chuyện gì xảy ra:** Agent chỉ xem thư mục local, thấy không có skill.yaml và kết luận hub chưa có routing. Người dùng hỏi lại thì thực tế hub đã có 9 trigger, 5 example và 5 not_for. skill show --verbose bị từ chối khi chạy từ máy khách, nên chỉ skill_get đọc được routing, nhưng nó không trả về operations, topics, technologies hay min_scope. Agent đã đọc nhầm nguồn và khẳng định sai.
**Bài học:** Trước khi nói 'chưa có', hãy kiểm tra đúng nguồn chứa dữ liệu đó; mỗi giao diện có thể trả về một tập trường khác nhau.
**Artefact:** Bảng 'Trên hub / Thêm vào' ở L1441. Không cần che.
