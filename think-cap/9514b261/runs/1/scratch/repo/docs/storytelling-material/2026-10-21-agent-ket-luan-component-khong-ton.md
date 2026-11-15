---
id: 2026-10-21-agent-ket-luan-component-khong-ton
date: 2026-10-21
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, đảo quyết định]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:9514b261#L492", "claude:9514b261#L508", "claude:9514b261#L513", "claude:9514b261#L530", "claude:9514b261#L542"]
hook: "Agent kết luận component không tồn tại, vì danh sách ẩn 926 mục đã xong"
tension: tuong_ma_hoa_ra
sides: ["Lệnh liệt kê không thấy component nên agent kết luận không có", "Mặc định chỉ hiện 269 mục mở trên tổng 1195, component đã done"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Agent kết luận component “không tồn tại” vì danh sách mặc định ẩn mục đã xong

**Bối cảnh:** Agent tìm trong danh sách work item các mục liên quan đến quản lý quyết định để xác định trạng thái của một component. Lần đầu nó nói ba máy kiểm không thuộc component nào.
**Chuyện gì xảy ra:** Lệnh liệt kê mặc định chỉ trả 269 mục đang mở, trong khi bản đầy đủ có 1195 mục. Component canonical-decision-projection (mục tsk-1lv, sáu mục con) đã done nên không hiện ra. Người dùng nhớ đúng có component này, và agent phải đính chính kết luận trước đó.
**Bài học:** Trước khi kết luận “không có”, tìm lại với cờ lấy cả mục đã đóng, vì danh sách mặc định có thể lọc mất đúng thứ cần tìm.
**Artefact:** Bảng trạng thái các mục tsk-1lv và sáu mục con, kèm cột “nằm trong 269 mục mặc định?” (không) và “trong bản đầy đủ?” (có).
