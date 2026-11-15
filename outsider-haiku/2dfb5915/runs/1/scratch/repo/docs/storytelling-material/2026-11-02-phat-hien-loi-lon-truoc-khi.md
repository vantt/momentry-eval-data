---
id: 2026-11-02-phat-hien-loi-lon-truoc-khi
date: 2026-11-02
repo: repo
status: raw
signals: []
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [hotspot, outsider]
lines: ["claude:2dfb5915#L591", "claude:2dfb5915#L615", "claude:2dfb5915#L769", "claude:2dfb5915#L819", "claude:2dfb5915#L1038", "claude:2dfb5915#L1045", "claude:2dfb5915#L1780", "claude:2dfb5915#L3286"]
hook: "Một agent đọc code của agent khác, bắt được lỗi treo trước khi merge"
tension: cam_ma_van_lot
sides: ["Code đã viết xong, tác giả tưởng ổn", "Agent review độc lập vẫn tìm ra lỗi treo, ngốn RAM, hạ cấp ngầm"]
strength: 1
stakes: 2
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Phát hiện lỗi lớn trước khi chúng gây hại thật: một agent review độc lập đọc code agent khác và tìm ra lỗi treo, ngốn bộ nhớ, hạ cấp ngầm; rồi gửi lại đúng agent viết code để sửa trên nhánh của nó.

**Chuyện gì xảy ra:** Phát hiện lỗi lớn trước khi chúng gây hại thật: một agent review độc lập đọc code agent khác và tìm ra lỗi treo, ngốn bộ nhớ, hạ cấp ngầm; rồi gửi lại đúng agent viết code để sửa trên nhánh của nó.
**Góc người ngoài:** cách làm phổ biến là Thường tác giả tự review, hoặc chỉ review khi có PR; ít khi có vòng review tự động trước khi merge; ở đây khác ở Người đọc sẽ muốn biết vì sao vòng review này đáng công: nó bắt được lỗi mà test và CI xanh không thấy (ví dụ stdout bị treo khi gặp byte lạ, một gói bị hạ cấp).
