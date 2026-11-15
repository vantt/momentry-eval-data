---
id: 2026-11-03-tha-hang-loat-quarantine-kiem-lai
date: 2026-11-03
repo: repo
status: raw
signals: ["4"]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L3326", "claude:ab9a1dd8#L3333", "claude:ab9a1dd8#L3366", "claude:ab9a1dd8#L3397", "claude:ab9a1dd8#L3400"]
hook: "Thả hàng loạt quarantine, nhưng mục còn lộ thông tin vẫn bị giữ"
tension: cam_ma_van_lot
sides: ["lệnh thả cả loạt mục bị cách ly", "mục còn vi phạm riêng tư vẫn bị giữ lại"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Thả hàng loạt quarantine: kiểm lại từng mục, giữ mục còn lộ thông tin

**Bối cảnh:** Người dùng yêu cầu thêm lệnh momentry quarantine --release all vào mục tiêu đang chạy.
**Chuyện gì xảy ra:** Lệnh mới kiểm lại từng mục trước khi thả. Mục sạch được đưa vào hộp, mục còn vi phạm riêng tư vẫn bị giữ. Thêm một test cho mỗi nhánh, test tổng từ 234 lên 235, và tài liệu tham chiếu lệnh được sinh lại.
**Bài học:** Thả hàng loạt phải kiểm lại từng mục và giữ mục còn lộ, đừng thả theo lô. Test cả hai nhánh.
**Artefact:** Đầu ra lệnh với một mục được thả và một mục bị giữ, che nội dung.
