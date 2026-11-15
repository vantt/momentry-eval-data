---
id: 2026-11-02-nguoi-dung-bo-sung-rang-buoc-40f9
code: M-T4WP
aliases: [M-T4WP]
date: 2026-11-02
repo: repo
status: raw
signals: []
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:c4caee3c#L2129", "claude:c4caee3c#L2394", "claude:c4caee3c#L2404", "claude:c4caee3c#L2459", "claude:c4caee3c#L2695", "claude:c4caee3c#L3787", "claude:c4caee3c#L3919"]
hook: "Ràng buộc mới chỉ nằm trong chat thì vài lượt sau là quên"
tension: khac
sides: ["Người dùng đã nói rõ ràng buộc", "Tài liệu và code không ghi lại"]
strength: 1
stakes: 0
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Người dùng bổ sung ràng buộc mới giữa chừng (ví dụ 'không được đưa vault thật lên remote', 'bỏ tự động đuổi theo upstream', 'chỉ chặn khi tụt') và agent cập nhật cả PRD, plan và mã trong cùng một lượt commit.

**Chuyện gì xảy ra:** Người dùng bổ sung ràng buộc mới giữa chừng (ví dụ 'không được đưa vault thật lên remote', 'bỏ tự động đuổi theo upstream', 'chỉ chặn khi tụt') và agent cập nhật cả PRD, plan và mã trong cùng một lượt commit.
**Góc người ngoài:** cách làm phổ biến là Thường ràng buộc mới chỉ nằm trong chat và bị quên sau vài lượt; tài liệu lệch khỏi mã; ở đây khác ở Mỗi quyết định của người dùng đều được ghi lại vào PRD/plan kèm ngày chốt và thường được commit ngay, nên khi phiên bị nén ngữ cảnh vẫn còn dấu vết để tiếp tục.
