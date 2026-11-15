---
id: 2026-11-05-phat-hien-mot-cho-ux-te-c4b4
code: M-SKHS
aliases: [M-SKHS]
date: 2026-11-05
repo: repo
status: raw
signals: []
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:6a207191#L1515", "claude:6a207191#L1520", "claude:6a207191#L1845", "claude:6a207191#L2008", "claude:6a207191#L2029", "claude:6a207191#L2038", "claude:6a207191#L2103"]
hook: "Thấy trang web không báo có bản chờ duyệt, tôi sửa luôn thay vì mở issue"
tension: khac
sides: ["Thói quen ghi issue rồi chờ", "Sửa tại chỗ ngay khi thấy"]
strength: 1
stakes: 1
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án skillstation là hub chia sẻ skill cho agent, và người làm đang đưa một bộ hướng dẫn đóng gói lên đó. Người làm tưởng skill chưa được duyệt thì sẽ không active; hoá ra hub vẫn giữ bản của lần duyệt trước, còn bản mới nằm ở Waiting for review mà trang skill không báo. Ai dùng hub để chia sẻ skill cho agent nên biết trạng thái active có thể lệch so với bản vừa gửi."
audience: dev dùng hub để chia sẻ skill cho agent
spine_context: Dự án skillstation là hub chia sẻ skill cho agent; người làm đang đưa bộ hướng dẫn đóng gói cs-packaging-distribution lên hub.
spine_context_lines: ["claude:6a207191#L5", "claude:6a207191#L1520"]
spine_want: Muốn hub hiện đúng bản đang chờ duyệt và quản lý được routing/metadata của skill.
spine_want_lines: ["claude:6a207191#L1520"]
spine_obstacle: "Trang skill không báo có bản chờ duyệt, và bản đang active là bản của một lần duyệt trước."
spine_obstacle_lines: ["claude:6a207191#L1503", "claude:6a207191#L1507"]
spine_turn: "Tưởng skill chưa được duyệt thì không thể active; hoá ra hub vẫn giữ bản của lần duyệt trước, còn bản gửi mới chỉ nằm ở Waiting for review."
spine_turn_lines: ["claude:6a207191#L1489", "claude:6a207191#L1503"]
spine_action: "Thêm thông báo bản chờ duyệt vào trang skill và danh sách skill, rồi gộp và đẩy lên main."
spine_action_lines: ["claude:6a207191#L2008", "claude:6a207191#L2103"]
spine_outcome: "Web qua 229 test, kiểm tra kiểu, lint và build đều sạch; commit 185b75d đã lên main và CI đang chạy. Hub chưa đổi vì cần phát hành bản mới."
spine_outcome_lines: ["claude:6a207191#L2008", "claude:6a207191#L2103"]
spine_takeaway: "Trạng thái active trên hub có thể đến từ lần duyệt cũ; trước khi tin bản mới đã lên, hãy xem mục Waiting for review."
spine_takeaway_lines: ["claude:6a207191#L1503", "claude:6a207191#L1515"]
completeness: 7
---

# Phát hiện một chỗ UX tệ trên sản phẩm (trang web không báo có bản chờ duyệt) và sửa tại chỗ thay vì chỉ ghi nhận

**Góc kể:** Dự án skillstation là hub chia sẻ skill cho agent, và người làm đang đưa một bộ hướng dẫn đóng gói lên đó. Người làm tưởng skill chưa được duyệt thì sẽ không active; hoá ra hub vẫn giữ bản của lần duyệt trước, còn bản mới nằm ở Waiting for review mà trang skill không báo. Ai dùng hub để chia sẻ skill cho agent nên biết trạng thái active có thể lệch so với bản vừa gửi.
**Chuyện gì xảy ra:** Phát hiện một chỗ UX tệ trên sản phẩm (trang web không báo có bản chờ duyệt) và sửa tại chỗ thay vì chỉ ghi nhận
**Góc người ngoài:** cách làm phổ biến là Hầu hết người ta ghi thành issue rồi chờ, hoặc chỉ nhắc với người phụ trách; ở đây khác ở Phiên này đọc mã nguồn web, viết thêm component kèm test, chạy đủ kiểm tra kiểu, lint, build và đẩy lên, rồi báo rõ phần nào chưa kiểm tra bằng trình duyệt thật. Người đọc sẽ hỏi vì sao làm được nhanh như vậy và vì sao dừng lại trước bước mở PR.
