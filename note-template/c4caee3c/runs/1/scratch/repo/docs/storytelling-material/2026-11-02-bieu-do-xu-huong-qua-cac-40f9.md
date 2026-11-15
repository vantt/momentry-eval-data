---
id: 2026-11-02-bieu-do-xu-huong-qua-cac-40f9
code: M-HPT9
aliases: [M-HPT9]
date: 2026-11-02
repo: repo
status: raw
signals: [artefact_nhin_duoc]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L2476", "claude:c4caee3c#L2491", "claude:c4caee3c#L2493", "claude:c4caee3c#L2965"]
hook: "Mỗi bản tụt 0,005 không ngưỡng nào bắt, 5 bản tụt 0,025"
tension: cam_ma_van_lot
sides: ["Mỗi lần đều dưới ngưỡng chặn", "Cộng lại tụt 0,025 mà không ai hay"]
strength: 3
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: none
spine_context: Một công cụ tìm kiếm cục bộ trên kho ghi chú Obsidian; người làm đang giữ bản fork của dự án này và đang làm báo cáo review so các bản phát hành.
spine_context_lines: [profile, "claude:c4caee3c#L2476"]
spine_want: "Muốn thấy xu hướng chất lượng qua nhiều bản, không chỉ so hai bản liền nhau."
spine_want_lines: ["claude:c4caee3c#L2476"]
spine_obstacle: "Mỗi báo cáo review chỉ so hai bản, nên không thấy điểm trôi dần."
spine_obstacle_lines: ["claude:c4caee3c#L2476"]
spine_action: Người làm xác nhận làm biểu đồ xu hướng chỉ số qua các bản; V14 đã viết mã và 34 test đã xanh.
spine_action_lines: ["claude:c4caee3c#L2491", "claude:c4caee3c#L2965"]
spine_outcome: Biểu đồ chưa được tạo; báo cáo cuối vẫn đang chạy.
spine_outcome_lines: ["claude:c4caee3c#L2965"]
spine_takeaway: So hai bản liền nhau có thể không lộ ra xu hướng; vẽ điểm qua nhiều bản để thấy.
spine_takeaway_lines: ["claude:c4caee3c#L2476"]
completeness: 6
---

# Biểu đồ xu hướng qua các bản phát hành (đang làm)

**Bối cảnh:** Mỗi báo cáo review chỉ so hai bản, nên không thấy được điểm trôi dần qua nhiều bản.
**Chuyện gì xảy ra:** Chủ dự án xác nhận làm biểu đồ xu hướng. Mục tiêu: sau 5 bản, mỗi bản tụt 0,005 là đã tụt 0,025 dù không lần nào vượt ngưỡng. Code và test đã xong (34 test). Biểu đồ đang chờ lần chạy báo cáo cuối và chưa được tạo khi phiên dừng.
**Bài học:** Ngưỡng cho từng lần so sánh có thể che xu hướng. Vẽ điểm qua thời gian để thấy.
**Artefact:** Biểu đồ chưa tạo; sẽ là ảnh các chỉ số theo bản phát hành.
