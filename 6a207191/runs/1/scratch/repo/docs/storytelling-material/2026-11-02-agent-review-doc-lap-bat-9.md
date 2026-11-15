---
id: 2026-11-02-agent-review-doc-lap-bat-9
date: 2026-11-02
repo: repo
status: raw
signals: [người duyệt thứ máy soạn, nguyên nhân bất ngờ]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [hotspot, harvest, outsider]
lines: ["claude:6a207191#L661", "claude:6a207191#L673", "claude:6a207191#L681", "claude:6a207191#L690"]
hook: "Agent review tìm ra 9 lỗi, có lỗi nằm ngay trong installer mẫu"
tension: giup_ma_hai
sides: ["Installer mẫu được viết để làm gương cho các rule", "Chính nó vi phạm các rule của skill"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Agent review độc lập bắt 9 vấn đề, có lỗi nằm ngay trong mẫu installer của skill

**Bối cảnh:** Sau khi skill có 230 rule, người dùng nhờ một agent mạnh, suy nghĩ cao, đánh giá độc lập. Agent review chỉ đọc và được giao mục tiêu: UX trước, agent-native, dễ hiểu, dùng lại cách đã kiểm chứng.
**Chuyện gì xảy ra:** Review đóng vai một agent được giao làm Go CLI có MCP server và đi đúng quy trình của skill. Nó tìm ra: hai rule mâu thuẫn về lệnh setup; chuỗi init --yes rồi doctor --fix không bao giờ chạy connect, nên agent chỉ đọc help sẽ không đăng ký được MCP; installer mẫu vi phạm chính các rule của skill; và 'proven ways first' lại trỏ Go CLI sang code Rust. Tổng cộng 9 điểm.
**Bài học:** Nhờ một agent khác đóng vai người dùng đi theo đúng quy trình của tài liệu. Nó bắt được mâu thuẫn mà người viết không thấy, vì người viết đã biết ý định của mình.
**Artefact:** Bảng 9 điểm review, phân loại must-fix và nên sửa, chỉ ghi tên rule.
**Góc người ngoài:** cách làm phổ biến là Tự review lại bài mình viết, hoặc nhờ AI 'xem giúp có ổn không' mà không nói bối cảnh. Hiếm ai cho reviewer chạy thử như người dùng thật; ở đây khác ở Đóng vai người dùng bằng một tình huống cụ thể lộ ra mâu thuẫn mà đọc lướt không thấy. Ví dụ một file bảo dùng lệnh `setup` trong khi file khác cấm lệnh này, hay chuỗi lệnh cho agent không bao giờ đăng ký MCP. Người đọc sẽ hỏi prompt giao việc cần gì và vì sao reviewer chỉ được đọc, không sửa.
