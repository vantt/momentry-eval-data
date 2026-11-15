---
id: 2026-11-02-onnxruntime-1-30-khong-co-ban
date: 2026-11-02
repo: repo
status: raw
signals: [Ràng buộc định hình thiết kế, Đảo quyết định có lý do, Người duyệt thứ máy soạn]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L2585", "claude:c4caee3c#L2604", "claude:c4caee3c#L2617", "claude:c4caee3c#L2981", "claude:c4caee3c#L3913", "claude:c4caee3c#L3919", "claude:c4caee3c#L3930"]
hook: "Ghim bản cũ cứu Mac Intel, nhưng một hạng mục tụt điểm"
tension: giup_ma_hai
sides: ["ghim onnxruntime 1.23.2 để giữ nền Mac Intel", "vi-synonym tụt 0,017 nên luật chấp nhận phải nới"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# onnxruntime 1.30 không có bản darwin-x64: ghim 1.23.2 và đổi luật chấp nhận

**Bối cảnh:** Upstream dùng onnxruntime-node 1.30.0 và gói npm không có file cho darwin-x64, nên không dựng được gói cho Mac chip Intel.
**Chuyện gì xảy ra:** Đề xuất bỏ nền Mac Intel bị bác. Agent ghim 1.23.2 chỉ cho gói Intel. Đo cùng máy: multilingual +0,063, vi-synonym -0,017, nên danh sách chấp nhận theo từng hạng mục được duyệt. Khi bản vantt.4 cho vi-synonym -0,021 và vi-snippet +0,024, người duyệt đổi luật thành chỉ chặn khi tụt quá 0,01.
**Bài học:** Danh sách chấp nhận cố định lỗi thời mỗi khi dữ liệu đổi; luật chỉ chặn khi tụt ổn định hơn.
**Artefact:** Bảng độ lệch theo hạng mục giữa bản ghim và bản gốc.
