---
id: 2026-10-31-bot-ghi-duoc-main-vi-repo
date: 2026-10-31
repo: repo
status: raw
signals: [đảo quyết định có lý do, ràng buộc định hình thiết kế]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L2255", "claude:f0bf048d#L2267", "claude:f0bf048d#L2367", "claude:f0bf048d#L2373", "claude:f0bf048d#L3327", "claude:f0bf048d#L3340"]
hook: "Muốn bot chỉ đọc, nhưng GitHub repo cá nhân cho nó ghi thẳng main"
tension: cam_ma_van_lot
sides: ["định cấp bot quyền chỉ đọc", "repo cá nhân private không có read-only, bot ghi được main"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Bot ghi được main vì repo cá nhân không cấp quyền chỉ đọc: kế hoạch ghi sai và được sửa

**Bối cảnh:** Kế hoạch cần bot đọc được repo nhưng không ghi được main; repo là private cá nhân, gói GitHub Free.
**Chuyện gì xảy ra:** Phương án quyền chỉ đọc không làm được vì GitHub không cấp read-only cho collaborator của repo cá nhân private, nên bot hiện có quyền ghi. Ba lựa chọn: tổ chức miễn phí (chưa chắc có cài đặt fork cho CI), GitHub Pro khoảng 4 USD mỗi tháng để bật bảo vệ main, hoặc hoãn. Người vận hành chọn hoãn. Về sau cơ chế chặn là deploy key chỉ đọc, bộ cài đặt vẫn do chủ push.
**Bài học:** Kiểm khả năng của nền tảng bằng tài liệu trước khi đưa vào kế hoạch; giới hạn bằng cơ chế (không có quyền ghi) thay vì dặn bot đừng ghi.
**Artefact:** Bảng so sánh ba phương án theo chi phí và điều kiện.
